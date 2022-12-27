# Altium_Tutorial_Project ⚡🖥️
The following files were completed as a part of the Altium free PCB design course. Project A - A Power Regulator and LED Board. The PCB design course can be found at the following link below
* [Altium Education Courses](https://education.altium.com/)

This project goes over all the material covered in this course which includes
* Schematics & Libraries
* PCB Layout
* Routing & Basic Signal Integrity
* PCB Manufacturing

## Functional Requirements

<img width="384" alt="image" align = 'Right' src="https://user-images.githubusercontent.com/73625971/209628494-6ed77d6c-a733-4575-81ec-dead882f790e.png">

The primary goal of this project was to design a power regulator shield board for the Arduino Uno that powers a bank of LEDs as well as the Arduino Uno. The design of the board had to meet the following set of requirements:

1. Receive power from a 12 V DC input
2. Regulate power down to 5 V DC
3. Deliver 12 V DC power to a bank of 2 LED lights in parallel
4. Provide 5 V DC power to the main Arduino Uno board
5. Provide enough current to power the Arduino and the LEDs
6. Regulate power with at least 90% efficiency
7. LEDs must be SMD parts with high power output (at least 10 W each)
8. Power input connection is provided by standard 16 AWG wire
9. Components must be placed only on the top layer
10. Total board thickness must be standard thickness (approximately 62 mils)

When designing the board shape I referenced the Arduino.cc website [See this link](https://store-usa.arduino.cc/products/arduino-uno-rev3/?selectedStore=us)

## Creating the schematics
When designing the schematics there were a couple components that required external libraries.

|   **Part number**  | **Quantity** | **Description** | **Where To Find** |
| ------------- |:-------------:|:-------------:|:-------------:|
| SSQ-108-03-T-S| 2            | 8-pin header | [Link](https://www.samtec.com/products/ssq-108-03-t-s)| 
| SSQ-106-03-T-S| 1            | 6-pin header | [Link](https://www.samtec.com/products/ssq-106-03-t-s)| 
| SSQ-110-03-T-S| 1            | 10-pin header | [Link](https://www.samtec.com/products/ssq-110-03-t-s)| 

The rest of the parts including the LEDs (MKRAWT-00-0000-0D0HG235H) can be directly placed from the manufacturer's part search.

The power regulator design was made using the [WeBench platform](https://webench.ti.com/power-designer/) with the following requirements:
* Vin Min: 12 V 
* Vin Max: 12 V 
* Vout: 5 V 
* Iout Max: 1 A
This porject used the TPS562200 regulator design.

## PCB layout
Details related to the PCB layout & Stackup layout can be found in the output files above

## Output files
The following output files were included
* Bill of Materials
* Gerber
* NC Drill 
* Pick-and-place
* Board Stackup
* Drill Drawing/Guides
* Schematic Prints
* PCB prints
