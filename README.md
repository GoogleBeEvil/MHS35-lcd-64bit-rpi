A quick guide on how to install a MHS 3.5 inch LCD on a Raspberry Pi running 64bit OS (namely Raspbian). 

This is cloned and cobbled together from https://github.com/tux1c/wavesharelcd-64bit-rpi (who deserves all the credit) and https://github.com/alexstacey/MHS35-lcd-64bit-rpiis(who fixes the typo errors).

tested on a raspberry 4B 8GB with a fresh install of Raspbian 64 bit lite from here https://downloads.raspberrypi.org/raspios_lite_arm64/images/raspios_lite_arm64-2021-05-28/

this LCD may have diffrent names ，waveshare is "3.5inch RPi LCD (C)" :
`https://www.waveshare.net/wiki/3.5inch_RPi_LCD_(C)`

goodtft is "mh35",some other call it "lcd35"；

actually 3.5 inch LCD series contains at least 3 types：LCD A /LCD B/LCD C. https://www.waveshare.net/wiki/3.5inch_RPi_LCD_(C)

Below is LCD (C) called by waveshare which also called mhs 3.5 by goodftf，and the exactly description is on
http://www.lcdwiki.com/MHS-3.5inch_RPi_Display  

| Name                                   | Description                          |
| -------------------------------------- | ------------------------------------ |
| SKU                                    | MHS3528                              |
| Screen Size                            | 3.5inch                              |
| LCD Type                               | TFT                                  |
| Module Interface                       | SPI (upports up to 125MHz SPI input) |
| Resolution                             | 320*480 (Pixel)                      |
| Touch Screen Controller                | XPT2046                              |
| LCD Driver IC                          | ILI9486                              |
| Backlight                              | LED                                  |
| power consumption                      | 0.16A*5V                             |
| Working temperature（℃）           | -20~60                               |
| Active Area                            | 48.96x73.44(mm)                      |
| Module PCB Size                        | 85.42*55.60 (mm)                     |
| Package Size                           | 136x98x41 (mm)                       |
| Product Weight(Package containing)(g)  | 92 (g)                               |   |
![avatar](https://raw.githubusercontent.com/GoogleBeEvil/XPT2046-64bit-rpi/master/%E6%8D%95%E8%8E%B7.PNG)
# Installation
`sudo rm -rf  XPT2046-64bit-rpi`

`git clone https://github.com/GoogleBeEvil/XPT2046-64bit-rpi.git`

`cd XPT2046-64bit-rpi`

`chmod +x install.sh`

`sudo bash install.sh` is for  OS have installed xorg

or 

`sudo bash install-lite.sh` is for OS have not installed xorg，usually raspberry pi OS lite

# Troubleshooting
## White screen on boot (raspberry pi boots)
make sure `dtoverlay=vc4-fkms-v3d` is **NOT** present / commented out in `/boot/config.txt`

