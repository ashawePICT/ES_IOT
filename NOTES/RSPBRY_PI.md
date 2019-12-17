# RASPBERRY PIE

## SPECS ( MODEL 3 B )
- Quad Core 1.2GHz Broadcom BCM2837 64bit CPU
- 1GB RAM
- BCM43438 wireless LAN and Bluetooth Low Energy (BLE) on board
- 100 Base Ethernet
- 40-pin extended GPIO
- 4 USB 2 ports
- 4 Pole stereo output and composite video port
- Full size HDMI
- CSI camera port for connecting a Raspberry Pi camera
- DSI display port for connecting a Raspberry Pi touchscreen display
- Micro SD port for loading your operating system and storing data
- Upgraded switched Micro USB power source up to 2.5A

## MIN REQ
- SD CARD **8 GB** ( 4GB for lite )
  - any SD card larger than 32GB is an SDXC card and has to be formatted with the exFAT filesystem. This means the official SD Formatter tool will always format cards that are 64GB or larger as exFAT.
  - The original Raspberry Pi Model A and Raspberry Pi Model B require full-size SD cards. From the Model B+ (2014) onwards, a micro SD card is required.

## TO INSTALL
- **balenaEtcher** is a graphical SD card writing tool and is the easiest option for most users. balenaEtcher also supports writing images directly from the zip file, without any unzipping required. ( zenity might be needed )
- if installing via dd command:
  - ```dd bs=4M if=2019-09-26-raspbian-buster.img of=/dev/sdX status=progress conv=fsync``` where
    ```
    bs=BYTES        read and write up to BYTES bytes at a time
    conv=CONVS      convert the file as per the comma separated symbol list
    if=FILE         read from FILE instead of stdin
    of=FILE         write to FILE instead of stdout
    status=WHICH    WHICH info to suppress outputting to stderr; 'noxfer' suppresses transfer stats, 'none' suppresses all
    ```
    BB can also be said to be block size
    can also do ```unzip -p 2019-09-26-raspbian-buster.zip | sudo dd of=/dev/sdX bs=4M conv=fsync```

## INTERFACES
- Camera — enable the Raspberry Pi Camera Module
- SSH — allow remote access to your Raspberry Pi from another computer using SSH
- VNC — allow remote access to the Raspberry Pi Desktop from another computer using VNC
- SPI — enable the SPI GPIO pins
- I2C — enable the I2C GPIO pins
- Serial — enable the Serial (Rx, Tx) GPIO pins
- 1-Wire — enable the 1-Wire GPIO pin
- Remote GPIO — allow access your Raspberry Pi’s GPIO pins from another computer

## COMMANDS
- ```pinout``` This will show you a labelled diagram of the GPIO pins, and some other information about your Pi. ![pinout command output](https://projects-static.raspberrypi.org/projects/raspberry-pi-using/062f905abdfbfaa2706685a187c2e8c46da5d5a8/en/images/pi-terminal-pinout.png)
