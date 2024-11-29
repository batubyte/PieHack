# PieHack

---

## Overview
PieHack is a collection of hardware and software tools for experimenting with and learning about hacking using Raspberry Pi Pico. The Pico, with its small form factor and various models, offers numerous possibilities for DIY hacking projects. This guide provides a hardware setup, software installation instructions, and a list of hacking ideas to explore.

---

## Hardware

### 1. Raspberry Pi Pico Models

- **[Raspberry Pi Pico W](https://www.waveshare.com/product/raspberry-pi/boards-kits/raspberry-pi-pico-cat/raspberry-pi-pico-w.htm?sku=23108)**  
  Includes built-in Wi-Fi, ideal for wireless hacking projects.

- **[Raspberry Pi Pico 2W](https://www.waveshare.com/product/raspberry-pi/boards-kits/raspberry-pi-pico-3/raspberry-pi-pico-2-w.htm?sku=29439)**  
  A newer version with Bluetooth and enhanced power capabilities.

### 2. USB Cables & Adapters

- **[USB Cable (A to Micro USB)](https://www.raspberrypi.com/products/usb-a-male-to-micro-usb-male-cable/)**  
  Required to connect your Pico to your computer.

- **[USB Adapter (B to USB-C)](https://www.raspberrypi.com/products/usb-b-to-usb-c-adapter/)**  
  For connecting to USB-C ports, if that's your preferred setup.

### 3. Power Source (Optional)

- **[Anker PowerCore 5000 Powerbank](https://www.amazon.com/Anker-Powercore-5000-mAh-Powerbank-A1109G11/dp/B01CU1EC6Y)**  
  Use this powerbank to power your Pico without needing a computer connection. Supports 1.8V to 5.5V input (3.3V recommended for Pico).

---

## Installation

### 1. Set Up Your Raspberry Pi Pico

To get started with your Raspberry Pi Pico, follow these steps:

1. **Download the firmware** for either **MicroPython** or **CircuitPython**:
   - [MicroPython](https://micropython.org/download/rp2-pico/)
   - [CircuitPython](https://circuitpython.org/board/raspberry_pi_pico/)

2. **Plug in the Pico** to your computer using the USB cable or adapter.

3. **Install an IDE** for coding:
   - **Thonny IDE**: Recommended for beginners using MicroPython.
   - **Visual Studio Code**: For advanced users, particularly for larger projects and extensions.

---

## Hacking Ideas

### 1. **USB Rubber Ducky (HID Attack)**
   - Use the Pico as a *HID (Human Interface Device)* that emulates a keyboard, automatically typing commands when plugged in.

### 2. **Wi-Fi Deauthentication**
   - Disrupt Wi-Fi connections by sending deauthentication packets (additional hardware like an ESP32 may be required).

### 3. **Bluetooth Hacking**
   - Pair your Pico with a Bluetooth module to sniff Bluetooth traffic or test the security of Bluetooth devices.

### 4. **Keylogger**
   - Create a keylogger by emulating a USB keyboard and recording keystrokes.

### 5. **Home Automation**
   - Control smart home devices or create your own home automation system using the Pico.

### 6. **Password Cracker**
   - Implement brute-force attacks to crack simple passwords (use responsibly and ethically).

### 7. **Reverse Engineer USB Devices**
   - Capture and analyze data from USB devices to learn how they communicate and work.

### 8. **Network Sniffer**
   - Use the Pico (with Wi-Fi or Ethernet module) to capture and analyze network traffic.

### 9. **JTAG Debugger**
   - Use the Pico as a debugger for other microcontrollers through JTAG, helping with hardware reverse engineering.

### 10. **Physical Security Hacking**
   - Use the Pico to test physical security systems such as RFID locks, alarm systems, or access control devices.

---

## Additional Hardware for Prototyping

- **[Raspberry Pi Pico WH](https://www.raspberrypi.com/products/raspberry-pi-pico/?variant=raspberry-pi-pico-wh)**  
  The Pico with pre-soldered headers, perfect for prototyping and connecting external hardware for security testing.

- **[Raspberry Pi Pico 2 WH](https://www.raspberrypi.com/products/raspberry-pi-pico-2/?variant=pico-2-wh)**  
  The new version with pre-soldered headers, enhanced performance, and Bluetooth support, ideal for advanced hacking projects.

---

## Ethical Considerations

While experimenting and learning with PieHack, it’s crucial to always follow ethical guidelines:

- **Obtain permission** before attempting any hacking activity.
- Unauthorized hacking is illegal and unethical.
- Respect privacy and always conduct security research in a legal, responsible manner.

---

Happy hacking! 🚀
