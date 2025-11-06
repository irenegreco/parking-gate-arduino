# Requirements (Libraries & Hardware)

This project is an **Arduino sketch**; it does not use a Python-style `requirements.txt`.
Install the following libraries via **Arduino IDE → Library Manager**:

- **Stepper** (built-in in the classic Arduino IDE; or the Arduino `Stepper` library)
- **IRremote** (project: *Arduino-IRremote/IRremote*). Recommended version: 4.x
- **WiFi** (included on **ESP32/ESP8266**; on Arduino UNO you need a WiFi shield if you plan to use WiFi)
- **ThingSpeak** (by MathWorks) – *optional*

## Expected Hardware
- **28BYJ-48 stepper** + **ULN2003** driver
- **IR receiver** (e.g., TSOP38238) on pin 7
- **HC-SR04** ultrasonic sensor on TRIG 9, ECHO 10
- **LED** on pin 2
- Board: Arduino UNO **or** ESP32/ESP8266 (if you use WiFi/ThingSpeak)

> For ESP32/ESP8266, install the board support first in **Tools → Board → Boards Manager**.
