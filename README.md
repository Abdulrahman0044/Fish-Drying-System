# Fish-Pond-System
# Dryer Monitor System

This project implements a Dryer Monitor System using an Arduino-based microcontroller. The system monitors and logs environmental data, including temperature, humidity, wind speed, and smoke levels, while providing alerts when thresholds are exceeded. 

## Features
- **Temperature Monitoring**: Reads data from a DHT11 sensor and triggers an alarm when temperature exceeds a predefined threshold.
- **Humidity Monitoring**: Displays real-time humidity levels.
- **Smoke Detection**: Detects smoke levels using an MQ-2 sensor and triggers a buzzer if smoke is detected.
- **Wind Speed Measurement**: Reads wind speed data from an analog sensor.
- **Data Logging**: Logs data to an SD card with timestamps from an RTC (Real-Time Clock).
- **Visual Feedback**: Displays temperature and humidity data on an I2C-connected LCD.
- **Alarm System**: Activates a buzzer and controls a relay for safety measures.

## Hardware Components
- Arduino Microcontroller
- DHT11 Temperature and Humidity Sensor
- MQ-2 Smoke Sensor
- Wind Speed Sensor (Analog)
- LiquidCrystal I2C LCD Display
- DS1302 RTC Module
- Buzzer
- Relay
- SD Card Module
- Miscellaneous: Resistors, jumper wires, breadboard, power supply

## Software Requirements
- Arduino IDE (v1.8.0 or later)
- Libraries:
  - `Wire`
  - `LiquidCrystal_I2C`
  - `hd44780`
  - `Bonezegei_DHT11`
  - `SD`
  - `SPI`
  - `TimeLib`
  - `Ds1302`

## Setup Instructions
1. **Hardware Assembly**:
   - Connect the sensors and modules to the Arduino as per the pin configurations defined in the code.
   - Ensure the SD card is properly inserted in the SD card module.

2. **Software Configuration**:
   - Install the required libraries via the Arduino IDE Library Manager.
   - Upload the code to the Arduino board.

3. **Testing and Usage**:
   - Power on the system.
   - The LCD will display introductory text and switch to monitoring mode.
   - Monitored data will be displayed on the LCD and logged to the SD card.
   - Alarms (buzzer and relay) will activate if thresholds are exceeded.

## Pin Configuration
| Component            | Arduino Pin | Description                        |
|-----------------------|-------------|------------------------------------|
| DHT11 Sensor          | 9           | Temperature and Humidity Data Pin |
| MQ-2 Sensor           | A0          | Smoke Detection Analog Pin        |
| Wind Speed Sensor     | A1          | Wind Speed Analog Pin             |
| Buzzer                | 7           | Buzzer Control Pin                |
| Relay                 | 6           | Relay Control Pin                 |
| SD Card Module (CS)   | 4           | SD Card Chip Select Pin           |
| RTC (DS1302)          | A4 (Data), A5 (RST), 2 (CLK) | Real-Time Clock Module |

## How It Works
1. **Initialization**:
   - The system initializes the LCD, sensors, RTC, and SD card.
   - Displays introductory messages on the LCD.

2. **Monitoring**:
   - Reads temperature and humidity from the DHT11 sensor.
   - Measures wind speed and smoke levels.
   - Logs data to the SD card with timestamps.

3. **Alert System**:
   - Activates the buzzer and relay if temperature or smoke exceeds defined thresholds.

## Authors
- Abdulrahman Abdulrahman
abdulrahamanbabatunde12@gmail.com

## License
This project is open-source and available for educational and non-commercial use. Modify and improve it as needed.

## Acknowledgments
Special thanks to the Arduino community and library contributors for enabling such projects.
