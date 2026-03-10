---
title: Appendix - Power Budget
---

## Overview
This power budget is used to ensure that all the selected components can be properly powered by the selected power source.

![budget1](https://github.com/riatron8/EGR314IndividualDataSheet/raw/main/docs/09-Power-Budget/55210420-1.png){style width:"350" height:"300;"}

![budget2](https://github.com/riatron8/EGR314IndividualDataSheet/raw/main/docs/09-Power-Budget/55210420-2.png){style width:"350" height:"300;"}

## Conclusions

A regulated 12 V wall adapter was selected as the external power source. The supply feeds the LM2595 switching regulator, which generates the 3.3 V rail used by the system electronics. The worst-case load current on the 3.3 V rail with a 25 % safety margin is approximately 250.5 mA. Assuming an 80 % efficient switching regulator, this corresponds to about 86 mA drawn from the 12 V source. A typical 12 V wall adapter rated for 2 A can easily supply this current, leaving approximately 1.9 A of remaining capacity. Therefore, the wall supply comfortably supports the system power requirements and is a more practical choice than the small A23 battery.

## Resouces

The power budget as a PDF download is available [*here*](https://github.com/riatron8/EGR314IndividualDataSheet/raw/main/docs/09-Power-Budget/Power_budget_pic.pdf), and a Microsoft Excel Sheet [*here*](https://github.com/riatron8/EGR314IndividualDataSheet/raw/main/docs/09-Power-Budget/Power_Budget_Completed.xlsx).
