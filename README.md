# Hydrobotics

# Smart Hydroponic System with IoT

## Overview

This project is a smart hydroponic system for urban farming, which integrates various sensors and actuators with an ESP32 WROOM DA module. The system provides real-time monitoring and control through the Arduino IoT Cloud, enabling users to track environmental conditions and manage the water pump remotely.

## Features

- Temperature & Humidity Monitoring: Uses a DHT11 sensor to measure air temperature and humidity.
- Water Temperature Measurement: Uses a DS18B20 sensor to monitor water temperature.
- Light Intensity Control: Uses an LDR sensor module to detect light levels and automatically control a grow light.
- Automated Water Pump Control: Users can remotely turn the water pump on/off through the Arduino IoT Cloud interface.
- Relay Module Integration: Controls the water pump and grow light based on sensor readings.
- ESP32 WROOM DA Module: Manages all sensors and actuators while connecting to the cloud for IoT functionality.

## Components Used

- ESP32 WROOM DA Module
- DHT11 Sensor (Temperature & Humidity)
- DS18B20 Sensor (Water Temperature)
- LDR Sensor Module (Light Intensity Detection)
- Grow Light
- Water Pump
- Relay Module
- Arduino IoT Cloud for User Interface

## Circuit Connections

| Component           | ESP32 Pin |
|--------------------|----------|
| DHT11 Sensor      | 26       |
| DS18B20 Sensor    | 32       |
| LDR Sensor        | 34       |
| Water Pump (Relay)| 12       |
| Grow Light (Relay)| 14       |

## Code Explanation

1. Sensor Initialization: The DHT11 and DS18B20 sensors are initialized in `setup()`.
2. Data Collection: Sensor readings for temperature, humidity, and water temperature are gathered in `loop()`.
3. Light Control: If the LDR reading is greater than 800, the grow light turns ON; otherwise, it remains OFF.
4. Water Pump Control: The user can turn the water pump ON/OFF via the Arduino IoT Cloud interface.
5. Cloud Integration: Sensor readings are updated on the cloud, and user commands are processed.

## Installation & Usage

1. Install Arduino IDE and required libraries:
   - `DHT.h`
   - `OneWire.h`
   - `DallasTemperature.h`
2. Connect the ESP32 to your computer and upload the Arduino sketch.
3. Link the ESP32 to the Arduino IoT Cloud.
4. Power on the system.
5. Monitor and control the system via the Arduino IoT Cloud Dashboard.

## How It Works

- When the system is powered on, DHT11, DS18B20, LDR, and the water pump are initialized.
- The LDR sensor checks light intensity and controls the grow light accordingly.
- The temperature and humidity values are displayed on the Arduino IoT Cloud Dashboard.
- Users can manually control the water pump from the interface.

## Future Improvements

- Add pH and EC sensors for better nutrient management.
- Implement automated nutrient dosing based on sensor readings.
- Develop a mobile app interface for better user experience.


