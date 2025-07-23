# 💪 AI Bicep Curl Counter with Pose Tracking

![Python](https://img.shields.io/badge/Python-3.7+-blue?logo=python)
![OpenCV](https://img.shields.io/badge/OpenCV-4.5+-green?logo=opencv)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0.8.9+-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)

A real-time computer vision application that counts your bicep curls using MediaPipe's pose detection and OpenCV. Perfect for tracking your workouts with just a webcam!

## ✨ Features

- **Real-time pose tracking** using your webcam
- **Accurate rep counting** with smart angle thresholding
- **Visual feedback**:
  - Dynamic angle visualization between arm segments
  - Strength meter showing range of motion
  - Clear rep counter display
- **Lightweight** implementation with minimal dependencies
- **Customizable thresholds** for different users
- 
### Prerequisites

- Python 3.7+
- Webcam

### Installation

1. Clone the repository:
```bash
git clone https://github.com/ammarsaqib-programmer/bicep-curl-counter.git
cd bicep-curl-counter
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

### Usage
```bash
python bicep_curl_counter.py
```
- Position yourself 1-2 meters from the camera
- Ensure your right arm is fully visible
- Perform bicep curls at a steady pace
- Press 'Q' to quit the application

## 🛠️ How It Works

1. **Pose Detection**:
   - Uses MediaPipe's Pose model to detect 33 body landmarks
   - Focuses on right arm landmarks (shoulder, elbow, wrist)

2. **Angle Calculation**:
   ```python
   lower_arm_angle = math.degrees(math.atan2((y2-y3),(x3-x2)))
   upper_arm_angle = math.degrees(math.atan2((y2-y1),(x2-x1)))
   ```

3. **Rep Counting Logic**:
   - Counts a rep when:
     - Arm bends beyond 150° (down position)
     - Returns below 45° (up position)

4. **Visual Feedback**:
   - Draws real-time arm segments and angle arc
   - Displays strength meter and rep counter

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

## 📧 Contact

Ammar Saqib - [@ammarsaqib-programmer](https://github.com/ammarsaqib-programmer)

## 🙏 Acknowledgments

- MediaPipe team for the excellent pose detection model
- OpenCV for computer vision capabilities
- Python community for awesome libraries
```
