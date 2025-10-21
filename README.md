# ESP32-luxpower
Connect inverter luxpower on RS-485 to ESP32 and ESPHOME

I completely bypassed the dongle issue by connecting a MAX485 and then an ESP32 to the Luxpower RJ-45 port, so I have my data locally without any problems and without having to rely on third-party Wi-Fi.

![PINOUT ESP32 LUX](https://github.com/user-attachments/assets/f36752d9-c978-4640-bb37-68654d0fe279)
https://github.com/nicolaERTT/ESP32-luxpower/blob/main/PINOUT%20ESP32%20LUX.jpg

I set up the ESP32 with HA's ESPHOME firmware (easy to use via the web GUI), then loaded the LuxPower MODBUS instructions.

![TABLE MODBUS](https://github.com/user-attachments/assets/995531ef-e892-45fa-9a34-43aa97b4a366)
https://github.com/nicolaERTT/ESP32-luxpower/blob/main/Luxpower%20table%20modbus%20address.pdf


 I use Port RJ-45 to connect MAX485 RS485 converter to Luxpower

 ![Port RJ-45 luxpower](https://github.com/user-attachments/assets/2c4eb826-d27b-4405-90e2-1cd69a6b87dc)


**Finally, I've attached the YAML file I used ;** you need to enter your initial configuration values.

Obviously, the file only contains the sensors I'm interested in.

Note some tricks for sensors that I've never seen on the web: SOC, state_class, and device_class to then get the energy produced or consumed with the integrals.

https://github.com/nicolaERTT/ESP32-luxpower/blob/main/esp-luxp-demo.yaml


