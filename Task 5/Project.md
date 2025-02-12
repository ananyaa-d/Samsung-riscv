# Security alarm system
## Overview:
This application uses a IR sensor to detect movement and sends an alert via attached buzzer when motion is detected.
## Features
Motion Detection: Uses a IR sensor to detect movement.\
Alert System: Triggers a buzzer.\
Low Power: Designed for energy-efficient operation.
## Components Required:
RISC-V Processor: A 32-bit RISC-V microcontroller (e.g., SiFive HiFive1).\
IR Sensor: Detects infrared radiation changes caused by movement.\
Buzzer/LED: Provides audible or visual alerts.
## Steps to Implement
### 1.Set Up the IR Sensor
Connect the IR sensor's VCC and GND pins to the 3.3V and GND of the RISC-V processor.\
Connect the IR sensor's OUT pin to a GPIO pin (e.g., D0).
### 2.Add Alerts
Connect a buzzer to another GPIO pin (e.g., D1) with a transistor to amplify the signal.
