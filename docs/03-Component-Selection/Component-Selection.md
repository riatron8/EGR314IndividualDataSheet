---
title: Module's Selected Major Components
---

## Module's Selected Major Components

The following sections are the selected major components necessary for  .....

>**For each of the following sections, use <ins>one of the two styles</ins> given near the end. *REMOVE THIS NOTE***

### Power Management

(**remove this note/placeholder**: this is where your 3.3 volt switching regulator, any other needed power regulator, and power source {if applicable} **THAT WERE SELECTED**)

For more details, review the ["Appendix - Component Selection Process - Power Mangement"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#power-management) selection.

### Sensor

(**remove this note/placeholder**: if applicable, this is where your  **SELECTED** sensor is shown. Otherwise, remove this section.)

For more details, review the ["Appendix - Component Selection Process - Sensor"](https://embedded-systems-design.github.io/EGR314DataSheetTemplate/Appendix/01-Componet-Selection/Component-Selection-Process/#sensor) selection.


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

<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


<img src="images/image1.png" width="" alt="alt_text" title="image_tooltip">

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

<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


<img src="images/image2.png" width="" alt="alt_text" title="image_tooltip">
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

<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image3.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


<img src="images/image3.png" width="" alt="alt_text" title="image_tooltip">

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


**Choice**: Option 3: SHTC3-TR-10KS

**Rationale**: This sensor is able to detect both temperature and humidity, removing the need for a separate humidity sensor. In addition, only having 4 pins means that it should be simple to set up on the hardware side. In addition, for containing two different sensors, it is fairly cheap, and the reduced number of components. \
 \
