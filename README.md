# HART(Helping Assistant Robotic Tracker)
# 🤖 Human-Following Robot using ESP32

As society ages, robotic helpers that follow and assist users are gaining interest. This report presents a conceptual design for a portable, person-following robot (“helper car”) using an ESP32 microcontroller ,  an L298N motor driver, and a smartphone with pedometer and orientation sensors. The smartphone app (created with MIT App Inventor) tracks the user’s movement and sends commands via Bluetooth  to the ESP32. The ESP32 processes Bluetooth data  to navigate and carry small objects. Key features include Bluetooth-based following,  load-carrying capability, and user-friendly interface. Emphasis is on a lightweight, battery-powered design for maximum portability. The architecture, interface, and implementation strategies are detailed, along with testing plans and discussion of performance trade-offs.
Smartphone Sensors (Pedometer & Orientation): Modern smartphones include inertial sensors (accelerometer, gyroscope, magnetometer) enabling step counting (pedometer) and heading/orientation detection. An app can use these sensors to estimate the user’s movement vector (distance and direction) without GPS. By integrating step count and compass bearing, the smartphone app can infer how far and in what direction the user has moved. These estimates are sent to the robot via Bluetooth  allowing the robot to “know” where the user is heading relative to itself.
---

## 🧠 Features

•	Portability: The system should be lightweight and powered by a portable battery (e.g. power bank or Li-ion pack). The design should minimize size and weight to be easily movable by one person.
•	Power efficiency: Components (ESP32, motors, sensors) should be chosen for low power usage to allow at least 5 hours of continuous operation on a single charge.
•	Safety: The robot must operate safely around humans. It should have a clearly safe stopping behavior on obstacles. Sharp edges or pinch points should be minimized. The speed should be moderate to avoid injury (e.g. ≤ 1 m/s).
•	User interface: The smartphone app should be intuitive. For example, it may use simple buttons or voice commands to initiate follow mode. Feedback (like connection status, battery level) should be shown.
•	Robustness: The system should handle common environmental variations . Bluetooth link should be maintained up to a reasonable range (e.g. 10 m).

---

## 🔧 Hardware Used
●	A stable internet connection (2Mbps or higher)
●	ESP32 Board
●	Motors and wheels
●	Motor Driver
●	Smartphone
●	Wires
●	Power supply

---

## 📱 Software Stack

| Platform        | Purpose                             |
|----------------|--------------------------------------|
| Arduino IDE     | Programming the ESP32               |
| Android BLE/Wi-Fi app | Sends control signals to ESP32 |

---
## Circuit Diagram
<img width="1090" height="708" alt="image" src="https://github.com/user-attachments/assets/6130eb75-cab2-424b-946f-d496f27d2b91" />
---

## MIT App Inventor Block Code
<img width="1090" height="667" alt="image" src="https://github.com/user-attachments/assets/f3ce0c1a-3152-46e0-bfa7-cb12b698ce3b" />



## 📲 Control Methods

- 🔵 *Bluetooth*: For manual  control from phone and human following
- 🔊 *Voice Commands*: Recognized on phone using offline ML

---
## Screenshots
<img width="564" height="564" alt="image" src="https://github.com/user-attachments/assets/e286013a-2314-435e-9f21-d66a04296f80" />
<img width="565" height="565" alt="image" src="https://github.com/user-attachments/assets/d76c72d1-deac-45c5-b046-be2aba274bac" />





## 📥 Download Project Files

- 📄 Download Arduino Code: [`ArduinoCode.ino`]
## 📱 Download the Android App

You can install the Android app used to control the robot:

- 📦 [Download APK](./Esp32_Compass.apk)

> ⚠️ Note: This is a pre-built APK file for installation only. The source code for the app was built using MIT App Inventor but is not included in this repository.


