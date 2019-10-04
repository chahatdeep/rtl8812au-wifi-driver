# rtl8812au-wifi-driver
WiFi driver for EDUP EP-DB1607 600MBps WiFi Module for Linux. Tested on Intel Up board with Linux Ubuntu 16.04.5 LTS.

Follow this:

1. Remove the rtl8812du driver if already exist:
```
sudo apt purge rtl8812au-dkms
```

2. Clone the driver and build
```
sudo apt install git
git clone https://github.com/chahatdeep/rtl8812au-wifi-driver.git
sudo cp -r rtl8812au  /usr/src/rtl8812au-4.2.2
sudo dkms add -m rtl8812au -v 4.2.2
sudo dkms build -m rtl8812au -v 4.2.2
sudo dkms install -m rtl8812au -v 4.2.2
```

3. Restart your system
```
sudo reboot
```


***

Original rights to this driver are reserved to [gnab](https://github.com/gnab/rtl8812au)
