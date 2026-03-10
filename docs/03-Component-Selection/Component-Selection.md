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
   <td>Solution
   </td>
   <td>Pros
   </td>
   <td>Cons
   </td>
  </tr>
  <tr>
   <td>

<img src="https://raw.githubusercontent.com/riatron8/EGR314IndividualDataSheet/main/docs/03-Component-Selection/Comp_1.png" width="300">


<p>
Option 1
<p>
TC74A4-3.3VCTTR
<p>
$1.15/ each
<p>
<em><a href="https://www.digikey.com/en/products/detail/microchip-technology/TC74A4-3-3VCTTR/443268">Link to product</a> </em>
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
   <td>Solution
   </td>
   <td>Pros
   </td>
   <td>Cons
   </td>
  </tr>
  <tr>
   <td>

<img src="https://raw.githubusercontent.com/riatron8/EGR314IndividualDataSheet/main/docs/03-Component-Selection/Comp_2.png" width="300">
Option 2
<p>
MCP9808-E/MS
<p>
$1.40/ each
<p>
<em><a href="https://www.digikey.com/en/products/detail/microchip-technology/MCP9808-E-MS/2802083">Link to product</a> </em>
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

<li>Less simple and has more pins to be aware of.</li>

<li>Slightly more expensive</li>
</ul>
   </td>
  </tr>
</table>



<table>
  <tr>
   <td>Solution
   </td>
   <td>Pros
   </td>
   <td>Cons
   </td>
  </tr>
  <tr>
   <td>


<img src="https://raw.githubusercontent.com/riatron8/EGR314IndividualDataSheet/main/docs/03-Component-Selection/Comp_3.png" width="300">

<p>
Option 3
<p>
SHTC3-TR-10KS
<p>
$2.06/ each
<p>
<em><a href="https://www.digikey.com/en/products/detail/sensirion-ag/SHTC3-TR-10KS/9477852?utm_source=chatgpt.com">Link to product</a> </em>
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

**Voltage Regulator**

Option 1

LM2595S-3.3/NOPB
$5.35 / each
Link to product

Pros

High efficiency switching regulator (~80–90%)

Wide input voltage range (4.5–40 V)

Can easily step down 12 V to 3.3 V

Capable of supplying up to 1 A output current

Lower heat generation compared to linear regulators

Cons

Requires additional external components (inductor, diode, capacitors)

Slightly more complex circuit design

Larger footprint than simple linear regulators

Option 2

AMS1117-3.3
$0.40 / each
Link to product

Pros

Very simple to implement

Requires very few external components

Small circuit footprint

Low cost

Cons

Linear regulator (low efficiency)

Large power loss when converting from 12 V to 3.3 V

Significant heat generation

Limited current capability (~800 mA)

Poor choice for large voltage drops

Option 3

MP1584EN Step-Down Converter
$1.20 / each
Link to product

Pros

High efficiency (~90%)

Small switching regulator

Supports up to 3 A output current

Very compact design

Wide input voltage range

Cons

Requires careful PCB layout

Slightly more complex configuration

Less familiar device compared to common regulators

Datasheet and configuration slightly harder for beginners

Choice: Option 1 – LM2595S-3.3/NOPB
Rationale

The LM2595S-3.3 switching regulator was selected as the final solution because it efficiently converts the 12 V system input voltage to the required 3.3 V rail used by the microcontroller and sensors. Unlike the AMS1117 linear regulator, which would dissipate a significant amount of power as heat when dropping from 12 V to 3.3 V, the LM2595 maintains high efficiency and significantly reduces thermal losses. While the MP1584EN also provides efficient voltage conversion, the LM2595 was chosen due to its simpler design requirements and widespread documentation, making it easier to implement reliably. Overall, the LM2595 provides the best balance of efficiency, reliability, and ease of implementation for the rover system.

If you'd like, I can also make a second comparison table for the power source selection (A23 battery vs wall adapter vs Li-ion pack), which is usually expected alongside the regulator comparison in this assignment.

<li>Unfamiliar setup</li>
</ul>
   </td>
  </tr>
</table>

