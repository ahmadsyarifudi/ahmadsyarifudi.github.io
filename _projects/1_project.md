---
layout: page
title: The Work of a Process
description: Designing a System Program for AVR Microcontrollers That Can Used to Regulate The  Work of a Process Unit
img: assets/img/project/project1/2.jpg
importance: 1
category: college
related_publications: true
---

Two types of chemical solutions will be placed into the storage tank, then heated and stirred, and finally discharged for the next process. As shown in the diagram, the unit contains several sensors (inputs) and actuators (outputs) that will be utilized by the microcontroller to control the process. Under normal conditions (when the system is not operating), all valves are closed, and similarly, the heater and stirrer are turned off.

this project pdf [here](https://drive.google.com/file/d/10qAKELwr0HBtpwgwk3e-BjsHP0C6eV2l/view?usp=drive_link)

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project/project1/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Circuit design on protheus
</div>
The START button must be pressed to initiate the process. Initially, solution 1 and solution 2 should be filled into the tank by opening valves INFLOW1 and INFLOW2 until the TANKFUL sensor = '1' (active), indicating that the solution level has reached the desired level. Subsequently, valves INFLOW1 and INFLOW2 are closed. After that, the Heater is turned on via HTRON and the Stirrer is activated through STIRON, both of which remain on until the desired solution temperature is achieved, indicated by the TEMPOK sensor = '0' (active). 

The heated mixture of solutions is then routed to the next process through the OUTFLOW valve, which will be closed after the TANKMT sensor = '0' (active). The entire process will repeat if the HOLD button has not been pressed earlier. If the HOLD button is pressed, the system will pause temporarily and resume the same process cycle when the START button is pressed again.

Additionally, the system is equipped with an emergency SHUTDOWN switch. If this button is pressed, the processor will be interrupted via the INT0 line, which stops any ongoing process. The ALARM light and BUZZER will activate (ON) in response.
