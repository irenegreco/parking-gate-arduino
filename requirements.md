# Requisiti (librerie e piattaforma)

Questo progetto è uno sketch **Arduino**; non usa `requirements.txt` (tipico di Python).
Installa le seguenti librerie tramite **Arduino IDE > Gestione librerie**:

- **Stepper** (built-in su IDE classico; in alternativa `Stepper` di Arduino)
- **IRremote** (autore *Arduino-IRremote/IRremote*). Versione consigliata: 4.x
- **WiFi** (inclusa su **ESP32/ESP8266**; su Arduino UNO non è disponibile a meno di shield specifici)
- **ThingSpeak** (MathWorks) – *opzionale*

## Hardware previsto
- Motore **stepper 28BYJ-48** + driver **ULN2003**
- Ricevitore **IR** (es. TSOP38238) sul pin 7
- Sensore **HC-SR04** su TRIG 9, ECHO 10
- **LED** sul pin 2
- Board: Arduino UNO **oppure** ESP32/ESP8266 (se usi WiFi/ThingSpeak)

> Per l'ESP32/ESP8266 installa prima il supporto scheda in **Strumenti > Scheda > Gestore schede**.
