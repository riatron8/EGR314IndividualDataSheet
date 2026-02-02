---
title: Module's Requirements
---

## Module Requirements
The following sections document the requirements that the external sensor modules need to fulfill to be able to fully and accurately take external measurements, primarily temperature and humidity. In addition, the rover should be able to send those measurements to the user through the ESP, giving the user the current external measurements. The power for the sensors will come through the rover's main battery, and be filtered by the 3.3V power switching power regulator, allowing the rover to remain wireless.

| **Requirement Description** | **Measure of<br> Threshold** | **Target<br>Measure** |**Stretch<br>Requirement<br>(Y-N)**|
|-----------------------------| ----------------- | ----------------- | :-----: |
| Surface mounted, 3.3V switching power regulator | 3.2 Volts | 3.3 Volts | No |
| Surface mounted microcontroller | 1 PIC or ESP | ESP32 | No |
| Wireless Communication | Able to send or receive a Wi-Fi data | Send and receive Wi-Fi Data to MQTT | Yes |
| Temperature sensor | Able to accurately measure the ambient temperature around the rover  within 5 degrees Farenheit | Sends a reading of the temperature that can be interpreted by the microcontroller | No |
| Humidity sensor | Able to accurately measure the humidity around the rover within 3% humidity in the air | Sends a reading of the humidity that can be interpreted by the microcontroller  | No |
| HMI | Able to show the current temperature and humidity to the operator | Shows the measurement readings, probably though an app or website, to the user continuously | No |
