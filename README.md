A quick guide on how to install a MHS 3.5 inch LCD on a Raspberry Pi running 64bit OS (namely Raspbian). 

this LCD may have diffrent names ，waveshare is "3.5inch RPi LCD (C)" ，https://www.waveshare.net/wiki/3.5inch_RPi_LCD_(C)
goodtft is "mh35",some other call it "lcd35",
actually 3.5 inch LCD contains at least 3 types：LCD A /LCD B/LCD C. 
below is LCD (C) by waveshare which also called mhs 3.5 by goodftf，and the exactly
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

This is cloned and cobbled together from https://github.com/tux1c/wavesharelcd-64bit-rpi (who deserves all the credit) and is tested on a RPi 4 with a fresh install of Raspbian 64 bit beta from here https://www.raspberrypi.org/forums/viewtopic.php?t=275370

# Installation
`git clone https://github.com/GoogleBeEvil/MHS35-lcd-64bit-rpi.git`

`cd MHS35-lcd-64bit-rpi`

`chmod +x install.sh`

`sudo bash install.sh` or `sudo bash installnotouch.sh`

# Troubleshooting
## White screen on boot (raspberry pi boots)
make sure `dtoverlay=vc4-fkms-v3d` is **NOT** present / commented out in `/boot/config.txt`

