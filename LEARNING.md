# LEARNING.md

## Project Overview

This project, "Deep Chair," is a real-time facial gesture recognition system designed to control a motorized wheelchair. It uses a deep learning model to classify facial gestures from a webcam feed and sends corresponding commands to an Arduino-controlled motor driver. The system is built in Python and leverages computer vision and deep learning techniques to provide an alternative control method for users with limited mobility.

## Tech Stack and Key Technologies

*   **Languages:** Python
*   **Frameworks and Libraries:**
    *   **PyTorch:** Used for building, training, and deploying the deep learning model.
    *   **OpenCV:** Employed for real-time video capture from the webcam and image preprocessing.
    *   **scikit-image:** Utilized for image transformations.
    *   **NumPy & Pandas:** Leveraged for numerical operations and data manipulation.
    *   **Matplotlib:** Used for data visualization and plotting during model training and evaluation.
*   **Hardware:**
    *   **Arduino:** Used as an intermediary to control the wheelchair's motors based on signals received from the Python script.
    *   **Serial Communication:** The `pyserial` library was used to establish communication between the computer running the Python script and the Arduino.

## Notable Libraries

*   **`torchvision`:** A key PyTorch library used for accessing pre-trained models like ResNet-18, as well as for applying common image transformations and data augmentation techniques. This was crucial for implementing transfer learning.
*   **`pyserial`:** This library was essential for the hardware integration aspect of the project, enabling the Python script to send control signals to the Arduino over a serial port.
*   **`OpenCV-Python`:** The primary tool for capturing the video feed from the webcam and performing necessary color space conversions and display functionalities.

## Major Achievements and Skills Demonstrated

*   **Designed and Implemented a Real-Time Facial Gesture Recognition System:** Developed a complete pipeline from video capture to hardware control, capable of processing video in real-time.
*   **Implemented Transfer Learning for Image Classification:** Fine-tuned a pre-trained ResNet-18 convolutional neural network (CNN) on a custom dataset of facial gestures, achieving high classification accuracy.
*   **Integrated a Deep Learning Model with External Hardware:** Successfully established serial communication between a Python application and an Arduino, allowing the deep learning model's predictions to control physical motors.
*   **Developed a Data Preprocessing and Augmentation Pipeline:** Created a pipeline using `torchvision.transforms` to prepare and augment the image dataset for training, which included resizing, cropping, normalization, and other techniques to improve model generalization.
*   **Engineered a Standalone Control Application:** The `ControlFacial.py` script serves as a complete application that captures video, performs inference with the trained model, and sends commands to the hardware, demonstrating the ability to create end-to-end solutions.

## Skills Gained/Reinforced

*   **Deep Learning:** Convolutional Neural Networks (CNNs), Transfer Learning, Model Training and Evaluation.
*   **Computer Vision:** Real-Time Image and Video Processing, Image Preprocessing, Data Augmentation.
*   **Hardware Integration:** Interfacing software with microcontrollers (Arduino), Serial Communication.
*   **Software Engineering:** Modular code structure, dependency management (implicitly), creating end-to-end applications.
*   **API Usage:** Proficient use of PyTorch, OpenCV, and NumPy APIs.