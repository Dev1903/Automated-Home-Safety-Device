# Automated-Home-Safety-Device

This project is a comprehensive home safety monitoring system that utilizes the ESP8266 microcontroller to monitor gas levels, smoke, and fire inside a house. It provides live updates to the Blynk app and performs various actions based on sensor readings.

## Features

- **Gas Detection:** Monitors LPG, CO, and smoke levels using an MQ2 sensor.
- **Fire Detection:** Detects fire using a combination of temperature and flame sensors.
- **Live Updates:** Sends live sensor data to the Blynk app.
- **Automated Actions:**
  - Activates a motor to open a window if gas levels exceed the threshold.
  - Opens a door using a servo motor if gas levels exceed the threshold.
  - Sends notifications and emails if fire is detected.

## Components

- **ESP8266**: Microcontroller for processing sensor data and communicating with the Blynk app.
- **MQ2 Sensor**: Detects LPG, CO, and smoke levels.
- **Flame Sensor**: Detects the presence of flame.
- **Temperature Sensor**: Measures the temperature to assist in fire detection.
- **Motor**: Controls the opening of a window.
- **Servo Motor**: Controls the opening of a door.

## Circuit Diagram

### Pin Connections

- **MQ2 Sensor**: Analog pin A0
- **Flame Sensor**: Digital pin D1
- **Temperature Sensor**: Analog pin A1
- **Motor**: Digital pin D2
- **Servo Motor**: Digital pin D3

## Software Setup

### Libraries Required

- **ESP8266WiFi.h**
- **BlynkSimpleEsp8266.h**
- **Servo.h**

### Blynk App Setup

1. Create a new project in the Blynk app.
2. Add a Value Display widget to monitor the MQ2 sensor readings.
3. Add Notification and Email widgets for alerts.
4. Note down the Blynk authorization token.

### Arduino Code

1. Include the necessary libraries.
2. Define your WiFi credentials and Blynk authorization token.
3. Set up pin configurations for the sensors, motor, and servo.
4. Implement logic to:
   - Monitor gas levels and send live data to the Blynk app.
   - Activate motor and open the door if gas levels exceed the threshold.
   - Detect fire using temperature and flame sensors and send notifications and emails.

### Adjustments

- **Thresholds:** Adjust the threshold values for the MQ2, flame, and temperature sensors based on your specific sensor readings to ensure accurate detection.
- **Live Feed:** Ensure you have set up a widget in the Blynk app to display the MQ2 sensor value.

## Usage

1. Connect all components as per the pin connections.
2. Upload the Arduino code to the ESP8266.
3. Monitor the live feed and alerts on the Blynk app.
4. Ensure automated actions (opening windows and doors) work correctly when sensor thresholds are exceeded.
