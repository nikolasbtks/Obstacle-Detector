# Obstacle-Detector

## Description

This project demonstrates an obstacle detector system, that uses an SRF05 Ultrasonic Sensor to identify nearby objects and indicate their presence using LEDs.

Based on FreeRTOS library, the project implements two tasks:
1. Distance Calculation
    - The SRF05 emits ultrasonic waves and calculates the distance to the nearest object.

2. LED Control and Data Processing
    - If the distance is less than 20 cm, the Red LED lights up. If there is no detection of an obstacle , the Green LED lights up.

A queue is used to transfer data from one task to another.

## Hardware Requirements and Circuit Schematic 

Below is a list of all the necessary components required for this project:

| Components        | Description       | Quantity        |
|----------------|-------------------|----------------|
|     Board     |     STM32 NUCLEO-F446RE     |     1     |
| Ultrasonic Sensor   |     HC-SRF05     |     1     |
| BreadBoard   | Standard solderless breadBoard | 1 |
| Jumper Wires   | Male-to-Male | As needed |
| LEDs   | Standard 5mm LEDs (Green, Red) | 2 |
| Resistors   | 100Ω (for LEDs) | 2 |
| Power Supply   | 5V via USB | 1 |

A detailed circuit schematic is also provided. This schematic show the connections between the components.

photo

- The LEDs are connected via 100Ω resistors to GPIO PA1 and PA4.
- The HC-SRF05 sensor has a 5V power supply, the Echo pin is connected to GPIO PA9, the Trig pin is connected to GPIO PA8 and the Out pin is not used.

## How to install and run this project ?
If you wish to test it, you need to download the entire project from GitHub. Then, setup the STM32CubeIDE and open the application files you've downloaded.
