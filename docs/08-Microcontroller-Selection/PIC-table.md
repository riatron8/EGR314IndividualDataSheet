---
title: Microcontroller Selection
---

**Microcontroller Selection**

**PIC18F57Q43-I/PT**

* 2 pins for I2C communication (SDA and SCL), optional UART pins for debugging/communication, and multiple power and ground pins available on the package.

* My role in the team is to use a sensor to measure the environment around the rover and provide those measurements to the user. I plan to accomplish this by connecting environmental sensors to the microcontroller using the I2C interface. The PIC will read the sensor values and send them to another controller or communication module on the rover that handles transmitting the data to the website or app used to control the rover. The sensors will continue monitoring the environment and update the measurements as conditions change.


| PIC Info | Answer | Help |
|---|---|---|
| **Model** | PIC18F57Q43 | Include entire part number (omit package suffix letters) |
| **Product Page URL** | [PIC18F57Q43 Product Page](https://www.microchip.com/en-us/product/PIC18F57Q43) | Found on Microchip.com |
| **PIC18F57Q43 Datasheet URL** | [PIC18F57Q43 Datasheet](https://ww1.microchip.com/downloads/en/DeviceDoc/PIC18F27-47-57Q43-Data-Sheet-40002147.pdf) | Primary device datasheet |
| **Technical Reference Manual URL** | [PIC18-Q43 Family Reference](https://www.microchip.com/en-us/products/microcontrollers/8-bit-mcus/pic18-q43) | Peripheral documentation |
| **Vendor Link** | [DigiKey Product Page](https://www.digikey.com/en/products/detail/microchip-technology/PIC18F57Q43-I-PT/11618236) | Vendor purchase link |
| **Code Examples** | [Microchip MCC Melody Examples](https://github.com/microchip-pic-avr-examples) <br> [I2C Host Example](https://github.com/microchip-pic-avr-examples/pic18f57q43-i2c-host-example) | Peripheral usage examples |
| **External Resources** | [Microchip PIC18 Q43 Overview](https://www.microchip.com/en-us/products/microcontrollers/8-bit-mcus/pic18-q43) | Tutorials / documentation |
| **Unit Cost** | ~$3.50 (qty 1, DigiKey) | Vendor pricing |
| **Absolute Maximum Current (entire IC)** | 200 mA total through VDD/VSS pins | From datasheet |
| **Supply Voltage Range** | Recommended: 1.8 – 5.5 V | From datasheet |
| **Maximum GPIO Current (per pin)** | 25 mA source/sink (max rating) | From datasheet |
| **Supports External Interrupts?** | Yes | Multiple interrupt-on-change pins |
| **Required Programming Hardware** | Microchip SNAP / PICkit 4 / PICkit 5 | ICSP programming interface |


| Module | # Available | Needed | Associated Pins |
|---|---|---|---|
| **UART** | 2 (EUSART) | 0–1 | Configurable via PPS |
| **SPI** | 2 | 0 | Configurable via PPS |
| **I2C** | 2 MSSP modules | 1 | SDA/SCL via PPS |
| **GPIO** | 44 I/O pins | ~2 | Any GPIO |
| **ADC** | 12-bit ADC (up to 35 channels) | 0 | Analog capable pins |
| **PWM** | Multiple CCP/PWM modules | 0 | Configurable |
| **Program/Debug** | 1 ICSP interface | 1 | MCLR, PGD, PGC |


![PIC18F57Q43 pinout](https://github.com/riatron8/EGR314IndividualDataSheet/raw/main/docs/08-Microcontroller-Selection/PIC_pinout.png)


Using the pin diagram for the PIC18F57Q43, there are more than enough pins available for the project requirements. The TQFP-48 package contains 48 pins, with over 40 configurable GPIO pins. Since the project only requires two pins for the I2C interface and possibly additional pins for debugging or communication, the microcontroller easily supports the required connections.

I have decided to go with the PIC18F57Q43-I/PT. This microcontroller is part of the PIC18 Q43 family and provides the peripherals needed for the project, including I2C communication for sensor integration. The device is also compatible with Microchip’s MPLAB X environment and MCC Melody, which simplifies peripheral configuration and code generation. Although the PIC does not include built-in wireless connectivity like the ESP32, it is well suited for interfacing with sensors and communicating with other controllers on the rover that handle wireless communication. The TQFP package also satisfies the surface mount requirement for this project.
