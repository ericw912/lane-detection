Deep Learning-Based Lane Detection for Autonomous Driving
Group Members: Hui Zhi, Di Zhang, Chingyi Wang
Problem Statement
Our goal for this project is to develop and evaluate a lane detection system which could accurately detect and segment lane markings from a front-facing vehicle camera. The main challenge is to build a system that performs reliably under diverse real-world conditions, including poor lighting, adverse weather, shadows, and curved or faded lanes.
Motivation
In the real road conditions, lane detection plays an important role in modern Advanced Driver-Assistance Systems (ADAS), directly impacting vehicle safety and reliability. Precise lane detection could directly improve the performance for self-driving vehicles, enabling functions like Lane Keeping Assist and navigation. While traditional computer vision methods often fail in difficult scenarios, deep learning–based semantic segmentation can capture fine-grained visual features, offering a more robust and generalizable solution. Our project wants to show how computer vision and machine learning work together to achieve this goal. 
Dataset Description
We will utilize the TuSimple Lane Detection Dataset, a well-established highway benchmark providing thousands of annotated frames from front-facing cameras across varied conditions (different times of day, good/medium weather, multi-lane traffic).
Source: https://github.com/TuSimple/tusimple-benchmark
Method
We will implement and compare two approaches:
1. Classical Baseline: Classical OpenCV Method
Convert images to grayscale and apply Gaussian blur, detect edges using Canny, apply ROI masking, and extract lane lines with the Hough Transform.
2. Proposed Method: U-Net for Semantic Segmentation
We will train a U-Net model (or SegNet variant) using PyTorch or TensorFlow to classify each pixel as “lane” or “background.” Data augmentation (e.g., brightness, flips, perspective transforms) will improve generalization. Training will be performed on GPU (e.g., Google Colab). If time permits, we may explore lightweight variants like Mobile U-Net.


