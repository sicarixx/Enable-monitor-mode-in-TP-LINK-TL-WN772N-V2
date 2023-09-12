# Enable monitor mode in TP-LINK TL-WN772N V2
## Realtek rtl8188eus & rtl8188eu & rtl8188etv WiFi drivers
### Linux system Debian based
```
sudo apt update
sudo apt install bc
sudo rmmod r8188eu.ko
git clone https://github.com/aircrack-ng/rtl8188eus
cd rtl8188eus
sudo -i
echo "blacklist r8188eu" > "/etc/modprobe.d/realtek.conf"
exit
make
sudo make install
sudo modprobe 8188eu
```
Commands to enable monitor mode
```
ifconfig wlan0 down
airmon-ng check kill
iwconfig wlan0 mode monitor
ifconfig wlan0 up
iwconfig
```
### Source
GitHub - https://github.com/aircrack-ng/rtl8188eus

### Credits
Realtek - https://www.realtek.com<br>
Alfa Networks - https://www.alfa.com.tw<br>
aircrack-ng. - https://www.aircrack-ng.org<br>
