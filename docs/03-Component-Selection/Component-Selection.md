---
title: Module's Selected Major Components
---

## Module's Selected Major Components

The final component selection for my individual subsystem focuses on the Riley Sensor Node (F). This node is responsible for reading environmental humidity and sending that information into the rover communication system. Since the individual subsystem is fairly specific, the main component decision was the environmental sensor, along with the PIC microcontroller configuration needed to read it.

The final humidity sensor selected was the **SHTC3-TR-10KS**. I reviewed multiple sensor options before choosing it, including simpler temperature-only sensors and more accurate temperature sensors. The SHTC3 was selected because it measures both humidity and temperature over I²C, which made it a better fit for the final design than a temperature-only sensor.

---

## Final Major Component Summary

| Component | Selected Part | Purpose | Reason for Selection |
|---|---|---|---|
| Microcontroller | PIC Microcontroller | Reads the sensor and handles local control logic | Required for I²C communication and integration with the rest of the system |
| Environmental Sensor | SHTC3-TR-10KS | Measures humidity and temperature | Provides humidity measurement, uses I²C, has a low pin count, and avoids needing a separate humidity sensor |

Passive components, wiring, and pushbuttons are not included in this table because the requirement only asks for major components.

---

## Sensor Selection Decision Process

The sensor choice changed from the earlier idea of only measuring temperature to a final design that measures humidity. This was important because the sensor node’s final role was environmental sensing, and humidity was the more relevant measurement for the final subsystem.

I compared three sensor options:

- **TC74A4-3.3VCTTR**
- **MCP9808-E/MS**
- **SHTC3-TR-10KS**

The TC74A4 was familiar and simple because it had already been used in class, but it only measured temperature and did not meet the final humidity sensing goal. The MCP9808 was more accurate and had better resolution, but it was still only a temperature sensor. The SHTC3 was selected because it provides both humidity and temperature readings, uses I²C, and only requires a small number of pins.

Even though the SHTC3 has a very small package and was less familiar to set up, it matched the final product requirements better than the other options. The extra setup difficulty was worth it because it avoided needing a separate humidity sensor.

---

## Requirements Alignment

The SHTC3-TR-10KS meets the subsystem requirements because it directly supports the sensor node’s main function: measuring environmental humidity. Its I²C interface also works well with the PIC because it only requires SDA and SCL communication lines.

Using a digital I²C sensor reduces the need for analog signal conditioning or ADC calibration. This makes the design simpler and more reliable, which was important for the final demonstration.

The PIC microcontroller supports the subsystem by reading the sensor, responding to the debug button input, and sending the humidity reading into the rest of the system.

---

## MCC Configuration / PIC Pinout Table

| PIC Pin | Function | Direction | Description |
|---|---|---|---|
| RC4 | SDA1 | In/Out | I²C data line for the SHTC3 humidity sensor |
| RC3 | SCL1 | In/Out | I²C clock line for the SHTC3 humidity sensor |
| RA5 | GPIO Input | Input | Button input used to force a sensor reading |
| VDD | Power | Power | Supplies power to the PIC and sensor circuit |
| GND | Ground | Ground | Common ground reference |

---

## Design Iteration and Feedback Integration

The component selection was updated to better match the final design and the actual role of the sensor node. Earlier component choices focused more on general temperature sensing, but the final implementation required humidity data. Because of that, the final design moved toward the SHTC3-TR-10KS.

The design was also simplified compared to earlier ideas. Instead of adding extra sensors or more complicated processing, the final design focuses on one environmental sensor that can provide the needed data reliably.

This final component selection better matches the implemented subsystem and avoids including components that were not actually used.

-----------
**Environment Sensor**

