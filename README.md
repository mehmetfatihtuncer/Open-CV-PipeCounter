# Open-CV-PipeCounter
Pipe Counting Project
This project aims to count the number of pipes present in an image of pipes stored in a truck or car.

Getting Started
Prerequisites
Python 3.7+
OpenCV
Numpy
Matplotlib
Installing
Clone this repository:

bash
Copy code
git clone https://github.com/mehmetfatihtuncer/Open-CV-PipeCounter.git
Usage
Place an image of pipes in a truck or car in the root directory of the project and name it pipe.jpeg.
Run the pipe_counting.py script using the following command:
Copy code
python pipe_counting.py
The script will output the number of pipes detected in the image and display the image with the detected pipes circled in red.
How it Works
The script uses OpenCV to perform the following steps:

Convert the image to the HSV color space and apply a color mask to isolate orange objects (assumed to be pipes).
Convert the resulting image to grayscale and apply a Gaussian blur to reduce noise.
Use Canny edge detection to identify the edges of the objects in the image.
Dilate the edges to connect any gaps in the edges.
Use contour detection to identify the objects in the image and draw them on a copy of the original image.
Compute the center of each contour and draw a red dot on the original image at the center of each contour.
Count the number of contours detected and output the count.
