# Data Collection for Robust Human Activity Recognition

Android app for Data Collection
---------------------

The aim of the Data Collection App for Robust Human Activity is to record study participants while they conduct certain activities: lying down, standing, walking, ascending stairs, descending stairs, running and cycling.
During these activities, the participants are equipped with the Respeck sensor, an accelerometer and Gyroscope, which is placed on the left side of the abdomen just below the rip cage.


BLE Transmission Information
----------------

Bluetooth Low Energy (BLE) provides a cheap and reliable way for low power devices to communicate. Devices advertise one of more services, which themselves contain a number of characteristics. For example a heart rate monitor may provide a service which contains a characteristic which will send the current pulse rate. Characteristics can either be readable, writable or allow notifications, which means that new data will be streamed over BLE when it is available. This is the mode that I use to send accelerometer and gyroscope data from the Respeck device to the Data Collection app.

Gyroscope and accelerometer data are packed into an 18 byte packet, where each axis of each sensor requires 2 bytes to send a 16 bit value.
