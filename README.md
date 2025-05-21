# ESP32WIFI-LIGHTSENSOR

Using ESP32

lightsensor used: https://wiki.dfrobot.com/DFRobot_Ambient_Light_Sensor_SKU_DFR0026?gad_source=1&gad_campaignid=834127384&gbraid=0AAAAADucPlB86-uzc1IMnlQTzuwzvVIlH&gclid=EAIaIQobChMIgJzd1dWzjQMVsqVmAh0yOzg0EAAYASAAEgL9dfD_BwE

Hardware set-up
- ESP32_3V3 --> Light sensor 'VCC' wire (red) 
- ESP32_GND (Next to 3V3) --> Light sensor 'GND' wire (black)
- ESP32_D34 (Opp side of 3V3 and GND) --> Light sensor 'S' wire (Green)

Software set-up
- arduino ide with esp32 expressif installed
- IDE: Tools > Board > ESP32 Arduino > ESP32 Dev Module
- Enter phone hotspot ssid and password in code. Placeholder is 'ABCD'
- Using Coolterm, Use TCP port, use the initial output from serial monitor to get IP and port number

During initial upload, ESP32 will be connected to computer. Get IP and port number by opening serial monitor and check it can connect with mobile data

For iphone: ENSURE maximise compatibility is turned on (IMPORTANT, forces mobile data to use 2.4 GHz, will not work otherwise)

Once you have unplug from computer and plug into powerbank, ensure that computer is connected to hotspot, you may wish to press EN button once to restart the code.

esp32 and computer should now be connected via mobile data

On coolterm, connect to the tcp port that you set-up based on your IP and port. 
- go to connection > file capture > start
- press connect in the UI when ready.
- disconnect to stop data collection, go back to file capture to press stop

The data should be saved in a textfile which you can import into sheets to edit accordingly to get lux-time.

Troubleshooting: press EN button on ESP32, chatgpt

Some of the data, when imported into sheets, may be missing and may not be logical, edit the data accordingly to get clean data.

