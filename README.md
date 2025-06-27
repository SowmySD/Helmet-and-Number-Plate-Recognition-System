# 🚦 Helmet and Number Plate Detection using YOLO and OCR

This Streamlit-based project detects **motorbike riders**, **helmet usage**, and **vehicle number plates** in real-time using the **YOLOv8 object detection model** and **PaddleOCR** for optical character recognition.

## 🔍 Features

-  Helmet detection (with and without)
-  Rider identification
- ✅ Number plate detection and OCR
- ✅ Support for:
  - Image upload
  - Video upload
  - Real-time webcam feed
- ✅ Similarity filtering and confidence-based number plate recognition
- ✅ Downloadable list of detected number plates

## 🧠 Tech Stack

- **Frontend**: [Streamlit](https://streamlit.io/)
- **Object Detection**: [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- **OCR**: [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR)
- **Computer Vision**: OpenCV, cvzone
- **Language**: Python


## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/helmet-number-plate-detection.git
cd helmet-number-plate-detection
```
### 2. Install dependencies

```bash
pip install -r requirements.txt
```
3. Run the application

```bash
streamlit run app.py
```
## 🛠 How it Works

1. The uploaded image, video, or webcam frame is passed through a YOLOv8 model trained on:
   - `"with helmet"`
   - `"without helmet"`
   - `"rider"`
   - `"number plate"`

2. For detected `"number plate"` regions, the cropped image is passed to an OCR engine (PaddleOCR) to extract text.

3. The system filters out similar detections using:
   - String similarity (≥ 80%)
   - Confidence threshold (≥ 60%)

4. The final detected number plates are:
   - Shown on the image with bounding boxes
   - Displayed in the sidebar
   - Available for download as a `.csv` file

---

## 📸 Example Screenshots

1. Image ![Alt Text](https://github.com/SowmySD/Helmet-and-Number-Plate-Recognition-System/blob/29231368c6497df19418101fa767fb3a3ea94771/Sample%20Outputs/image.png)

2. Video ![Alt Text](https://github.com/SowmySD/Helmet-and-Number-Plate-Recognition-System/blob/29231368c6497df19418101fa767fb3a3ea94771/Sample%20Outputs/video.png)

3. Webcam ![Alt Text](https://github.com/SowmySD/Helmet-and-Number-Plate-Recognition-System/blob/29231368c6497df19418101fa767fb3a3ea94771/Sample%20Outputs/webcam.png)

