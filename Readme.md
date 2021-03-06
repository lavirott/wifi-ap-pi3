# Readme

This install file configures your Raspberrypi 3 as a Wifi-Access Point (AP)
by sharing the incoming internet connection on `eth0` on the `wlan0` device
(internal WiFi Chip on the new Pi).

## Goal
Setup your Raspberrypi 3 as a WiFi Access Point (or Router) to share your ethernet connection with friends and family as a nice take-it-with-you WiFi Network.

## Environment
This script was tested on:
- Raspberry-Pi 3 Model B
- No additonal HW connected
- Rasbian GBU/Linux 9 (`cat /etc/issue`) and Debian version 9.6 (`cat /etc/debian_version`)
- No changes made to the configuration so far

## Installing
```
git clone https://github.com/sebastianzillessen/WiFi-AP-Raspberry-Pi-3.git
cd WiFi-AP-Raspberry-Pi-3
chmod a+x install.sh
sudo ./install.sh
```

Your can specify the following parameters when calling `./install.sh`:

1. SSID (default: $HOSTNAME )
2. PASSPHRASE(default: raspberry)
3. IP_RANGE (default: 192.168.222, produces IP of Pi with 192.168.222.1)
4. Incoming Internet connection device (default: eth0)
5. WiFi Connection Device (default: wlan0)

These are parsed in the order. So with

```
sudo ./install.sh TestAP test123
```
You would setup your Raspberrypi with a SSID `TestAp` and a Password `test123`.

*NOTE*: As the script runs an update of all installed software at the beginning, it might take some time. So be patient!

Feel free to modify it.
