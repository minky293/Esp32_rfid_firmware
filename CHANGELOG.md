# Changelog

All notable changes to this project will be documented in this file.

## [1.0.0] - 2026-10-15
### Added
- Initial release of the ESP32 RFID MQTT authentication system.
- Integration with MFRC522 RFID reader using SPI communication (SS=5, RST=22, SCK=18, MOSI=23, MISO=19).
- Wi-Fi station mode connection and secure MAC address initialization post-connection to fix the `000000000000` MAC issue.
- MQTT publishing functionality to broker `broker.freemqtt.com:1883` using JSON payloads (`{"uid":"..."}`).
- Project documentation in `docs/Index.md` and example configurations.