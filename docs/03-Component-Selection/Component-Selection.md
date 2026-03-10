---
title: Module's Selected Major Components
---

## Module's Selected Major Components

The following sections are the selected major components necessary for properly measuring the environement around the rover, and the power neccessary to keep the measurement operational.



### Power Management

(**remove this note/placeholder**: this is where your 3.3 volt switching regulator, any other needed power regulator, and power source {if applicable} **THAT WERE SELECTED**)

For more details, review the ["Appendix - Component Selection Process - Power Mangement"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#power-management) selection.

**Choice**: Option 2: MCP9808-E/MS

### Sensor

**Choice**: Option 2: MCP9808-E/MS

**Rationale**: This sensor is able to accurately detect humidity with a fairly low cost, even compared to the less precise option. Since a team member will be measuring temperature, the added temperature functionality is not needed and not worth the extra cost.

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

<p><strong>Rationale:</strong> This sensor is able to detect both temperature and humidity, removing the need for a separate humidity sensor. In addition, only having 4 pins means that it should be simple to set up on the hardware side. For containing two different sensors, it is fairly cheap, and the reduced number of components is another benefit.</p>

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

<p><strong>Rationale:</strong> The LM2595S-3.3 switching regulator was selected as the final solution because it efficiently converts the 12 V system input voltage to the required 3.3 V rail used by the microcontroller and sensors. Unlike the AMS1117 linear regulator, which would dissipate a significant amount of power as heat when dropping from 12 V to 3.3 V, the LM2595 maintains high efficiency and significantly reduces thermal losses. While the MP1584EN also provides efficient voltage conversion, the LM2595 was chosen due to its simpler design requirements and widespread documentation, making it easier to implement reliably. Overall, the LM2595 provides the best balance of efficiency, reliability, and ease of implementation for the rover system.</p>
