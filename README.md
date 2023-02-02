# Solarstation-ESPHome
Solarstation für Solarthermie mit ESP32, ESPHome, HomeAssistant

Komponenten: 
  1. ESP32
  2. LED oder OLED Display
  3. Integration mit HomeAssistant
  4. Gehäuse (3D-Druck?)


Input: 
  1. 4x TemperaturSensor ds18b20
  2. 2x PT100 
  3. Setting for delta, Wlan, Language
  
Output:
  1. Pumpe Solar
  2. Pumpe Circulation
  3. LED


  You can actually connect multiple sensors to a single pin and use them all at once.
  4x ds18b20 will be connect to pin23 of ESP32
  
