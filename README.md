# BoxRFID-Touch – Standalone RFID Tag Tool for QIDI Box

<p align="center">
  <a href="https://github.com/TinkerBarn/BoxRFID-Touch/blob/main/screenshots/Home.jpeg">
    <img src="https://raw.githubusercontent.com/TinkerBarn/BoxRFID-Touch/main/screenshots/Front.jpeg" height="320" alt="BoxRFID-Touch device">
  </a>
</p>

BoxRFID-Touch is a standalone touchscreen device for reading and writing NFC/RFID filament tags used by the **QIDI Box** ecosystem.  
It runs on an **ESP32-2432S028R CYD** together with a **PN532** RFID/NFC reader and allows you to create, read and modify tag data directly on the device — no PC required during normal use.

- **Platform:** ESP32-2432S028R CYD + PN532 (I2C)
- **Firmware:** Version 2.0
- **License:** CC BY-NC-SA 4.0

---

## 🚀 WEB INSTALLER – THE EASIEST WAY TO GET STARTED

> **No Arduino IDE. No library setup. No TFT_eSPI configuration.**
>
> BoxRFID-Touch can be installed directly from your browser in just a few clicks:
>
> ## **[➡ Open BoxRFID-Touch Web Installer](https://tinkerbarn.github.io/BoxRFID-Touch/)**

This is the **recommended installation method for most users**, especially beginners.

### What you need

- **Chrome** or **Edge**
- a supported **ESP32-2432S028R CYD**
- a **USB data cable**
- a connected **PN532** module

### Why the Web Installer is easier

The Web Installer is designed for users who do **not** want to deal with:

- Arduino IDE
- manual library installation
- ESP32 board package setup
- TFT_eSPI configuration

### Installation steps

1. Connect the ESP32 board via USB
2. Open the Web Installer
3. Click **Connect**
4. Select the correct serial port
5. Flash the firmware
6. Start using BoxRFID-Touch

### Notes

- If the board is not detected immediately, reconnect it and try again
- If needed, keep the **BOOT** button pressed while connecting
- During normal use, the device only needs a **USB power source**

---

## Features

- Read RFID tags in **manual mode**
- Read RFID tags in **auto mode**
- Write filament data to compatible tags:
  - **manufacturer**
  - **filament type**
  - **color**
- Standalone operation with only **USB power**
- Touchscreen-based user interface
- Multi-language support (**6 languages**)
- Support for customized **manufacturer lists**
- Support for customized **material lists**
- Reset custom lists back to factory defaults
- Full factory reset including **touch calibration**
- Integrated **BLE support**
- Can be used as an external RFID reader/writer via Bluetooth
- Intended for iOS companion app usage (**app currently in alpha stage**)
- Browser-based **Web Installer** for quick and easy installation
- Optional **3D-printable housing**

---

## Compatibility

Tested with:

- **QIDI Plus 4**
- **QIDI Box V1**
- **QIDI Box V2**

Possible compatibility with:

- **QIDI Q2**  
  Not tested yet. Feedback is welcome.

---

## Requirements

### Main hardware

- **ESP32-2432S028R CYD**
- **PN532 NFC/RFID module**
- **USB cable**
- **jumper wires**

### Optional

- **3D-printed enclosure**
- mounting hardware depending on enclosure design

---

## BOM

### Electronics

- **ESP32-2432S028R CYD**
  - Main controller with integrated display and touchscreen
  - [Amazon Germany ESP32-2432S028R](https://www.amazon.de/dp/B0CG2WQGP9)
  - ASIN: B0CG2WQGP9

- **PN532 NFC/RFID module**
  - Used for reading and writing compatible RFID/NFC tags
  - [Amazon Germany PN532](https://www.amazon.de/dp/B0D86CPN5J)
  - ASIN: B0D86CPN5J

- **Jumper wires**
  - Used to connect the CYD and PN532  
  - Often included with the ESP32-2432S028R board

- **USB cable**
  - Used for flashing and power supply

### Optional parts

- **3D-printed case**
  - Housing for the CYD + PN532 setup

- **Mounting material**
  - Screws, spacers, adhesive pads or similar accessories

---

## Wiring

BoxRFID-Touch uses the PN532 RFID module in **I2C mode**.  
Do not forget to switch the PN532 to **I2C mode** before use. Depending on your module version, this is usually done with the DIP switches or jumpers. See the detailed photos below.

The following pinout shows how to connect the PN532 RFID board to the ESP32-2432S028R.

### Pinout CYD ↔ PN532

- **3.3V** → **VCC**
- **GND** → **GND**
- **GPIO 21** → **SDA**
- **GPIO 22** → **SCL**

```text
ESP32-2432S028R CYD    PN532
-------------------    -----
3.3V                -> VCC
GND                 -> GND
GPIO 21             -> SDA
GPIO 22             -> SCL
