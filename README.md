# MultiProbe-Arduino
Arduino based temperature surface monitor

# Hardware
* 5 Thermocouples
* AREF pull up resistor
* Push Button
* Debounce resistor
* LCD
* Potentiometer
* Arduino Module


# State Machine
* Initialize
* Scan Channels
* Idle
* Settings
* DAQ
* Error

#Intialize

Purpose: To configure the Arduino I/O and setup the serial communication protocol

# Scan Channels

Purpose: To scan all the thermocouple channels and to determine which ones are connected and ready for use and which ones are not.

# Idle

Purpose: Waits for a button press or serial command to trigger a state change.  Possible next states are scan channel, settings or DAQ.

# Settings

Purpose: The settings for the DAQ.  This includes the type of averaging, average sample size, average frequency and units.

# DAQ

Purpose: This gets the thermocouple data, converts it to data, updates the display and sends the result over serial communication. 

# Error

Purpose: To catch errors and update the user on the controller status.
