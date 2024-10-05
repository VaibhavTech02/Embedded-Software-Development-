# Embedded-Software-Development- 
1. Technologies Used :
Microcontroller: Arduino Nano
Bluetooth Communication: HC-05 Bluetooth Module
Relay Control: 4-Channel Relay Module
Android App: MIT App Inventor
Libraries: SoftwareSerial, EEPROM
App Files Provided: APK, AAB

2. Project Flow :
Component Setup and Circuit Design

Hardware Components:
Connected the Arduino Nano to the HC-05 Bluetooth module and the 4-Channel Relay Module.
Relays were wired to control different home appliances (lights, fans, etc.), with each relay connected to a separate digital pin.
Power supply and proper isolation for relays were ensured for smooth operation.
Pin Configuration:
Defined pin numbers for the relays in the Arduino code and assigned them as output pins to switch loads (appliances).
Pin configuration: Relay1 (Pin 4), Relay2 (Pin 5), Relay3 (Pin 6), Relay4 (Pin 7).
Arduino Code Implementation

EEPROM for Load Status:
Used EEPROM to store the status of each appliance, ensuring the system remembers their state even after a power reset.
Example: If a light was turned on before a power cut, it will remain on after reboot.
Bluetooth Communication:
Implemented serial communication between the Arduino and the Android app using the SoftwareSerial library.
Bluetooth commands from the app are received and interpreted by the Arduino to control the relays.
Power Management:
Controlled power for all appliances using a master command (bt_data == 'E' for OFF, bt_data == 'e' for ON).
Status Feedback:
The Arduino sends the status of each appliance back to the Android app for real-time monitoring.
Android App Development

MIT App Inventor:
Designed the app interface to control four appliances with buttons for manual control and an additional voice control feature for hands-free operation.
Used the Speech Recognizer component of MIT App Inventor to enable voice commands such as “Turn on light.”
App Files:
Provided APK and AAB files for the Android app, allowing easy installation and updates.
App Features:
Individual control buttons for appliances.
A status bar showing real-time load statuses, updated based on the communication with the Arduino.
Voice control functionality for users with mobility challenges. 
