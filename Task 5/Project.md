# Smart Home Motion Detector with Alert System
## Overview:
This application uses a PIR (Passive Infrared) motion sensor to detect movement and sends an alert via UART or an attached buzzer when motion is detected. It can also control an LED or relay to simulate turning on a light or appliance.
## Features
Motion Detection: Uses a PIR sensor to detect movement.\
Alert System: Sends an alert via UART or triggers a buzzer.\
Control Outputs: Activates an LED or relay to simulate turning on a light or device.\
Low Power: Designed for energy-efficient operation.
## Components Required:
RISC-V Processor: A 32-bit RISC-V microcontroller (e.g., SiFive HiFive1).\
PIR Motion Sensor: Detects infrared radiation changes caused by movement.\
Buzzer/LED: Provides audible or visual alerts.\
UART: Sends motion detection status to a connected device.\
Relay Module: Controls appliances like lights or fans.
## Steps to Implement
### 1.Set Up the PIR Sensor
Connect the PIR sensor's VCC and GND pins to the 3.3V and GND of the RISC-V processor.\
Connect the PIR sensor's OUT pin to a GPIO pin (e.g., D0).
### 2.Configure UART
Connect the processor's UART TX pin to a USB-to-serial converter for debugging.
### 3.Add Alerts
Connect an LED to a GPIO pin (e.g., D1) with a current-limiting resistor (220 Ω).\
Connect a buzzer to another GPIO pin (e.g., D2) with a transistor to amplify the signal.
### 4.Relay for Appliance Control 
Use a relay module connected to a GPIO pin (e.g., D3) to control a light or fan.
