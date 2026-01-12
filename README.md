# LED Status Bar for 3D Printers (ESP32 + Home Assistant)

This project is a simple **LED status bar** used to monitor the status of one or more 3D printers using **Home Assistant**.

It’s based on:
- ESP32
- WS2812 / addressable LEDs (30 LEDs/m)
- ESPHome
- Home Assistant

The printed enclosure is shared on MakerWorld.  
This repository contains the **ESPHome configuration** and **example Home Assistant automations**.

---

## How it works

Each LED (or group of LEDs) represents a printer.

Home Assistant controls the LEDs via ESPHome to show different states, for example:
- idle
- printing
- finished
- error

All logic is handled in software.

---

## ESPHome configuration
What it does:
- defines one or more LED strips
- splits the main strip into multiple **partitions**
- each partition is exposed as a separate light entity in Home Assistant

You can customize:
- number of LEDs
- GPIO pins

---

## Home Assistant automations

This repository includes **example automations** for:

- Moonraker / Klipper printers  
- BambuLab printers  

These automations are provided as **examples**.

To use them, you only need to:
- change the ESPHome **light entity IDs**
- change the **printer status entity IDs** to match your setup

No other logic changes are required.

---

## Notes

- Designed for **30 LEDs/m addressable LED strips**
- ESP32 + ESPHome
- Simple and easily adaptable setup

This project is shared as-is as a base for custom printer monitoring setups
The ESPHome configuration is located here:

