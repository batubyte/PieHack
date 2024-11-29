![](https://www.waveshare.com/media/catalog/product/cache/1/image/560x560/9df78eab33525d08d6e5fb8d27136e95/r/a/raspberry-pi-pico-2-w-1.jpg)

The **Raspberry Pi Pico** can be transformed into a "Bad USB" device. A "Bad USB" is essentially a USB device that acts like a keyboard to execute commands or scripts automatically when plugged into a computer. This is often done for ethical hacking, penetration testing, or education on security practices.

However, unlike traditional USB devices (e.g., the Raspberry Pi Zero), the Pico 2W is not a true USB host. It leverages USB emulation via its firmware. Below is how you can set up your Raspberry Pi Pico to act as a "Bad USB."

---

### Prerequisites
1. **Hardware:**
   - [Raspberry Pi Pico 2W](https://www.waveshare.com/product/raspberry-pi/boards-kits/raspberry-pi-pico-3/raspberry-pi-pico-2-w.htm?sku=29439)
   - Micro USB cable for power and data

2. **Software:**
   - MicroPython or CircuitPython installed on the Pico 2W.
   - Libraries to emulate HID (Human Interface Device).
   - A script to define the payload.

---

### Steps to Turn Pico 2W into a Bad USB

#### 1. **Install CircuitPython**
   - Download CircuitPython for the Raspberry Pi Pico 2W from the [CircuitPython website](https://circuitpython.org/board/raspberry_pi_pico/).
   - Hold the BOOTSEL button on the Pico and connect it to your computer via USB.
   - Drag and drop the `.uf2` file for CircuitPython onto the RPI-RP2 drive.

#### 2. **Set Up HID Functionality**
   CircuitPython includes built-in libraries for USB HID devices like keyboards or mice. To enable HID:
   - Copy the `adafruit_hid` library folder to the `lib` folder on your Pico.
     You can download it from the [Adafruit CircuitPython Bundle](https://github.com/adafruit/Adafruit_CircuitPython_Bundle).

#### 3. **Create a Payload Script**
   Here’s an example Python script to emulate a keystroke payload:

   ```python
   import usb_hid
   from adafruit_hid.keyboard import Keyboard
   from adafruit_hid.keycode import Keycode
   from adafruit_hid.keyboard_layout_us import KeyboardLayoutUS

   # Initialize HID Keyboard
   keyboard = Keyboard(usb_hid.devices)
   layout = KeyboardLayoutUS(keyboard)

   # Start the payload
   keyboard.press(Keycode.GUI, Keycode.R)  # Win+R
   keyboard.release_all()
   layout.write("notepad\n")
   keyboard.release_all()
   ```

   This script opens the Run dialog, launches Notepad, and can be extended to write additional payloads.

#### 4. **Deploy the Script**
   - Save the Python script as `code.py` on the Pico.
   - Once saved, the Pico will automatically execute the payload when connected to a target machine.

#### 5. **Testing**
   - Plug the Pico into a computer and monitor its behavior.
   - Ensure that the HID functionality works as expected.

---

### Ethical Considerations
Using a device as a Bad USB must be done ethically:
- Only test on systems you own or have permission to test.
- Do not use this for unauthorized access or harm.

This approach is suitable for learning about security vulnerabilities and testing defenses.
