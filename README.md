# ESP Cam Nabto

Nabto website is providing free trail service to monitor esp cam globally https://www.nabto.com/esp32/

# Process

  - Sign up in https://console.cloud.nabto.com/#/signup
  - create device and key
  - now download and install ESP-IDF https://docs.espressif.com/projects/esp-idf/en/stable/get-started/#setting-up-development-environment
  - connect the ESP Cam to the PC
  - clone git file
```sh
$ git clone --recursive https://github.com/nabto/nabto-esp32cam.git
```
```sh
$ cd nabto-esp32cam
```
```sh
$ idf.py menuconfig (command for windows os )
```
- Chose the “Camera configuration” menu:
- fill wifi credentials and save
- Adjust the serial device on your workstation used to flash (and monitor) the device:
- choose serial flasher menu
- set to QIO
- SET to 4MB
- SET to 80HZ
- save 
- go to component config > Driver confi > RTCIO enable
- save and quit
```sh
$ idf.py build
```
```sh
$ idf.py flash
```
```sh
$ idf.py monitor
```
- download app and search to find camera (use same wifi network for first time)
Now download the appropriate app for your phone:
Android: https://play.google.com/store/apps/details?id=com.appmyproduct.video
iOS: https://itunes.apple.com/lc/app/appmyproduct-video-client/id1276975254
