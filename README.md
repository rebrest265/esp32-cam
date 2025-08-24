# esp32-cam

## 📷 Introduction

This project contains example code for the ESP32-CAM module commonly found on AliExpress:

![ESP32-CAM Module](https://github.com/user-attachments/assets/fd8e7177-5787-4752-88bb-a274b01d3d1b)

The code is based on the ESP32 Arduino library (Espressif Systems) examples.

> ⚠️ **Important:** Use **esp32 version 1.0.6** — newer versions may be unstable and not work correctly with this module. Mentioned version of libary is also preserved in this repository

![Library Version](https://github.com/user-attachments/assets/52dd8d03-4888-4fc4-98da-c5acba459686)

![Libary repository](https://github.com/espressif/arduino-esp32)

---

## 🔧 Software Modifications

To improve reliability, a simple workaround has been added:  
**The ESP32 automatically restarts every 5 minutes**, which helps recover from potential Wi-Fi disconnections.

---

## 🛠️ Hardware Modifications

If you're using a motherboard like this:

![Motherboard Image](https://github.com/user-attachments/assets/78268632-2c51-4234-a0d6-db0731de24a8)

It is recommended to **cut the trace for GPIO0 after uploading the firmware**.  
Otherwise, the board may require pressing the **RST** button every time to boot.

---

## 📝 Misc

- The code is fully working and tested.
- If you're unable to get an image from the camera, it's possible that the **OV2640 sensor is faulty** — this is a common issue with cheap modules.

---

