---
title: Module's Block Diagram
tags:
- tag1
- tag2
---

## Overview
This block diagram shows the planning for the final board. The overall goal is to use a humidity sensor, and send the results to a team member to display them to the user. The power will be coming in with 12V, from either a wall or a team member. The board will be able to connect to other parts of the board, such as to receive other signals or measurements to be displayed.

## Block Diagram 

![Individual Block diagram ](https://github.com/riatron8/EGR314IndividualDataSheet/blob/main/docs/02-Block-Diagram/Final_314_Individual_block_diagram.drawio.png)

## Block Diagram Design Process

The individual block diagram was made to clearly show what the Riley Sensor Node (F) actually does and how it connects to the rest of the system. Instead of trying to show the whole rover, the focus here is just on the parts that matter for this subsystem: the humidity sensor, the microcontroller, the button input, and the connection to the camera system (H).

The layout follows how things are actually wired. The humidity sensor feeds directly into the microcontroller, which handles reading the data and sending it out. The button is included because it ended up being useful for testing, since it can force a reading without needing to go through the full system.

One thing that might seem a bit odd is that the data goes through the camera system instead of directly to the gateway. That wasn’t necessarily the most efficient design, but it matches how the system was actually built and wired. Since the goal of this diagram is to reflect the final implementation, it was more important to show the real data path than an ideal one.

Overall, the diagram is kept pretty simple on purpose. It only shows the components and connections that are actually used, so it’s easier to read and easier to relate back to the physical system.

---

## Requirements Alignment

This block diagram shows how the sensor node meets the main requirement of collecting and sending environmental data. The humidity sensor provides the data, the microcontroller processes it, and the communication path shows how that data eventually reaches the user through MQTT.

Including the connection to the camera system makes it clear how this node fits into the larger system. Even though it’s not directly connected to the gateway, the diagram shows the full path the data takes, which is important for understanding how everything works together.

The button input also ties into requirements around testing and reliability. Being able to manually trigger a reading made it a lot easier to verify that the sensor and communication were working without depending on everything else being active.

---

## Design Iteration and Feedback Integration

This diagram changed a bit over time as the system got closer to the final version. Earlier versions either left out parts of the communication path or included things that didn’t end up being used.

Based on feedback and just working through integration issues, the diagram was simplified and updated to match what was actually implemented. The communication path through the camera system was clarified, and anything unnecessary was removed.

The final version is less complicated than what was originally planned, but it’s a much better representation of the system that actually works.

---

## Diagram Source Files

- [Download PDF](https://github.com/riatron8/EGR314IndividualDataSheet/raw/main/docs/02-Block-Diagram/Final_314_Individual_block_diagram.drawio.pdf)

