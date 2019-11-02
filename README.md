# HP LaserJet 2100 WIFI bridge

Providing WIFI to an old HP LaserJet 2100 with a ethernet card (10/100MBit/s)


## parts

  * Raspberry 2b
  * USB WIFI dongle
  * DC-DC Step up Converter (3.5V from LaserJet motherboard) to 5V 
  * ethernet cable
  
## setup

Raspbian works read only. If the LJ 2100 is switched on, raspberry starts. The LJ2100 receives via a DHCP-Server on the Raspbian a static IP address.

I have enabled ip routing between eth0 and wlan0, but you can also use CUPS.


## manual setup

setup wpa passphrase:
```bash
wpa_passphrase WIFI-NAME > /etc/wpa_supplicant/wpa_supplicant-wlan0.conf
```
