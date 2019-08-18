# WiFi-Fish-Feeder-With-Camera

### 3D Printing

Use these settings: 0.2 / 10% infill. 

### Schema

Connect 5V, GND and GPIO12 for the signal wire to the servo. Use a micro usb pcb to connect it to a regular 5V power adapter.

### Arduino source

First install the ESP32 library. 
1. Start the Arduino IDE
2. Go to File > Preferences
3. Edit the "Additional Board Manager URLs" and add this URL:
    https://dl.espressif.com/dl/package_esp32_index.json
4. Go to Tools > Board > Boards Manager
5. Search for ESP32 and Install

Use an FTDI board and connect RX of the FTDI board to TX of the ESP32 board, TX (FTDI) to RX (ESP32) together with GND and 3.3V. If you're having trouble with the ESP32 (horizontal lines on the camera or "brownout detected" errors, you can try connecting an external 5V power supply to the 5V pin of the ESP32 (and connect GND's).  

Open the "WiFi-Fish-Feeder-With-Camera.ino" file from this repository and change the following setttings:

* Tools > Board, select ESP32 Wrover Module
* Tools > Port, select the COM port 
* In Tools > Partition Scheme, select "Huge APP (3MB No OTA)"

To upload the code, connect GPIO0 to GND and press the reset button on the device. Then hit upload in the Arduino IDE. After succesfully uploading press the reset button again and check the serial monitor to find out which IP Address it get's assigned. Browse to that IP and check if everything works.

### YouTube video

TODO:

<a href="https://youtu.be/24RslguGy58" target="_blank"><img src="https://img.youtube.com/vi/24RslguGy58/0.jpg" 
alt="Click to view: Homemade CNC with 3D printed parts V2" width="500" border="1" /></a>
