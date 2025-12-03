# LEARNING.md

## Project Overview

**Deep Chair** is a real-time facial gesture recognition system designed to provide hands-free control for motorized wheelchairs. The objective was to create an assistive technology that translates specific facial expressions (Up, Down, Left, Right, Neutral) into physical motor commands. The system integrates a deep learning classification model with a computer vision pipeline and an embedded hardware interface, demonstrating a complete end-to-end AI application from input (webcam) to actuation (Arduino-controlled motors).

## Tech Stack and Key Technologies

*   **Languages:** Python 3.x, C++ (Arduino Firmware)
*   **Deep Learning:** PyTorch, Torchvision
*   **Computer Vision:** OpenCV (cv2)
*   **Hardware Interface:** PySerial, Arduino
*   **Data Processing:** NumPy
*   **Visualization:** Matplotlib

## Notable Libraries

*   **`torchvision`:** Used for Transfer Learning. Leveraged the pre-trained **ResNet-18** architecture and its image transformation utilities (`transforms`) to fine-tune a model on a custom facial gesture dataset.
*   **`OpenCV` (cv2):** The core of the real-time pipeline. Handled video capture, frame preprocessing (resizing, color conversion), and the graphical overlay of predictions on the live feed.
*   **`pyserial`:** Enabled the critical bridge between the high-level Python AI model and the low-level Arduino hardware, managing serial communication protocols to send control signals.

## Major Achievements and Skills Demonstrated

*   **End-to-End AI System Design:**
    *   Designed and implemented a full stack AI solution that captures real-world data, processes it with a deep neural network, and actuates physical hardware in real-time.
    *   Bridged the gap between software (Python/PyTorch) and hardware (Arduino/Serial), handling latency and communication stability.

*   **Transfer Learning & Model Fine-Tuning:**
    *   Adapted a **ResNet-18** model (pre-trained on ImageNet) for a specific 5-class classification task.
    *   Modified the fully connected layer to match the target output and implemented a custom training loop with **CrossEntropyLoss** and **SGD** optimization.
    *   Utilized **Learning Rate Scheduling** (`StepLR`) to optimize model convergence during training.

*   **Real-Time Computer Vision Pipeline:**
    *   Developed a low-latency inference loop in `ControlFacial.py` capable of processing video frames, running model inference, and sending hardware commands within milliseconds.
    *   Implemented robust error handling for hardware connections (e.g., auto-detecting Arduino ports).

*   **Custom Dataset Creation & Augmentation:**
    *   Built a custom dataset structure for facial gestures.
    *   Implemented data augmentation techniques (RandomResizedCrop, Normalization) using `torchvision.transforms` to improve model generalization and robustness against lighting and pose variations.

## Skills Gained/Reinforced

*   **Deep Learning Engineering:** Practical application of CNNs (Convolutional Neural Networks), Transfer Learning, and model evaluation.
*   **Computer Vision:** Real-time video processing, image manipulation, and integration with ML models.
*   **Embedded Systems Integration:** Serial communication (UART) and interfacing high-level software with microcontrollers.
*   **Python Development:** Proficiency in scientific computing libraries (NumPy) and managing external hardware dependencies.
*   **System Architecture:** Designing modular systems where data acquisition, processing, and actuation are decoupled but synchronized.