# 🚗 Vehicle Counter using OpenCV

> A computer vision project that counts vehicles crossing a designated line in a video using background subtraction and contour detection.

![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)
![OpenCV](https://img.shields.io/badge/OpenCV-4.0+-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## 📋 Description

This project uses OpenCV to detect and count vehicles passing through a virtual counting line in a video. It employs background subtraction techniques to identify moving objects and tracks them as they cross a predefined boundary.

---

## ✨ Features

- ✅ Real-time vehicle detection using background subtraction
- ✅ Automatic counting when vehicles cross the counting line
- ✅ Visual feedback with bounding boxes and center points
- ✅ Configurable detection parameters
- ✅ Counter display on video feed

---

## 📦 Requirements

```text
opencv-python
opencv-contrib-python
numpy
```

---

## 🚀 Installation

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/vehicle-counter.git
cd vehicle-counter
```

### Step 2: Install Dependencies
```bash
pip install opencv-python opencv-contrib-python numpy
```

### Step 3: Add Your Video
Place your video file in the project directory and name it `video.mp4` (or update the file path in the code)

---

## 💻 Usage

Run the script:
```bash
python vehicle_counter.py
```

### What Happens:
- ▶️ Opens and processes the video file
- 🟢 Displays the video with detected vehicles marked by green rectangles
- 📏 Shows a counting line across the frame
- 🔢 Counts vehicles as they cross the line
- 📊 Displays the total count on screen

**Press `Enter` to stop the program.**

---

## ⚙️ Configuration Parameters

| Parameter | Description | Default Value |
|-----------|-------------|---------------|
| `min_width_react` | Minimum width of detected rectangle | 80 |
| `min_height_react` | Minimum height of detected rectangle | 80 |
| `count_line_position` | Y-coordinate of counting line | 550 |
| `offset` | Allowable pixel error for counting | 6 |

You can adjust these parameters in the code to fine-tune detection for your specific video.

---

## 🔍 How It Works

1. **Background Subtraction**: Uses MOG (Mixture of Gaussians) algorithm to separate foreground (vehicles) from background
2. **Preprocessing**: Applies Gaussian blur and morphological operations to reduce noise
3. **Contour Detection**: Identifies vehicle shapes using contour detection
4. **Center Tracking**: Calculates center point of each detected vehicle
5. **Line Crossing Detection**: Counts vehicles when their center crosses the counting line

---

## 🎨 Customization

### Use with Different Video:
```python
cap = cv2.VideoCapture('your_video.mp4')
```

### Use with Webcam:
```python
cap = cv2.VideoCapture(0)  # 0 for default webcam
```

---

## 📊 Output

The program displays:

- 🎥 Original video with annotations
- 🟢 Green rectangles around detected vehicles
- 🔴 Red circles at vehicle centers
- 🟠 Orange/blue counting line
- 🔢 Real-time vehicle count
- 💬 Console output for each counted vehicle

---

## ⚠️ Limitations

- 📹 Works best with static camera angles
- 💡 Performance depends on video quality and lighting conditions
- 🔧 May require parameter tuning for different scenarios
- 🌦️ Background subtraction can be sensitive to environmental changes

---

## 🔧 Troubleshooting

| Issue | Solution |
|-------|----------|
| No vehicles detected | Adjust `min_width_react` and `min_height_react` values |
| False positives | Increase minimum size parameters or adjust morphological operations |
| Missed vehicles | Lower the offset value or adjust counting line position |
| Video not found | Verify video file path and name |

---

## 📌 Important Notes

> **Note:** This project requires `opencv-contrib-python` for the `cv2.bgsegm.createBackgroundSubtractorMOG()` function.

> **Tip:** For best results, use videos with:
> - Static camera position
> - Good lighting conditions
> - Clear view of vehicles
> - Minimal background movement

---


## 🙏 Acknowledgments

- OpenCV community for excellent documentation
- Background subtraction algorithms research
- Computer vision tutorials and resources

⭐ Star this repo if you find it helpful!

</div>
