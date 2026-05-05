## API Compliance Overview

The Riley Sensor Node (F) follows the team communication structure by sending humidity data using the defined message format. While the original design included a more complex packet-based protocol, the final implementation uses a simplified but consistent message structure that still meets the system requirements.

The goal for this subsystem was to remain compatible with the team communication system while keeping the implementation simple and reliable.

---

## Messages Used

### Outgoing Messages

| Message | Destination | Description |
|---|---|---|
| Humidity Data | Gateway Node (W) | Sends current humidity reading (forwarded through H) |
| Debug Trigger (Button) | Local | Forces a new sensor reading |

### Incoming Messages

This node does not require incoming messages for normal operation. All actions are either automatic or triggered locally through the button input.

---

## Message Format

Humidity data is transmitted using the team-defined message structure. Messages follow a consistent format with start and end markers, source and destination identifiers, and a payload.

An example humidity message is:

AZFWH045BY

In this message:
- AZ represents the start of the message  
- F represents the source node (sensor node)  
- W represents the destination node (gateway/MQTT node)  
- H indicates a humidity data message  
- 045 is the humidity value (45%)  
- BY represents the end of the message  

This format matches the overall team communication protocol and ensures that messages can be correctly interpreted by other nodes in the system.

---

## Compliance with Team Communication Structure

The node follows the required communication structure defined by the team:

- Data is generated at node F  
- Data is sent toward node W (gateway/MQTT node)  
- Data is physically routed through node H (camera system)  
- Data is published to MQTT for the user  

This distinction between logical destination (W) and physical routing (through H) matches the team communication design.

---

## Verification and Testing

Compliance was verified by observing successful transmission of humidity data through the system. Testing included:

- Triggering sensor readings using the button input  
- Confirming data passed through the camera system (H)  
- Verifying that the data reached the gateway node (W) and was published to MQTT  

These tests confirmed that the node follows the expected communication flow and produces valid data messages.

---

## Design Decisions and Deviations

The original design included a more structured packet-based communication protocol with message types, acknowledgements, and error handling. However, the final implementation simplified this structure because those features were not required for the subsystem to function.

This decision reduced complexity and improved reliability, while still maintaining compatibility with the overall system communication flow.

The simplified message format still meets the functional requirements of the system and allows the node to integrate correctly with the rest of the rover.
