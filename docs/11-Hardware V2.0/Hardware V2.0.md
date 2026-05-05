---
title: Hardware V2.0
---

## Hardware V2.0

If I were to create a version 2.0 of my hardware design, the first improvement would be redesigning the PCB to better match the final direction of the project. The current design changed during development, especially with the move toward the SHTC3 humidity sensor. Because of that, a second version of the PCB could be laid out more cleanly around the final sensor, communication pins, and power needs.

A revised PCB would improve reliability and make the design easier to assemble and debug. The schematic section shows the important connections for the final design, including the PIC microcontroller, the SHTC3 sensor, the I²C lines, power, ground, and the button input. In a Version 2.0 board, I would use that final schematic as the starting point instead of adapting from earlier design assumptions.

One specific improvement would be cleaning up the routing for the I²C connections between the PIC and the SHTC3. Since the sensor communicates using SDA and SCL, those traces should be routed clearly and kept simple. I would also make sure the pull-up resistors, power connections, and ground connections are placed in a way that reduces possible communication issues.

Another improvement would be using more of the SHTC3’s built-in functionality. The sensor can measure both humidity and temperature, but the final system mainly focused on humidity. In a Version 2.0 design, I would include temperature data as part of the sensor output. This would add useful environmental information without needing a major hardware change, since the same sensor already supports it.

A larger improvement would be adding more environmental sensors if the project requirements expanded. For example, the subsystem could include sensors for light, air quality, or pressure. This would make the sensor node more useful as a general environmental monitoring module instead of only a humidity sensor. However, I would only add these if they had a clear purpose, since adding more sensors also increases code complexity, wiring, and possible failure points.

Overall, the main goal of a Hardware V2.0 would be to make the board match the final implementation more closely. The original hardware design worked for demonstrating the core function, but a revised version could be cleaner, easier to debug, and more capable by fully using the SHTC3 sensor and improving the PCB layout.
