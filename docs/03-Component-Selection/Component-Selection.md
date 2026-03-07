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

<li>Unfamiliar setup</li>
</ul>
   </td>
  </tr>
</table>

