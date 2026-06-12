# esp32-cam

## Introduction

This project contains example Arduino code for the ESP32-CAM module commonly found on AliExpress:

<img width="404" height="423" alt="image" src="https://github.com/user-attachments/assets/028b4bd5-a822-4c55-abcf-b83069e8e265" />

The code is heavily based on the ESP32 Arduino library (Espressif Systems) examples, but has been reviewed and refactored to be simpler.

>  **Important:** Use **esp32 version 1.0.6 for Arduino IDE** — newer versions may be unstable and not work correctly with this module. Mentioned version of library is also preserved in this repository.

<img width="437" height="201" alt="image" src="https://github.com/user-attachments/assets/525289f4-92b1-4771-acbe-27bddb6c2c50" />

[Library repository](https://github.com/espressif/arduino-esp32)

**To run it, simply add your Wifi SSID and password in the .ino file, upload to code into your ESP32-CAM board with Arduino IDE, and then access the camera using IP address shown in your router setting or in the Serial monitor.**

Example photo with default settings, taken at night with the Flashlight enabled:

<img width="640" height="481" alt="image" src="https://github.com/user-attachments/assets/22d17db7-a90a-4929-9ff7-d18ae4d00c9f" />

---

##  Software Modifications

- To improve reliability, a simple optional workaround has been added: The ESP32 automatically restarts every **5 minutes**, which helps recover from potential Wi-Fi disconnections. You can comment out lines 128 and 129 in the `esp32-cam.ino` file to disable this feature.
- LED functionality has been added and simplified - it's no longer PWM dimming, just a simple ON/OFF toggle.
- Default parameters such as resolution and gain celling have been adjusted to higher higher values.

---

##  Hardware Modifications

If you're using a motherboard like this:

<img width="284" height="222" alt="image" src="https://github.com/user-attachments/assets/f45172e2-2655-4d10-8415-8ca7214cd198" />

It is recommended to **cut the trace for GPIO0 after uploading the firmware**.  
Otherwise, the board may require pressing the **RST** button every time to boot.

---

##  Misc

- The code is fully working and tested.
- If you're unable to get an image from the camera, it's possible that the **OV2640 sensor is faulty** — this is a common issue with cheap modules.

---

