# IOT-DATA-LOGGER-WITH-THRESHOLD-VIOLATION-DETECTION
This IoT-based data logger monitors temperature and humidity using a DHT11 sensor and LPC2148 microcontroller. It alerts users via buzzer when thresholds are exceeded, logs data, and uploads values to ThingSpeak. Setpoints are stored in EEPROM and can be updated locally via keypad or remotely via the cloud.

⚙️ HARDWRAE REQUIREMENTS:

1.LPC2148 : The main controller for the project.
2.DHT11 : For reading temperature and humidity data.
3.AT24C256 : For storing and retrieving the set points for temperature and humidity.
4.4x4 MATRIX KEYPAD : To allow user input for changing set points.
5.SWITCH : For triggering interrupt-based changes in set points.
6.LCD : To display data from sensors and system status.
7.BUZZER : For alerting when threshold violations occur.
8.WI-FI MODULE (ESP01): To send data to the Thingspeak cloud for remote monitoring.
9.DB-9 CABLE/USB-UART CONVERTER : To interface with UART for communication.

💾 SOFTWARE REQUIREMENTS:

1.KEIL C Compiler : For embedded C programming.
2.PROGRAMMING IN EMBEDDED C :The primary programming language for LPC2148.
3.Flash Magic:To load the program onto the LPC2148.

🏗️ SYSTEM ARCHITECTURE: 
  ![image](https://github.com/user-attachments/assets/0b6ee6a4-61b3-4b35-ba83-d123fda940c0)



🔑 KEY FEATURES:

* Real-time environmental monitoring
* EEPROM-based persistent storage of threshold values
* Alerts using buzzer on threshold violation
* Cloud integration with Thingspeak for data logging
* Remote configuration via cloud and local keypad

🔁 WORKING PRINCIPLE: The system initializes all peripherals (LCD, DHT11, EEPROM, ESP01, keypad, and buzzer).

* Setpoints are read from EEPROM during startup.
* The DHT11 sensor continuously measures temperature and humidity.
* These values are compared with the setpoints, and if a threshold is violated:
   I The current value is sent to the Thingspeak cloud.
  II The buzzer is activated with timed ON/OFF cycles to alert nearby personnel.
* Every 3 to 5 minutes, the system fetches the latest setpoints from the Thingspeak cloud.
* If the new setpoint differs from the current EEPROM value, the EEPROM is updated.
* If a local interrupt is triggered, the user can manually update setpoints using the keypad.

✅ APPLICATIONS AND USE CASES:

1. Industrial Monitoring 🏭: Used in manufacturing plants or warehouses to monitor temperature and humidity for storage conditions, especially in environments like pharmaceutical storage, food preservation, and electronic equipment storage.
2. Environmental Monitoring🌡️💧☁️: Can be used for monitoring conditions in agricultural greenhouses, laboratories, or research environments where precise control over temperature and humidity is critical.
3. Smart Home Automation🏠📱⚙️: The system can be integrated into a smart home setup to monitor and control environmental parameters, ensuring comfort and energy efficiency.

🚀🧠FUTURE ENHANCEMENTS:

* Additional Sensors (Air Quality, Pressure, etc.)
* Mobile App Integration
* Improved Alert System (SMS, Push Notifications)
* Data Analytics and Visualization
* AI and Machine Learning for Predictive Maintenance

📝📌CONCLUSION: This IoT Data Logger with Threshold Violation Detection offers real-time monitoring, local and remote alerting, and continuous cloud integration for enhanced visibility. By providing user-friendly setpoint modification, cloud-based monitoring, and real-time feedback, this system has vast potential in various industries and environments where parameter control is essential for safety, comfort, or operational efficiency.
