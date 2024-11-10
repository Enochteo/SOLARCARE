# SOLARCARE
SOLAR TRACKER/MONITORING STATION

This is a hardware hack that leverages Arduino technology to improve the efficiency of solar panels. It aligns the panels with the motion of sunlight and monitors them to keep them at a cool and safe temperature.

Description: The device uses two Light-Detecting resistors to determine the relative difference in light intensity on opposite sides of a panel. It also uses a servo motor that rotates according to that difference in light intensity, a DHT11 sensor that measures both temperature and relative humidity on the panel's surface to maintain them and notify the user of extreme weather conditions, and an Arduino.

# Components:
- Arduino Uno
- 2 light detecting resistors
- Servo motor
- Solar panel
- DHT 11 temperature sensor
- Jumper wires
- Breadboard

# Circuit Diagram![SOLACARE SCHEMATICS](https://github.com/user-attachments/assets/da29aaaf-07f2-41a0-a1ff-a35ec693b370)

How it works:
- The two LDRs act as light sensors. Each LDR detects the intensity of sunlight falling on it. When the sunlight intensity is high, the LDR's resistance decreases, which increases the voltage at the analog input pin on the Arduino.
The Arduino reads the voltage values from both LDRs, which indicates the relative amount of light each LDR receives.
- The code compares the readings from the two LDRs. If there is a significant difference between the two readings, it means that one LDR is receiving more light than the other.
This difference tells the Arduino the direction in which the light source is positioned relative to the current orientation of the servo.
- Based on the light difference, the servo motor adjusts the position of the solar panel or surface.
If the left LDR has more light, the servo rotates left. If the right LDR has more light, the servo rotates right. The servo keeps adjusting until the two LDRs detect similar light levels, which means the panel is aligned with the light source.
This process repeats throughout the day, so the solar panel always points toward the strongest light source, maximizing sunlight exposure and, potentially, the panel’s energy generation.

Also, the DHT11 contains a thermistor (temperature sensor) that transmits both temperature and Relative Humidity values to the Arduino and could be read on a Serial monitor or cloud server.

Power: The circuit runs on 5Volts from the Arduino.

# Conclusion 
This project combines sensors, a microcontroller, and communication with a serial monitor which would later become an application or cloud server, to create interactive, automated systems that respond to environmental changes, enhancing the functionality and sustainability of renewable energy sources, and enhanced sustainability through data-driven adjustments.



