# Sbarra di parcheggio con PIN IR e sensore di distanza

Prototipo di **sbarra per parcheggio** che si apre inserendo un **PIN** da telecomando **IR** e
usa un **sensore a ultrasuoni (HC-SR04)** per rilevare se l'unico posto è **occupato** o **libero**.
Include (opzionale) invio dati a **ThingSpeak**.

![Schema logico](docs/Sistema_di_parcheggio_IoT.pdf)

## Funzionalità
- Sblocco con **PIN** (predefinito `1111`) letto da telecomando IR
- Controllo **motore stepper** (28BYJ-48 + ULN2003) per alzare/abbassare la sbarra
- Rilevazione **occupato/libero** tramite distanza (soglia configurabile)
- LED stato posto (acceso = occupato)
- **Auto-chiusura** dopo n secondi o quando rileva un'auto
- (Opzionale) invio a **ThingSpeak**

## File principali
- `progetto3.ino` – sketch Arduino (codice principale)
- `docs/Sistema_di_parcheggio_IoT.pdf` – presentazione
- `requirements.md` – librerie/hardware richiesti
- `.gitignore` – esclusioni consigliate
- `LICENSE` – licenza MIT (puoi cambiarla)

## Requisiti rapidi
Vedi **[requirements.md](requirements.md)** per dettagli su librerie e hardware.

## Pinout di default
- **IR**: pin 7
- **HC-SR04**: TRIG 9, ECHO 10
- **LED**: pin 2
- **Stepper**: A5, A3, A4, A2 (ULN2003)

## Come usare
1. Apri `progetto3.ino` con **Arduino IDE**
2. Installa le librerie elencate in `requirements.md`
3. Scegli la **Scheda** corretta (Arduino UNO *oppure* ESP32/ESP8266 se usi WiFi)
4. Se vuoi ThingSpeak, inserisci **SSID/password** e **API key** nel codice dove indicato
5. Carica lo sketch sulla board

## Struttura repository
```
parking-gate-arduino/
├─ progetto3.ino
├─ requirements.md
├─ LICENSE
├─ .gitignore
└─ docs/
   └─ Sistema_di_parcheggio_IoT.pdf
```

## Licenza
Rilasciato sotto **MIT**. Sostituisci `YOUR NAME` in `LICENSE` con il tuo nome.

## Nota
Questo progetto nasce come prototipo didattico: regola soglie/passaggi motore in base alla tua meccanica.
