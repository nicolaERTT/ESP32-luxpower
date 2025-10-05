# ESP32-luxpower
Connect inverter luxpower on RS-485 to ESP32 and ESPHOME

I completely bypassed the dongle issue by connecting a MAX485 and then an ESP32 to the Luxpower RJ-45 port, so I have my data locally without any problems and without having to rely on third-party Wi-Fi.

https://github.com/nicolaERTT/ESP32-luxpower/blob/main/PINOUT%20ESP32%20LUX.jpg
![PINOUT ESP32 LUX](https://github.com/user-attachments/assets/f36752d9-c978-4640-bb37-68654d0fe279)

I set up the ESP32 with HA's ESPHOME firmware (easy to use via the web GUI), then loaded the LuxPower MODBUS instructions.

InputAddr Item Unit Range Note 

1 Vpv1 0.1V 0-65535 PV1voltage,theACenergystorage 
systemdoesnothavethisvariable 
2 Vpv2 0.1V 0-65535 PV2voltage,theACenergystorage 
systemdoesnothavethisvariable 
3 Vpv3 ​​0.1V 0-65536 PV3voltage, theACenergystorage 
systemdoesnothavethisvariable 
4 Vbat 0.1V 0-65535 Batteryvoltage 
5 SOC % 0-100 Batterycapacity 
SOH % 0-100 BatteryStateofhealth 
6 InternalFault 0-65535 Formoreinformation,seeInternal 
FaultCodeDefinitionfile 
7 Ppv1 W 0-65535 PV1power/ACenergystoragePpv 
8 Ppv2 W 0-65535 PV2power,theACenergystorage

etc....
