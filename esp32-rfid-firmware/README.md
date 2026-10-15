<p align="center">
  <img src="https://raw.githubusercontent.com/minky293/Esp32_rfid_firmware/main/images/conntion-icon.jpg" alt="Connection Icon" width="600"/>
</p>

# 🏷️ ESP32 RFID MQTT Authentication Project

[![status](https://img.shields.io/badge/status-active-success.svg)]()
[![pull requests](https://img.shields.io/badge/pull%20requests-0%20open-blue.svg)]()
[![license](https://img.shields.io/badge/license-MIT-green.svg)]()

---

## 📖 Introduction
A project involves creating a device that uses an ESP32 microcontroller to read RFID tags, allowing for wireless identification and access control applications via MQTT.

## 📋 Table of Contents
* [Introduction](#-introduction)
* [Getting Started](#-getting-started)
* [Bill of Material](#-bill-of-material)
* [Hardware Schematic / Wiring Diagram](#-hardware-schematic--wiring-diagram)
* [Software & Firmware Setup](#-software--firmware-setup)

---

## 🚀 Getting Started
To get started with this project, clone the repository and open it in your preferred IDE (such as Arduino IDE or VS Code with PlatformIO).

---

## 🛠️ Bill of Material
* **[Arduino IDE](https://www.arduino.cc/):** For programming the device.
* **ESP32 Microcontroller:** x1
* **RFID-RC522 Module:** x1

---

## 📦 Hardware Schematic / Wiring Diagram

<p align="center">
  <img src="https://raw.githubusercontent.com/minky293/Esp32_rfid_firmware/main/images/setup.jpg" alt="Hardware Setup" width="600"/>
</p>

| MFRC522 Pin | ESP32 GPIO Pin |
| :--- | :--- |
| SDA (SS) | GPIO 5 |
| SCK | GPIO 18 |
| MOSI | GPIO 23 |
| MISO | GPIO 19 |

<p align="center">
  <img src="https://raw.githubusercontent.com/minky293/Esp32_rfid_firmware/main/images/mqtt-connect.png" alt="MQTT Connection" width="600"/>
</p>

---

## 💻 Software & Firmware Setup
Ensure you configure your Wi-Fi credentials and MQTT broker details inside the firmware files before uploading to the ESP32 board.