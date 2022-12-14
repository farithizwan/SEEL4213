## Brave Lynx
### PROBLEM STATEMENT
- This causes the loss of life due to the delay in the arrival of ambulance to the accident spot or from the accident spot to the hospital. So, the system is use to monitor the data from sensor to make a emergency alert in the system.

### SYSTEM ARCHITECTURE
- Sensor
IR sensor, Accelerometer, Gyro
- Cloud Platform
Django Rest Framework and Python Everywhere 
- Dashboard
Grafana

![Sensor   Device](https://user-images.githubusercontent.com/118268884/207471163-ebc28b07-bd37-409c-be45-090c10b01415.png)

### SENSOR
- NodeMCU ESP32 using HTTP protocol
- Gyroscope sensor use to measure the orientation of the crush detection device
- Accerometer sensor use to measure the acceleration of the vehicle

## CLOUD PLATFORM
- All data from the sensor will transfer throught HTTPS protocol to Django Rest Framework.
- After that, the data will pass to python everywhere

## DASHBOARD
In the dashboard, user can monitor the orientation of the gyroscope, the data from the accelerometer and the risk to accident. User also can
monitor the false alert that trigger by the device. If there are many false alert in the table in one day, that means the driver is very reckless
in driving. 
![Screenshot 2022-12-14 082915](https://user-images.githubusercontent.com/118268884/207474805-9bff2810-ade5-4bbc-be02-3bfcc1b782ac.jpg)
