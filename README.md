# HART(Helping Assistant Robotic Tracker)
# 🤖 Human-Following Robot using ESP32

A smart, low-cost robot that follows a human using a combination of sensors and AI. Built around the ESP32, this project uses an ultrasonic sensor mounted on a servo for directional scanning, voice or image recognition on a smartphone, and Bluetooth/Wi-Fi-based communication with the robot.


---

## 🧠 Features

- 🧍 Detects and follows humans using ultrasonic scanning
- 🎤 Accepts voice commands processed on smartphone
- 📷 Optional person detection using smartphone camera + TensorFlow Lite
- 📡 Communicates over *Bluetooth* or *Wi-Fi*
- 🧭 Azimuth-based directional turning with angle wrap-around support
- 🚧 Basic obstacle detection and avoidance
- ⚙ PID control for smooth motion

---

## 🔧 Hardware Used

- 🔲 *ESP32 (e.g., NodeMCU or ESP32-C3)*
- 🔋 4 × 3.7V Li-ion batteries
- 🔀 *L298N Motor Driver*
- 🎛 *Servo Motor* (for ultrasonic scanning)
- 👁 *HC-SR04 Ultrasonic Sensor*
- 🔦 *IR Sensors / LDRs* (for basic line/light sensing)
- 🔊 Buzzer for alerts
- 📱 Smartphone (for AI + voice control interface)

---

## 📱 Software Stack

| Platform        | Purpose                             |
|----------------|--------------------------------------|
| Arduino IDE     | Programming the ESP32               |
| Android BLE/Wi-Fi app | Sends control signals to ESP32 |

---

## 🔌 Wiring Overview

- ESP32 PWM → Servo
- ESP32 GPIO → Ultrasonic Trigger/Echo
- ESP32 GPIOs → L298N IN1/IN2/IN3/IN4
- ESP32 TX/RX → Bluetooth (optional)
- ESP32 I2C/SPI → Additional sensors (if used)

> 📐 The servo rotates left/right (e.g., -90° to +90°) to scan for human presence. Based on distance < 30 cm, robot turns toward that direction and follows.

---

## 📲 Control Methods

- 🔵 *Bluetooth*: For manual or AI-based control from phone
- 📡 *Wi-Fi WebSocket*: For real-time azimuth data or camera tracking
- 🔊 *Voice Commands*: Recognized on phone using offline ML
- 🧍 *Person Detection*: Uses TensorFlow Lite model on mobile, classification result sent to ESP32

---



## 📥 Download Project Files

- 📄 Download Arduino Code: [`ArduinoCode.ino`]
## 📱 Download the Android App

You can install the Android app used to control the robot:

- 📦 [Download APK](./Esp32_Compass.apk)

> ⚠️ Note: This is a pre-built APK file for installation only. The source code for the app was built using MIT App Inventor but is not included in this repository.


