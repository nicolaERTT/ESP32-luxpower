# ESP32-luxpower
Connect inverter luxpower on RS-485 to ESP32 and ESPHOME

I completely bypassed the dongle issue by connecting a MAX485 and then an ESP32 to the Luxpower RJ-45 port, so I have my data locally without any problems and without having to rely on third-party Wi-Fi.

![PINOUT ESP32 LUX](https://github.com/user-attachments/assets/f36752d9-c978-4640-bb37-68654d0fe279)
https://github.com/nicolaERTT/ESP32-luxpower/blob/main/PINOUT%20ESP32%20LUX.jpg

I set up the ESP32 with HA's ESPHOME firmware (easy to use via the web GUI), then loaded the LuxPower MODBUS instructions.

![TABLE MODBUS](https://github.com/user-attachments/assets/995531ef-e892-45fa-9a34-43aa97b4a366)
https://github.com/nicolaERTT/ESP32-luxpower/blob/main/Luxpower%20table%20modbus%20address.pdf
