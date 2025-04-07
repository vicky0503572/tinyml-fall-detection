# tinyml-fall-detection

A real-time fall detection system using an *ESP32* and *MPU6050 accelerometer*, powered by a lightweight machine learning model trained with *Edge Impulse* and deployed using *TensorFlow Lite for Microcontrollers*.

-----

## Project Goal

Build a compact, low-power system that can detect *human falls* based on motion patterns, suitable for wearable health monitoring devices (especially for elder care).

-----

## Features

- Real-time motion classification: *walking*, *standing*, *falling*
- Deployed ML model runs fully *on-device* (no cloud)
- Uses *MPU6050* accelerometer + gyroscope
- Optional alert via *LED / OLED / Wi-fi notification*
- Build with *Edge Impulse* + Arduino framework

-----

## Hardware Used

| Component      | Description                            |
|----------------|----------------------------------------|
| ESP32 Dev Board| Main microcontroller (ML inference)    |
| MPU6050        | Accelerometer & Gyroscope (I2C)        |
| Breadboard     | For prototyping                        |
| Jumper Wires   | Connections                            |
| (Optional) OLED| Display classification result          |
| (Optional) Battery | 18650 Li-ion for mobile testing    |

-----

## 🧠 Machine Learning Pipeline

| Stage           | Tool/Method        |
|---------------  |--------------------|
| Data Collection | Edge Impulse Studio (mobile or serial) |
| Preprocessing   | Spectral features / statistical features |
| Model Type      | Decision Tree / KNN / or Neural Net |
| Deployment      | Quantized `.tflite` → C++ Arduino Library |
| Runtime         | TensorFlow Lite Micro + Arduino IDE |

-----

## 📁 Folder Structure

```bash
tinyml-fall-detection/
├── model/                # Trained model files
├── src/                  # Arduino sketch & model headers
│   ├── main.ino
│   └── model.h
├── data/                 # Optional: sample raw sensor CSV
├── images/               # Screenshots, circuit photos
├── README.md
└── LICENSE
