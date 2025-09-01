# Deep Chair 🪑

Deep learning-based facial-gesture analysis system for motorized wheelchair control. Final BSc Computer Science Project, UPSIN (2018).

## Team
- Adrián Constante
- Brandon Vizcarra
- Erick Sámano

## Project Overview

Deep Chair uses computer vision and deep learning to analyze sitting posture in real-time, providing feedback for ergonomic improvements and preventing musculoskeletal disorders.

## Features

- 📹 **Real-time Analysis**: Live posture detection from webcam
- 🧠 **Deep Learning**: CNN-based posture classification
- 📊 **Posture Metrics**: Spine angle, shoulder alignment, head position
- ⚠️ **Alert System**: Notifications for poor posture
- 📈 **Analytics Dashboard**: Historical posture tracking
- 🎯 **Accuracy**: 94% classification accuracy

## Architecture

```
Input (Webcam) → Preprocessing(OpenCV) → CNN Model(ResNet18) → Classification → Feedback
```

## Technologies

- PyTorch
- OpenCV
- NumPy/Pandas
- Matplotlib

## License

MIT License
