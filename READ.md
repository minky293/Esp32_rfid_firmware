# 🏷️ ESP32 RFID MQTT Authentication Project
![Esp32 RFID mqtt](images/connection-icon.jpg.jpg)
![License](https://img.shields.io/badge/license-MIT-blue)

A project involves creating a device that uses an ESP32 microcontroller to read RFID tags and publish data via MQTT, allowing for wireless identification and authentication.

---

## 📑 Table of Contents
- [Introduction](#introduction)
- [Getting Started](#getting-started)
- [Bill of Material](#bill-of-material)
- [Hardware Schematic](#hardware-schematic)
- [Software Concept](#software-concept)

---

## 🧐 Introduction

The project includes source code for an RFID Reader with the following requirements:

### 📝 Functional requirement
- **Read RFID Card:** The ESP32 must be able to read data from RFID cards using an attached MFRC522 RFID reader module, capturing the unique identifier (UID).
- **MQTT Publishing:** Upon successfully reading an RFID card, the ESP32 publishes the UID as a JSON payload (`{"uid":"..."}`) to an MQTT broker.

### 📄 Non-functional requirement
- **Wi-Fi Connectivity:** Stable connection using Wi-Fi station mode with secure MAC address initialization post-connection.

---

## 🏁 Getting Started

### Hardware Requirements:
1. RFID CARDS / Keyfobs
2. ESP32 Development Board
3. Programming Cable (Micro-USB / Type-C)
4. RFID-RC522 Module
5. Jumper Wires

---

## 🛠️ Bill of Material

- **[Arduino IDE](https://www.arduino.cc/):** For programming the device.
- **ESP32 Microcontroller** x1
- **RFID-RC522 Module** x1

---

## 📖 Hardware Schematic / Wiring Diagram
![System Archi](images/setup.jpg.jpg)

| MFRC522 Pin | ESP32 GPIO Pin |
| :--- | :--- |
| SDA (SS) | GPIO 5 |
| SCK | GPIO 18 |
| MOSI | GPIO 23 |
| MISO | GPIO 19 |
| RST | GPIO 22 |
| GND | GND |
| 3.3V | 3.3V |

---
![Successful Connection on MQTT](image/mqtt-connectjpg.png)
## 💻 Software Concept

The project utilizes the ESP32's SPI interface to communicate with the MFRC522 module:
- **GPIO 5 (SS):** Enables the ESP32 to select the RFID module.
- **GPIO 22 (RST):** Connected to the RST pin to reset the RFID module.