<table>
  <tr>
    <td><strong>Solution</strong></td>
    <td><strong>Pros</strong></td>
    <td><strong>Cons</strong></td>
  </tr>
  <tr>
    <td>
      <img src="https://raw.githubusercontent.com/riatron8/EGR314IndividualDataSheet/main/docs/03-Component-Selection/Comp_1.png" width="300"><br><br>
      <strong>Option 1</strong><br>
      TC74A4-3.3VCTTR<br>
      $1.15 / each<br>
      <em><a href="https://www.digikey.com/en/products/detail/microchip-technology/TC74A4-3-3VCTTR/443268">Link to product</a></em>
    </td>
    <td>
      <ul>
        <li>Already used in class</li>
        <li>Low pin count</li>
        <li>Very simple and easy to set up</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Not especially accurate</li>
        <li>Lower resolution than competition</li>
        <li>Low acceptable voltage range</li>
      </ul>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td><strong>Solution</strong></td>
    <td><strong>Pros</strong></td>
    <td><strong>Cons</strong></td>
  </tr>
  <tr>
    <td>
      <img src="https://raw.githubusercontent.com/riatron8/EGR314IndividualDataSheet/main/docs/03-Component-Selection/Comp_2.png" width="300"><br><br>
      <strong>Option 2</strong><br>
      MCP9808-E/MS<br>
      $1.40 / each<br>
      <em><a href="https://www.digikey.com/en/products/detail/microchip-technology/MCP9808-E-MS/2802083">Link to product</a></em>
    </td>
    <td>
      <ul>
        <li>Very accurate</li>
        <li>Higher resolution</li>
        <li>Good voltage range</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Less simple and has more pins to be aware of</li>
        <li>Slightly more expensive</li>
      </ul>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td><strong>Solution</strong></td>
    <td><strong>Pros</strong></td>
    <td><strong>Cons</strong></td>
  </tr>
  <tr>
    <td>
      <img src="https://raw.githubusercontent.com/riatron8/EGR314IndividualDataSheet/main/docs/03-Component-Selection/Comp_3.png" width="300"><br><br>
      <strong>Option 3</strong><br>
      SHTC3-TR-10KS<br>
      $2.06 / each<br>
      <em><a href="https://www.digikey.com/en/products/detail/sensirion-ag/SHTC3-TR-10KS/9477852">Link to product</a></em>
    </td>
    <td>
      <ul>
        <li>Detects temperature and humidity</li>
        <li>Few pins</li>
        <li>Quite accurate</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Very small package</li>
        <li>Unfamiliar setup</li>
      </ul>
    </td>
  </tr>
</table>

<p><strong>Choice: Option 3 - SHTC3-TR-10KS</strong></p>

<br>

**Voltage Regulator**

<table>
  <tr>
    <td><strong>Solution</strong></td>
    <td><strong>Pros</strong></td>
    <td><strong>Cons</strong></td>
  </tr>
  <tr>
    <td>
      <img src="https://github.com/riatron8/EGR314IndividualDataSheet/raw/main/docs/03-Component-Selection/Regulator_1.png" width="300"><br>
      <strong>Option 1</strong><br>
      LM2595S-3.3/NOPB<br>
      $5.35 / each<br>
      <em><a href="https://www.digikey.com/en/products/detail/texas-instruments/LM2595S-3-3-NOPB/363698">Link to product</a></em>
    </td>
    <td>
      <ul>
        <li>High efficiency switching regulator (~80-90%)</li>
        <li>Wide input voltage range (4.5-40 V)</li>
        <li>Can easily step down 12 V to 3.3 V</li>
        <li>Capable of supplying up to 1 A output current</li>
        <li>Lower heat generation compared to linear regulators</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Requires additional external components (inductor, diode, capacitors)</li>
        <li>Slightly more complex circuit design</li>
        <li>Larger footprint than simple linear regulators</li>
      </ul>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td><strong>Solution</strong></td>
    <td><strong>Pros</strong></td>
    <td><strong>Cons</strong></td>
  </tr>
  <tr>
    <td>
      <img src="https://github.com/riatron8/EGR314IndividualDataSheet/raw/main/docs/03-Component-Selection/Regulator_2.png" width="300"><br>
      <strong>Option 2</strong><br>
      AMS1117-3.3<br>
      $0.40 / each<br>
      <em><a href="https://www.digikey.com/en/products/detail/umw/AMS1117-3-3/17635498">Link to product</a></em>
    </td>
    <td>
      <ul>
        <li>Very simple to implement</li>
        <li>Requires very few external components</li>
        <li>Small circuit footprint</li>
        <li>Low cost</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Linear regulator (low efficiency)</li>
        <li>Large power loss when converting from 12 V to 3.3 V</li>
        <li>Significant heat generation</li>
        <li>Limited current capability (~800 mA)</li>
        <li>Poor choice for large voltage drops</li>
      </ul>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td><strong>Solution</strong></td>
    <td><strong>Pros</strong></td>
    <td><strong>Cons</strong></td>
  </tr>
  <tr>
    <td>
      <img src="https://github.com/riatron8/EGR314IndividualDataSheet/raw/main/docs/03-Component-Selection/Regulator_3.png" width="300"><br>
      <strong>Option 3</strong><br>
      MP1584EN<br>
      $1.20 / each<br>
      <em><a href="https://www.monolithicpower.com/en/mp1584en-lf-z.html">Link to product</a></em>
    </td>
    <td>
      <ul>
        <li>High efficiency (~90%)</li>
        <li>Small switching regulator</li>
        <li>Supports up to 3 A output current</li>
        <li>Very compact design</li>
        <li>Wide input voltage range</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Requires careful PCB layout</li>
        <li>Slightly more complex configuration</li>
        <li>Less familiar device compared to common regulators</li>
        <li>Datasheet and configuration are slightly harder for beginners</li>
      </ul>
    </td>
  </tr>
</table>

<p><strong>Choice: Option 1 - LM2595S-3.3/NOPB</strong></p>
