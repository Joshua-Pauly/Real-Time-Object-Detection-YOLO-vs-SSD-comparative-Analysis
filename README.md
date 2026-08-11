Status: I am actively working to get the repository set up.
This was my Masters capstone project in May 2025.

This project is a comparative analysis of the two most common real time object detectors (YOLO and SSD). 

YOLO (You Only Look Once) and SSD (Single Shot MultiBox Detector) are single-stage object detectors that predict object classes and bounding boxes in one forward pass: YOLO divides the input image into a grid and directly predicts bounding box coordinates, objectness scores, and class probabilities for each cell, optimizing for real-time throughput by treating detection as a regression problem; SSD places a set of default (anchor) boxes of different scales and aspect ratios over multiple feature maps, predicts class scores and box offsets for each anchor, and combines detections across scales to handle objects of varying sizes, leveraging multiple convolutional feature layers to balance speed and localization across resolutions.
