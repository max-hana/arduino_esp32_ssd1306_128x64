# arduino_esp32_ssd1306_128x64

- This is a quick project starter for ESP32 with SSD1306 OLED modules.

## installation instruction
- Add esp32 tool chain to your Arduino IDE.
  [github.com/espressif/arduino-esp32](https://github.com/espressif/arduino-esp32)

- Add "Adafruit-GFX-Library" to your libraries folder.
[github.com/adafruit/Adafruit-GFX-Library](https://github.com/adafruit/Adafruit-GFX-Library)

- Add "Adafruit_SSD1306" to your libraries folder.
[github.com/adafruit/Adafruit_SSD1306](https://github.com/adafruit/Adafruit_SSD1306)

- Due to the nature of Adafruit library, you need to do the following:
1. change the value of "SSD1306_LCDHEIGHT" to 64 so that it fits the display dimensions. To do this, simply uncomment "#define SSD1306_128_64" in stead of "#define SSD1306_128_32" in Adafruit_SSD1306.h:Line74-75
2. change "Wire.begin()" to "Wire.begin(4,15)" in Adafruit_SSD1306.cpp:Line206
