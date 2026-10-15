# Esp32, RFID and Mqtt authetication project

## Overview
This project implements an RFID-based authtication system using a esp32 controller and MFRC522 rfid reader.
It connect to a wifi network and publish rfid uid as json paylod to mqtt broker.

## Hardware Components
-Esp32 devkit development board
-RFID reder card
-jumper wires

## Wiring diagram
| MFRC522  |  Esp32 gpio pin  |
|----------|------------------|
| SDA(ss)  | gpio-05          |
| SCk      | gpio-18          |
| Mosi     | gpio-23    |     |
| Miso     | gpio-19          |
| Rst      | gpio-22          |
| GND      | GND              |
| 3.3 v    | 3.3v             |

## MQTT COnfig 
- **Broker:** broker.freemqtt.com
- **Port:** 1883
- **Topic Format:** 'demo/rfid/000000000000/uid'
- **Payload Format:** '{"uid":"<CARD_UID>"}'