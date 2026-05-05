---
title: Reflection
---

## Review of Module's Success

Looking back at the module requirements, most of the core functionality was successfully implemented. The system uses a PIC microcontroller as required, and the humidity sensor is able to take readings and send them through the communication chain. The data is successfully transmitted through the rover system and made available to the user through the MQTT gateway, which meets the main goal of reporting external environmental measurements.

The humidity sensing requirement was mostly met. While the humidity was not formally measured against a calibrated reference, the SHTC3 sensor consistently produced reasonable and stable readings during testing. The data could be interpreted correctly by the microcontroller and passed along to the rest of the system without issues.

The power requirement was also met in terms of functionality. The system used wall power as the input to the 3.3V voltage regulator, and the regulator functioned correctly in supplying stable power to the microcontroller and sensor. However, the original requirement mentioned a battery-powered system to allow the rover to remain wireless. That part was not implemented in the final design, so while the power system worked correctly, it did not fully meet the original wireless requirement.

Overall, the main sensing and communication goals were achieved, and the system functioned reliably during testing, with the only major difference being the use of wall power instead of a battery.

---

## Microcontroller / Module Startup Tips

- Start with simple I/O testing before trying to integrate sensors or communication.
- Set up and test I²C communication early, since many sensors depend on it.
- Double and triple check that the components you plan to use are actually the ones you have configured and wired in your design.
- Give yourself a strong foundation with documentation (datasheets, notes, and configuration details) so you have something to reference when things go wrong.
- Use debug outputs whenever possible to see what the system is doing.
- Test each subsystem independently before integrating everything.
- Leave plenty of time for debugging, since it will take longer than expected.
- Add redundancy where possible, because something will end up failing at some point.

---

## Lessons Learned

One of the most important things learned during this project was how much simpler designs are often more reliable. The original plan included more complex communication structures and additional features, but simplifying the system made it easier to implement and debug.

Another key lesson was the importance of testing each subsystem independently. When something didn’t work, breaking it down into smaller parts made it much easier to find the issue. This was especially important for getting I²C communication working correctly with the sensor.

Working with real hardware also showed how important wiring and physical layout are. Even when the code is correct, issues like incorrect connections or noise can cause problems. This made it clear that hardware and software need to be developed together.

The project also reinforced the importance of reading datasheets carefully. The SHTC3 sensor required specific communication steps, and understanding those details was necessary to get correct readings.

Time management was another major lesson. Debugging and integration took longer than expected, especially when dealing with communication between nodes. Leaving more time for testing would have reduced last-minute pressure.

Integration between team members was also an important experience. Even when individual subsystems worked, getting everything to communicate properly required coordination and additional debugging.

Another takeaway was that documentation is more important than expected. Keeping track of design decisions made it easier to update diagrams and reports later.

The value of having simple debug tools, like a button to force a sensor reading, became very clear. These features made testing faster and more reliable.

It was also learned that initial design assumptions often change. Being flexible and willing to adjust the design was necessary to get a working system.

Finally, the project showed that focusing on core functionality first is the best approach. Once the main features work, improvements can be added, but trying to implement everything at once makes the system harder to complete.

---

## Recommendations for Future Students

1. Start working with your microcontroller and basic I/O as early as possible so you are comfortable before adding more complex components.
2. Learn how to use I²C communication early, since many sensors depend on it and it can take time to get working correctly.
3. Double and triple check that your selected components match your actual configuration and hardware setup to avoid mismatches later.
4. Leave yourself plenty of time for debugging, since integration issues will take longer than expected.
5. Build in redundancy and fallback options where possible, because something in the system will likely fail during development.
