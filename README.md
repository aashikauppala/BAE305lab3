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
#### Instruments
• A Digital Multimeter
• A DC Power supply
• Resistors: 2.2Ω, 270Ω, 1kΩ
• An LED (any type)
• A sliding switch (from the Sparkfun inventor’s kit)
• An electric motor (from the Sparkfun inventor's kit)
• A NTE 125 diode
• A 1kΩ trimmer potentiometer
• A TIP31C transistor

### Results
#### Part 1 - LED Driving Circuits

_Measured Resistance_
|Resistor|Expected (Ω)| Measured (Ω) |
|---|---|---|
|$R_1$|  270 | 269.6 |
|$R_2$| 1000   | 989 |
|$R_3$|  2.2  | 2.6 |

##### Measurements in a circuit with an LED directly connected to a switch


![Figure 3](https://github.com/aashikauppala/BAE305lab3/blob/main/Lab%203%20Figure%203.png)

_Measured voltage at each point with respect to ground (T4)_
|Test Point|Voltage - Switch On (V)| Voltage - Switch Off (V) |
|---|---|---|
|T2|  2.014 | 5.006 |
|T3| 0.000 | 3.619 |

_Measured voltage across components_
|Component|Voltage Across - Switch On (V)| Voltage Across - Switch Off (V) |
|---|---|---|
|R1|  3.006 | 0.000 |
|LED1| 1.994   | 0.033 |
|S1|  0.002  | 0.000 |

_Measured current_
|Resistor|Current Through - Switch On (mA)| Current Through - Switch Off (mA) |
|---|---|---|
|LED1|  11.12 | 0.000 |


##### Measurements on a circuit with an LED connected through a transistor


![Figure 4](https://github.com/aashikauppala/BAE305lab3/blob/main/Lab%203%20Figure%204.png)

_Measured voltage at each point with respect to ground (T4)_
|Test Point|Voltage - Switch On (V)| Voltage - Switch Off (V) |
|---|---|---|
|T2|  1.995 | 4.997 |
|T3 (VCE)| 0.021 | 3.613 |
|T5 (VBE)|  0.694 | 0.001 |
|T6| 5.003 | 0.010 |

_Measured voltage across components_
|Component|Voltage Across - Switch On (V)| Voltage Across - Switch Off (V) |
|---|---|---|
|R1|  2.999 | 0.000 |
|LED1| 1.979   | 1.384 |
|R2|  4.306  | 0.000 |
|S1|  0.000  | 5.000 |

_Measured current_
|Resistor|Current Through - Switch On (mA)| Current Through - Switch Off (mA) |
|---|---|---|
|LED1 (IC)|  10.89 | 0.010 |
|R2 (IB)|  4.350 | 0.000 |


##### Controlling LED current through a transistor


![Figure 5](https://github.com/aashikauppala/BAE305lab3/blob/main/Lab%203%20Figure%205.png)

_Measured voltage at each point with respect to ground (T4)_
|Test Point|Voltage - Dim LED (V)| Voltage - Midpoint 1 (V) | Voltage - Midpoint 2 (V) | Voltage - Bright LED (V) |
|---|---|---|---|---|
|T2|  4.920 | 4.728 | 4.255 | 1.937 |
|T3 (VCE)| 3.329 | 3.077 | 2.542 | 0.097 |
|T5 (VBE)|  0.530 | 0.562 | 0.587 | 0.628 |
|T6| 0.534 | 0.573 | 0.613 | 0.792 |

_Measured voltage across components_
|Component|Voltage - Dim LED (V)| Voltage - Midpoint 1 (V) | Voltage - Midpoint 2 (V) | Voltage - Bright LED (V) |
|---|---|---|---|---|
|R1|  0.076 | 0.268 | 0.729 | 3.056 |
|LED1| 1.592   | 1.652 | 1.713 | 1.838 |
|R2|  0.003  | 0.011 | 0.026 | 0.162 |


_Measured current_
|Resistor|Current Through - Dim LED (mA)| Current Through - Midpoint 1 (mA) | Current Through - Midpoint 2 (mA) | Current Through - Bright LED (mA) |
|---|---|---|---|---|
|LED1 (IC)|  0.04 | 1.02 | 2.79 | 11.29 |
|R2 (IB)|  0.02 | 0.03 | 0.04 | 0.18 |
|Gain (IC/IB)|  2 | 34 | 69.75 | 62.7 |


#### Part 2 - Motor Driving Circuit
##### Controlling motor current and speed using a transistor


![Figure 6](https://github.com/aashikauppala/BAE305lab3/blob/main/Lab%203%20Figure%206.png)

_Measured voltage at each point with respect to ground (T4)_
|Test Point|Voltage - Slow Motor (V)| Voltage - Midpoint 1 (V) | Voltage - Midpoint 2 (V) | Voltage - Fast Motor (V) |
|---|---|---|---|---|
|T2|  4.920 | 4.728 | 4.255 | 1.937 |
|T3 (VCE)| 3.329 | 3.077 | 2.542 | 0.097 |
|T5 (VBE)|  0.530 | 0.562 | 0.587 | 0.628 |
|T6| 0.534 | 0.573 | 0.613 | 0.792 |

_Measured voltage across components_
|Component|Voltage - Slow Motor (V)| Voltage - Midpoint 1 (V) | Voltage - Midpoint 2 (V) | Voltage - Fast Motor (V) |
|---|---|---|---|---|
|R1|  0.076 | 0.268 | 0.729 | 3.056 |
|LED1| 1.592   | 1.652 | 1.713 | 1.838 |
|R2|  0.003  | 0.011 | 0.026 | 0.162 |


_Measured current_
|Resistor|Current Through - Slow Motor (mA)| Current Through - Midpoint 1 (mA) | Current Through - Midpoint 2 (mA) | Current Through - Fast Motor (mA) |
|---|---|---|---|---|
|LED1 (IC)|  0.04 | 1.02 | 2.79 | 11.29 |
|R2 (IB)|  0.02 | 0.03 | 0.04 | 0.18 |
|Gain (IC/IB)|  2 | 34 | 69.75 | 62.7 |



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
