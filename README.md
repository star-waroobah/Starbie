# Starbie

[![View PCB on KiCanvas](https://hack.club/pcb-badge)](https://kicanvas.org/?repo=https://github.com/star-waroobah/Starbie/tree/main/PCB)
A small star-shaped PCB desk pet built around a XIAO ESP32-C3, with an OLED screen, a motion sensor and a temperature sensor.

![3D view of the board](Assets/3d%20front.png)

## Why I made it
I made it as the week 1 project of half life hack club and I picked Starbie because it’s a small, fun project that combines a screen, sensors and buttons on one board. It was a great way to learn KiCad as a beginner using the guide :)

## How it works
The XIAO ESP32-C3 is the brain. It draws the pet on the OLED screen, reads the MPU6050 so the pet reacts when the board is tilted or shaken, reads the DHT11 for temperature and humidity, and reads two buttons for input.

## How the parts fit together
- **XIAO ESP32-C3 (U1):** the microcontroller. It powers everything from its 3V3 pin and GND.
- **OLED display (J1, 4-pin header):** pin 1 GND, pin 2 3.3V, pin 3 SCL (D5), pin 4 SDA (D4)
- **MPU6050 module (J2, 8-pin header):** pin 1 3.3V, pin 2 GND, pin 3 SCL (D5), pin 4 SDA (D4). It shares the I2C lines with the OLED. Pins 5 to 8 are unused.
- **DHT11 (U2):** data pin to D1. A 10k pull-up resistor (R1) connects the data line to 3.3V.
- **Button 1 (SW1):** connects D2 to GND
- **Button 2 (SW2):** connects D3 to GND
  
## Schematic
![Schematic](Assets/Schematic.png)

## PCB layout
![PCB layout](Assets/pcb%20layou.png)

## 3D model
![3D front](Assets/3d%20front.png)
![3D back](Assets/3d%20back.png)

## Repo files
- `PCB/` KiCad project files
- `production/` Gerber and drill files
- `Firmware/` Arduino code
- `Assets/` images
- `BOM.csv` parts list
