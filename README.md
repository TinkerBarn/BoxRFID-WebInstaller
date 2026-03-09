# BoxRFID

BoxRFID is a standalone RFID/NFC-based filament tag manager for the **QIDI Box** ecosystem.  
It is designed to run on an **ESP32-2432S028R CYD (Cheap Yellow Display)** together with a **PN532 NFC reader** and allows you to read, manage and write filament tag information directly on a touchscreen device.

BoxRFID is intended as an easy-to-use tool for makers who want a dedicated hardware device for working with RFID filament tags without needing a PC during normal use.

---

## What is BoxRFID?

BoxRFID is a touchscreen tool for working with RFID/NFC filament tags.

It allows you to:

- read existing RFID filament tags
- display stored tag information on the screen
- create or modify tag content
- manage spool-related data in a practical device-oriented workflow
- use a compact standalone device instead of relying only on software tools

The project is especially aimed at users working with QIDI Box related tag workflows and compatible RFID tags.

---

## Main Features

- Touchscreen-based standalone operation
- Runs on ESP32 CYD hardware
- PN532 RFID/NFC reader support via I2C
- Read RFID filament tags
- Write RFID filament tags
- Edit stored values directly on the device
- User-friendly on-screen menus
- Compact DIY hardware project
- Web Installer for easy firmware installation
- 3D printable housing available separately

---

## Supported Hardware

Currently supported:

- **ESP32-2432S028R CYD**
- **PN532 NFC/RFID module (I2C mode)**

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

## Hardware Required

## Main Components

- 1x ESP32-2432S028R CYD display board
- 1x PN532 NFC/RFID module
- 1x suitable USB cable with data support
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

### Important

Set the PN532 module to **I2C mode**.  
Depending on the PN532 board version, this may require setting DIP switches or solder bridges correctly.

Always verify the labeling on your specific PN532 module before powering it.

---

## Wiring Overview

```text
ESP32-2432S028R CYD    PN532
-------------------    -----
3.3V                -> VCC
GND                 -> GND
GPIO 21             -> SDA
GPIO 22             -> SCL
