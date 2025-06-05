# HuskyLens Face Recognition Relay Control

This Arduino project uses a [HuskyLens module](https://www.huskylens.com/) to control a relay based on face recognition. The relay unlocks when an authorized face (ID 1 or 2) is detected and locks when the face is no longer present, with a 5-second cooldown to prevent rapid toggling.

## Table of Contents
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Wiring](#wiring)
- [Installation](#installation)
- [Usage](#usage)
- [Code Overview](#code-overview)
- [Serial Output](#serial-output)
- [Configuration](#configuration)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Hardware Requirements
- Arduino board (e.g., Arduino Uno)
- HuskyLens module (I2C protocol enabled)
- Relay module (5V compatible)
- Jumper wires
- USB cable for Arduino

## Software Requirements
- [Arduino IDE](https://www.arduino.cc/en/software)
- [HUSKYLENS Arduino Library](https://github.com/HuskyLens/HUSKYLENSArduino) (install via Arduino Library Manager)
- Wire library (included with Arduino IDE)

## Wiring
| HuskyLens | Arduino  | Relay    |
|-----------|----------|----------|
| VCC       | 5V       | VCC      |
| GND       | GND      | GND      |
| SDA       | SDA (A4) |          |
| SCL       | SCL (A5) |          |
|           | Pin 3    | IN/SIG   |

1. Connect HuskyLens to Arduino via I2C (SDA to A4, SCL to A5, VCC to 5V, GND to GND).
2. Connect the relay signal pin to Arduino digital pin 3, with VCC and GND connected.
3. Set HuskyLens to I2C protocol (General Settings > Protocol Type > I2C).

## Installation
1. **Install Arduino IDE**: Download and install from [arduino.cc](https://www.arduino.cc/en/software).
2. **Install HUSKYLENS Library**:
   - In Arduino IDE, go to `Sketch > Include Library > Manage Libraries`.
   - Search for "HUSKYLENS" and install.
3. **Clone or Download Repository**:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
