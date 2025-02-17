# Laboratory 3. Let’s Switch: Transistors as Switches
Aashika Uppala, Megan Fister

2/17/2025
### Introduction
The purpose of this lab is to explore the functionality of transistors as switches, focusing on the Bipolar Junction Transistor (BJT).
While modern digital electronics primarily use Metal-Oxide-Semiconductor Field-Effect Transistors (MOSFETs), BJTs still play a crucial role in various applications such as amplification and switching. 
This lab aims to demonstrate how BJTs can control the current flow in an LED and a motor, analyzing their behavior in different operating modes.
Additionally, we will examine the role of diodes and LEDs in circuit design. 
Diodes, which allow current to flow in only one direction, are vital in protection circuits, while LEDs serve as indicators in numerous electronic devices.
The lab will involve constructing circuits to observe transistor operation and evaluating the effects of varying input voltages on circuit performance.

### Methods

### Results


### Discussion
#### Part 1
_Discussion question 1: How does the current through the LED compare between circuits 1 and 2?_

In Circuit 1, where the LED is directly connected to a switch, the current is solely dependent on the resistor value and the voltage source.

In Circuit 2, where the LED is controlled by a transistor, the current is regulated more effectively due to the transistor’s switching capability.

This results in a more stable and predictable current through the LED, as opposed to the direct switch circuit where variations in source voltage can lead to flucuating current.


_Discussion question 2: How does your measured VCE compare to the one listed in the datasheet? Do you think we are operating this transistor in the saturation region?_

The datasheet specifies a maximum VCE (saturation) of 1.2V. Our measured VCE should ideally be lower than this value when the transistor is fully saturated.
If our observed VCE is close to this threshold or below, it indicates that the transistor is operating in the saturation region. 
Adjusting the power supply should further confirm this by showing minimal changes in IC when VCE is in saturation.

#### Part2
_Discussion question 1: What is the voltage drop (VCE) across the transistor (Q1) when the motor is in the Fast setting? How does this compare with the circuit that drove the LED?_

The voltage drop across Q1 in the motor circuit at the Fast setting should be compared to the LED circuit. 
Generally, the motor circuit requires higher current than the LED circuit, leading to a slightly higher VCE in the motor circuit.
However, both should remain within the saturation region if the transistor is operating correctly.


_Discussion question 2: How much current is going through the motor in the Fast setting? How does this compare to the current that the LED circuit used?_

The motor typically draws significantly more current than the LED circuit due to its mechanical load. 
If the switch used in the LED circuit was barely sufficient to handle LED current, it would be inadequate for the motor, necessitating the use of a transistor switch.
The transistor allows for effective current amplification, enabling the motor to receive the necessary power while being controlled by a lower input current.

### Summary
This lab provided a hands-on exploration of transistors as switches, demonstrating their ability to regulate current flow in circuits involving LEDs and motors.
By constructing different circuit configurations, we observed the effects of transistor operation, including its behavior in saturation and the relationship between base and collector currents.
Key findings include the importance of VCE in determining the transistor's state, the advantages of using a transistor 
over a direct switch for stable current regulation, and the necessity of transistors in high-current applications like motor control.
The practical applications of these concepts are widespread in modern electronics, reinforcing the significance of transistors in both simple and complex circuit designs.
Overall, this experiment enhanced our understanding of semiconductor devices, specifically diodes and BJTs, and their essential roles in circuit functionality.
