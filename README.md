
1. Clone the repo


2. Download the [Arduino 1.8.x IDE](https://www.arduino.cc/en/software)

3. Double click to open `pocket-wifi.ino` in the IDE.

4. Go to File > Preferences and add this line to 'Additional Boards Manager URLs'. Hit Ok.

```
https://arduino.esp8266.com/stable/package_esp8266com_index.json
```

5. Go to Tools > Board > Boards Manager. Type `esp8266` to find the package, then click Install. Close when done.

6. Now go to Tools > Board > ESP8266 Boards and select LOLIN(WEMOS) D1 mini (clone).

7. Connect your Wemos D1 mini to your computer using a USBC cable. In the menu bar, go to Tools > Port and select /dev/cu.usbserial-XXX.

### Install SPIFFS uploader plugin

8. Download the [latest release](https://github.com/esp8266/arduino-esp8266fs-plugin/releases) of the plugin. Unzip the file to create a directory called ESP8266FS.

9. Go to Arduino > Preferences and make a note of the path under "Sketchbook location." In the sketchbook directory, look for a directory called tools. If you don't see one, you can create it yourself. Move the ESP8266FS directory from your Downloads folder to the tools directory. Relaunch the IDE if needed.

10. To upload files = In the menu bar, select Tools > ESP8266 Sketch Data Upload. This plugin will look for a directory called data in the project directory and upload its contents to SPIFFS storage on the ESP8266.

11. Click the Upload button in the top left to compile and upload the project code to your Wemos D1 mini.

## Deploy

Run

```bash
 chmod +x ./deploy.sh
./deploy.sh

