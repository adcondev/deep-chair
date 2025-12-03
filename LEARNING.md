# LEARNING.md

## Project Overview

This project, "Deep Chair," is a real-time facial gesture recognition system designed to control a motorized wheelchair. It uses a deep learning model to classify facial gestures from a webcam feed and sends corresponding commands to an Arduino-controlled motor driver. The system is built in Python and leverages computer vision and deep learning techniques to provide an alternative control method for users with limited mobility.

## Tech Stack and Key Technologies

*   **Languages:** Python
*   **Deep Learning Frameworks:**
    *   **PyTorch:** Core framework for model definition, loading pre-trained weights (ResNet-18), and inference.
    *   **Torchvision:** Used for accessing the ResNet-18 architecture and implementing complex image transformations (CenterCrop, RandomResizedCrop, Normalization) for data augmentation.
*   **Computer Vision & Image Processing:**
    *   **OpenCV (cv2):** Primary tool for real-time video capture, frame extraction, and overlaying text on the video feed.
    *   **scikit-image:** Used for additional image processing tasks.
    *   **PIL (Python Imaging Library):** Used in conjunction with Torchvision for image format compatibility.
*   **Data Science & Utilities:**
    *   **NumPy & Pandas:** For efficient numerical computation and data structure management.
    *   **Matplotlib:** For visualizing training progress and model predictions.
*   **Hardware Interface:**
    *   **PySerial:** Critical for establishing serial communication (UART) between the Python application and the Arduino microcontroller.
    *   **Arduino:** The embedded system receiving control commands ('0', '1', '2', '3', '4') to drive the wheelchair motors.

## Notable Libraries

*   **`torchvision`:** A key PyTorch library used for accessing pre-trained models like ResNet-18, as well as for applying common image transformations and data augmentation techniques. This was crucial for implementing transfer learning.
*   **`pyserial`:** This library was essential for the hardware integration aspect of the project, enabling the Python script to send control signals to the Arduino over a serial port.
*   **`OpenCV-Python`:** The primary tool for capturing the video feed from the webcam and performing necessary color space conversions and display functionalities.

## Major Achievements and Skills Demonstrated

*   **End-to-End AI Application Development:**
    *   Built a complete system connecting a high-level Python AI application with low-level hardware control.
    *   Orchestrated the flow from **Webcam Input -> Preprocessing -> Deep Learning Inference -> Serial Output -> Physical Action**.

*   **Transfer Learning & Model Fine-Tuning:**
    *   Successfully implemented **Transfer Learning** using a pre-trained **ResNet-18** model.
    *   Modified the fully connected layer (`model.fc`) to match the specific 5-class problem (Up, Down, Left, Right, Neutral).
    *   Implemented a training loop with **SGD optimizer**, **CrossEntropyLoss**, and **Learning Rate Scheduling** (`StepLR`).

*   **Real-Time Computer Vision Pipeline:**
    *   Developed a real-time inference loop in `ControlFacial.py` that processes video frames on the fly.
    *   Optimized performance by using **CUDA** (GPU acceleration) when available, ensuring low-latency control signals.
    *   Handled real-time video streams and gracefully managed hardware exceptions (e.g., Arduino disconnection).

*   **Robust Data Pipeline:**
    *   Created a comprehensive data augmentation strategy in `TransferLearning.py` using `transforms.RandomResizedCrop` and `transforms.Normalize` to improve model generalization and robustness against lighting/position variations.

## Skills Gained/Reinforced

*   **Deep Learning Engineering:** Practical experience with CNNs, hyperparameter tuning, and managing training/validation splits.
*   **Embedded Systems Integration:** Bridging the gap between software and hardware using Serial communication protocols.
*   **Python Proficiency:** Advanced usage of libraries like `torch`, `cv2`, and `serial` to build complex, multi-component systems.
*   **Problem Solving:** Addressing real-world constraints like real-time processing requirements and hardware availability checks.