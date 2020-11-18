# M5DV Project
Make digital voice radio (M17 Digital Voice) play yourself over the internet width M5Stack.
The project made M5Stack to talk digital voice with M17 mode via wifi display on the screen. Set up via the web Press the key to speak when mike or listening.

## Equipment needed
- 1.M5Stack 1pc
- 2.Mic MAX9814 Adafruit module 1pc

To connect, connect the mic pin Vdd-> 3.3V, GND-> GND and Out -> GPIO36 (AD) in the gain pin to Vdd, the sound will be low for people speaking loudly.Mic can be used in other models, but must do or set Offset DC to 1.25V.

![image](https://github.com/nakhonthai/M5DV/raw/main/img/M5DVMic.png)

## M5STACK firmware installation (do it first, next, update via web)
- 1.Connect the USB cable to the M5STACK.
- 2.Download firmware and open the program ESP32 DOWNLOAD TOOL, set it in the firmware upload program, set the firmware to M5DV_Vxx.bin, location 0x10000 and partitions.bin at 0x8000 and bootloader.bin at 0x10000 and boot.bin at 0xe000, if not loaded, connect GPIO0 cable to GND, press START button finished, press power button or reset (red) again.
- 3.Keep the left button (A) pressed and press the power button or plug in to default setting.
- 4.Then go to WiFi SSID: M5DV and open a browser to the website. http://192.168.4.1 Can be fixed Or turn on your Wi-Fi router / share SSID name: APRSTH Pass: aprsthnetwork Then enter with IP from M5Stack, receive IP from LCD screen.

![image](https://github.com/nakhonthai/M5DV/raw/main/img/ESP32Tool.png)

## Setting up using a web browser
- 1.Set up Wi-Fi in the Settings tab. Connect to a router or device that shares the Internet. According to the router name (SSID) and password
- 2.Set up digital voices in the IoT tab in the server side. Refactor service also does not need to be modified (except for testing elsewhere), the test room in the M17 Module compartment has 26 rooms, AZ insert one. letter Users put their own name in the myCallSign field and the device sequence (some people use multiple machines) can be assigned 26 characters, one letter A-Z as well.

## How to use
- Push C KEY for PTT 3200 Voice Mode
- Push B KEY for PTT 1600 V/D Mode
- Push A hold and pwr/reset for Factory default.

## M17-THA Reflector
Name: M17-THA
IP: 203.150.19.24
PORT: 17000
Dashboard: https://m17.dprns.com
