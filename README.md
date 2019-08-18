# Wi-Fi Fish Feeder With Camera

### Components

You need the following components:

* An ESP32-Cam module with Wi-Fi Antenna
* A large continuous rotating servo (it might also work with the more popular tiny MG90 but then you would have to modify it for continuous rotation and design another servo mount)
* Micro usb pcb
* 5V power adapter
* A regular 608 bearing 
* M3 nuts, bolts and washers
* 15 * 15 mm aluminium rod (optional)
* Wires

### 3D Printing

Use these settings: 0.2 / 10% infill. Support is needed for some pieces.

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

<a href="https://youtu.be/dWhmNZHbLFU" target="_blank"><img src="https://img.youtube.com/vi/dWhmNZHbLFU/0.jpg" 
alt="Click to view: Fish Feeder" width="500" border="1" /></a>
