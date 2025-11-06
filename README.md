# Parking Gate with IR PIN and Distance Sensor

Prototype of a **parking gate** that opens when a **PIN** is entered from an **IR remote**, and uses an
**ultrasonic sensor (HC-SR04)** to detect whether the single parking spot is **occupied** or **free**.
(Optional) data upload to **ThingSpeak**.

> **Collaboration note:** this project was created together with **Ilaria Ballerini** (as shown on the first slide of the included PDF).

## Features
- Unlock with **PIN** (default `1111`) read from an IR remote
- **Stepper motor** control (28BYJ-48 + ULN2003) to open/close the barrier
- **Occupied/free** detection via distance (configurable threshold)
- Status **LED** (on = occupied)
- **Auto-close** after a timeout or when a car is detected
- (Optional) **ThingSpeak** data upload

## Main Files
- `parking_miniproject.ino` – Arduino sketch (left **unchanged** from your original)
- `docs/Parking_System_Presentation.pdf` – presentation
- `requirements.md` – required libraries/hardware
- `.gitignore` – recommended exclusions

## Quick Requirements
See **[requirements.md](requirements.md)** for details on libraries and hardware.

## Default Pinout
- **IR**: pin 7
- **HC-SR04**: TRIG 9, ECHO 10
- **LED**: pin 2
- **Stepper**: A5, A3, A4, A2 (ULN2003)

## How to Use
1. Open `parking_miniproject.ino` with **Arduino IDE**
2. Install the libraries listed in `requirements.md`
3. Choose the correct **Board** (Arduino UNO *or* ESP32/ESP8266 if you use WiFi)
4. If you want ThingSpeak, insert your **SSID/password** and **API key** where indicated in the code
5. Upload the sketch to the board

## Repository Structure
```
parking-gate-arduino-en/
├─ parking_miniproject.ino
├─ requirements.md
├─ .gitignore
└─ docs/
   └─ Parking_System_Presentation.pdf
```

## Note
This repository is an English-only packaging of the original project: **code unchanged**, documentation translated.
