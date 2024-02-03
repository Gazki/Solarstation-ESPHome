# Solarstation-ESPHome
Solarstation for Solarthermie with ESP32, ESPHome, HomeAssistant

Komponents: 
  1. ESP32 https://de.aliexpress.com/item/1005003413562394.html
  2. LED or OLED Display https://de.aliexpress.com/item/4000790549724.html
  3. Integration with HomeAssistant
  4. Case (3D-Print?)
  5. 2 Way Relay https://de.aliexpress.com/item/33038634587.html
  6. MAX31865 https://de.aliexpress.com/item/1005001351273869.html

Input: 
  1. 4x TemperaturSensor ds18b20	
  2. 2x PT100 
  3. Setting for delta, Wlan, Language
  
Output:
  1. Pumpe Solar        GPIO32
  2. Pumpe Circulation  GPIO33
  3. LED


Dallas:
  You can actually connect multiple sensors to a single pin and use them all at once.
  
  4x ds18b20 will be connect to ESP32: 
    - GPIO14
    - GPIO25
    - GPIO26
    - GPIO27
    
  Pinout description for a ESP-WROOM-32 see hier:
  https://www.studiopieters.nl/esp32-pinout/
    
  PT100 with MAX31865:
  https://esphome.io/components/sensor/max31865.html
  - VIN connects to 5V (3V3 will output 3.3V), or directly connect 3V3 to 3.3V
  - 3Vo is not used by ESPHome
  - GND connects to ground
  - CLK connects to the SPI clk_pin   / GPIO18    /GPIO6
  - SDO connects to the SPI miso_pin  / GPIO19    /GPIO7 
  - SDI connects to the SPI mosi_pin  / GPIO23    /GPIO8
  - CS connects to a free GPIO pin    / GPIO5     /GPIO17
  - RDY is not used by ESPHome

![Top](https://github.com/Gazki/Solarstation-ESPHome/blob/main/Images/2023-02-16%2012_46_46-EasyEDA(Standard)%20-%20A%20Simple%20and%20Powerful%20Electronic%20Circuit%20Design%20Tool.png)

![Top](https://github.com/Gazki/Solarstation-ESPHome/blob/main/Images/2023-02-10%2011_04_44-EasyEDA(Standard)%20-%20A%20Simple%20and%20Powerful%20Electronic%20Circuit%20Design%20Tool.png)


[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/J3J6IRJUR)
[![paypal](https://www.paypalobjects.com/webstatic/en_US/i/buttons/PP_logo_h_100x26.png)](https://paypal.me/Gazki)
