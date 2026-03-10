---
title: Module's Requirements
---

## Module Requirements
The following sections document the requirements that the external sensor modules need to fulfill to be able to fully and accurately take external measurements, primarily humidity. In addition, the rover should be able to send those measurements to the user through the ESP on a team member's board, giving the user the current external measurements. The power for the sensors will come through the rover's main battery, and be filtered by the 3.3V power switching power regulator, allowing the rover to remain wireless.

| **Requirement Description** | **Measure of<br> Threshold** | **Target<br>Measure** |**Stretch<br>Requirement<br>(Y-N)**|
|-----------------------------| ----------------- | ----------------- | :-----: |
| Surface mounted, 3.3V switching power regulator | 3.2 Volts | 3.3 Volts | No |
| Surface mounted microcontroller | 1 PIC or ESP | PIC | No |
| Humidity sensor | Able to accurately measure the humidity around the rover within 3% humidity in the air | Sends a reading of the humidity that can be interpreted by the microcontroller  | No |

