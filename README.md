# BoxRFID

BoxRFID is a standalone RFID tag tool for creating and managing RFID filament tags for the **QIDI Box** ecosystem.

It is designed to run on an **ESP32-2432S028R CYD (Cheap Yellow Display)** together with a **PN532 NFC reader** and allows you to read and write filament tag information directly on a touchscreen device.

BoxRFID is intended as an easy-to-use hardware tool for makers who want to create RFID tags for the QIDI Box without needing a PC during normal use.

---

## What is BoxRFID?

BoxRFID is a touchscreen-based standalone device for creating and managing RFID filament tags for the **QIDI Box**.

It has been tested with:

- **QIDI Plus 4**
- **QIDI Box Version 1**
- **QIDI Box Version 2**

Compatibility with the **Q2** may be possible, but this has **not been tested yet**.  
Feedback from users is welcome.

---

## Main Features

- Create RFID tags for the **QIDI Box**
- Read tags in **manual mode**
- Read tags in **auto mode**
- Write tags with:
  - **manufacturer**
  - **filament type**
  - **color**
- Standalone operation
- Only a **USB power connection** is required during normal use
- Touchscreen-based user interface
- **6 languages supported**
- Customizable **manufacturer list**
- Customizable **material list**
- Lists can be reset to **factory defaults**
- All settings including **touch calibration** can be reset to factory settings
- Integrated **BLE support** for iOS devices
- Can be used as an external RFID reader/writer via Bluetooth
- Companion iOS app already planned/in development (**currently alpha stage**)
- Web Installer for easy firmware installation
- Optional 3D printable housing

---

## Supported Hardware

Currently supported:

- **ESP32-2432S028R CYD**
- **PN532 NFC/RFID module (I2C mode)**

---

## Printer / Ecosystem Compatibility

BoxRFID has been tested with:

- **QIDI Plus 4**
- **QIDI Box V1**
- **QIDI Box V2**

Possible compatibility:

- **QIDI Q2**  
  Not tested by the project yet. User feedback is welcome.

---

## Web Installer

You can install the firmware directly from your browser using the BoxRFID Web Installer:

**[Open Web Installer](https://YOURNAME.github.io/BoxRFID-WebInstaller/)**

Requirements:

- Chrome or Edge
- USB data cable
- Supported ESP32 board

If needed, keep the **BOOT** button pressed while connecting the board.

---

## Standalone Use

After the firmware has been installed, BoxRFID can be used as a **standalone device**.

For normal operation, only a **USB power source** is required, for example:

- USB charger
- power bank
- USB port on another device

No PC connection is required for normal tag reading or writing.

---

## Hardware Required

### Main Components

- 1x **ESP32-2432S028R CYD** display board
- 1x **PN532 NFC/RFID module**
- 1x suitable **USB cable with data support**
- jumper wires
- optional 3D printed case

---

## BOM

### Electronics

- **ESP32-2432S028R CYD**
  - Main controller with integrated touchscreen display

- **PN532 RFID/NFC module**
  - Used for reading and writing RFID/NFC tags

- **Jumper wires**
  - For connecting CYD and PN532

- **USB cable**
  - For flashing and power supply

### Optional Parts

- **3D printed enclosure**
  - Custom housing for CYD + PN532 setup

- **Mounting material**
  - Screws, spacers, adhesive pads, depending on housing design

---

## Wiring

BoxRFID uses the PN532 in **I2C mode**.

### CYD to PN532 wiring

- **3.3V** → **VCC**
- **GND** → **GND**
- **GPIO 21** → **SDA**
- **GPIO 22** → **SCL**

### Wiring Overview

```text
ESP32-2432S028R CYD    PN532
-------------------    -----
3.3V                -> VCC
GND                 -> GND
GPIO 21             -> SDA
GPIO 22             -> SCL
