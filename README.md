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


Dallas:
  You can actually connect multiple sensors to a single pin and use them all at once.
  4x ds18b20 will be connect to pin23 of ESP32
  
PT100:
  https://esphome.io/components/sensor/max31865.html
  - VIN connects to 5V (3V3 will output 3.3V), or directly connect 3V3 to 3.3V
  - 3Vo is not used by ESPHome
  - GND connects to ground
  - CLK connects to the SPI clk_pin   / GPIO6
  - SDO connects to the SPI miso_pin  / GPIO7 
  - SDI connects to the SPI mosi_pin  / GPIO8
  - CS connects to a free GPIO pin    / GPIO17
  - RDY is not used by ESPHome
