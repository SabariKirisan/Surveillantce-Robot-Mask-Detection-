# 🛡️ Face Mask Detection with OpenCV and TensorFlow

This project uses a pre-trained deep learning model to detect whether a person is wearing a face mask in real-time via webcam. It combines OpenCV’s face detection with a MobileNetV2-based Keras model for mask classification.

---

## 🚀 Features

- Real-time face detection using OpenCV’s DNN module
- Mask classification using a MobileNetV2-based model
- Live webcam feed with bounding boxes and labels
- Lightweight and easy to run locally

---

## 📡 ESP32-CAM Integration with TCP/IP

The project also uses an ESP32-CAM board to transmit live video over Wi-Fi and remotely control a surveillance robot.

- The ESP32 connects to a Wi-Fi network using the WiFi.begin() function.
- It starts a web server (startCameraServer()), which runs on top of the TCP/IP protocol stack.
- A live MJPEG video stream and robot movement commands (forward, backward, left, right) are transmitted via HTTP requests over TCP.
- This demonstrates a practical use of TCP/IP for real-time communication between a web browser and an IoT device.

## 🧠 Model Overview

The project uses:

- **Face Detection**: OpenCV's DNN module with the `res10_300x300_ssd_iter_140000.caffemodel`
- **Mask Detection**: A custom-trained MobileNetV2 model saved as `mask_detector.h5`

---

## 📁 Project Structure

    face-mask-detector/
       - face_detector/
          - deploy.prototxt
          - res10_300x300_ssd_iter_140000.caffemodel
    mask_detector.h5
    detect_mask_video.py
    requirements.txt

---

## 🖥️ Usage
To run the real-time mask detection via your webcam:

    python detect_mask_video.py

---

## 📝 Requirements
- opencv-python
- imutils
- tensorflow
- numpy

---

## 📊 Output 
When running the script, you'll see your webcam feed with faces labeled as:

✅ Mask: 98.74% — shown in green

❌ No Mask: 99.11% — shown in red

