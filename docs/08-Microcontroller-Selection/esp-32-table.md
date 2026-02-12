---
title: Appendix - Controller Table for the ESP32
---

**Microcontroller Selection**

**ESP32-WROOM-32-N4**

* No SPI pins, 2 I2C pins, 2 pins for UART, and 3 pins for power and ground, totaling 7 pins

* My role in the team is to use a sensor to measure the environment around the rover, and give those measurements to the user. I plan to accomplish this with a sensor on the robot, and sending the sensor values to the web app or website, whichever is chosen to control the rover. After readings are sent, the sensors will continue to monitor the environment and change the outputs accordingly.


| ESP Info                                    | Answer                                                                                                                                                                                                                                                                                                        | Help                                                     |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| **Model**                                   | ESP32-S3-WROOM-1-N4                                                                                                                                                                                                                                                                                           | Include entire part number (omit package suffix letters) |
| **Product Page URL**                        | [ESP32-S3-WROOM-1 Product Page](https://www.espressif.com/en/products/modules/esp32-s3-wroom-1)                                                                                                                                                                                                               | Found on Espressif.com                                   |
| **ESP32-S3-WROOM-1 Datasheet URL**          | [ESP32-S3-WROOM-1 Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-s3-wroom-1_wroom-1u_datasheet_en.pdf)                                                                                                                                                                          | Module datasheet                                         |
| **ESP32-S3 Datasheet URL**                  | [ESP32-S3 Series Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-s3_datasheet_en.pdf)                                                                                                                                                                                            | SoC details                                              |
| **ESP32-S3 Technical Reference Manual URL** | [ESP32-S3 TRM](https://www.espressif.com/sites/default/files/documentation/esp32-s3_technical_reference_manual_en.pdf)                                                                                                                                                                                        | I/O muxing, USB, etc.                                    |
| **Vendor Link**                             | [DigiKey Product Page](https://www.digikey.com/en/products/detail/espressif-systems/ESP32-S3-WROOM-1-N4/16162639)                                                                                                                                                                                             | Vendor purchase link                                     |
| **Code Examples**                           | [ESP-IDF WiFi Example](https://github.com/espressif/esp-idf/tree/master/examples/wifi/getting_started/station) <br> [ESP-IDF I2C Example](https://github.com/espressif/esp-idf/tree/master/examples/peripherals/i2c) <br> [SHTC3 Arduino Library](https://github.com/sparkfun/SparkFun_SHTC3_Arduino_Library) | Related to Wi-Fi + I2C sensor                            |
| **External Resources**                      | [Random Nerd Tutorials ESP32-S3 Guide](https://randomnerdtutorials.com/esp32-s3-devkitc-pinout-guide/)                                                                                                                                                                                                        | Tutorials / videos                                       |
| **Unit Cost**                               | ~$5.00 (qty 1, DigiKey)                                                                                                                                                                                                                                                                                       | Vendor pricing                                           |
| **Absolute Maximum Current (entire IC)**    | 1500 mA cumulative IO output (absolute max rating)                                                                                                                                                                                                                                                            | From datasheet                                           |
| **Supply Voltage Range**                    | Recommended: 3.0 – 3.6 V (3.3 V nominal) <br> Absolute Max: −0.3 V to 3.6 V                                                                                                                                                                                                                                   | From datasheet                                           |
| **Maximum GPIO Current (per pin)**          | ~40 mA source, ~28 mA sink (typical test conditions)                                                                                                                                                                                                                                                          | From datasheet                                           |
| **Supports External Interrupts?**           | Yes                                                                                                                                                                                                                                                                                                           | GPIO interrupt capable                                   |
| **Required Programming Hardware**           | None required (built-in USB Serial/JTAG)                                                                                                                                                                                                                                                                      | USB flash/debug                                          |


| Module                | # Available                 | Needed | Associated Pins (or * for any) |
| --------------------- | --------------------------- | ------ | ------------------------------ |
| **UART**              | 3                           | 1      | * (GPIO matrix routable)       |
| **External SPI***     | 2                           | 0      | *                              |
| **I2C**               | 2                           | 1      | SDA/SCL = *                    |
| **GPIO**              | 45                          | 0      | *                              |
| **ADC**               | 2 units (20 channels total) | 0      | Analog-capable GPIOs           |
| **LED PWM (LEDC)**    | 8 channels                  | 0      | *                              |
| **Motor PWM (MCPWM)** | 2 peripherals               | 0      | *                              |
| **USB Programmer**    | 1                           | 1      | GPIO19 (D−), GPIO20 (D+)       |


MCC does not have a layout for the ESP, however, by looking at the pin diagram, there should be more than enough pins to accommodate the requirements. The chip contains 38 pins, and although some are reserved for specific purposes, there are more than enough pins for the 7 needed connections.

I have decided to go with the ESP32-WROOM-32-N4. It is a surface mount version of the ESP32 chip I am already familiar with. Initially, the ESP32-S2 was considered, however, the component had the QFN package, disqualifying it for this project. The ESP32 in general is also necessary over the PIC, as I need to be able to access a wireless connection to display the measurements to the user, and the ESP32 is superior to the PIC for that purpose. 
