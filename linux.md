# Linux
  
Test for bad sectors.  
`badblocks -sv /dev/device`  
  
Check SMART status:  
`smartctl -t long /dev/device`  
  
Burn DVD   
`growisofs -dvd-compat -Z /dev/sr0=/path/to/file.iso`  
   
dmesg is the kernel ring buffer. Use the following to list the last ten things that happened.  
`dmesg | tail`  
   
Bring up the device 'wlan0'  
`sudo ifconfig wlan0 up`   
  
Use iwlist to scan for SSIDs  
`sudo iwlist scan`  

Connect to an SSID with a WEP key.  
`sudo iwconfig wlan0 essid "ssid" key WEPKEY`  

Set the channel to auto.  
`sudo iwconfig wlan0 channel auto`  

Request an IP from DHCP   
`sudo dhcpcd wlan0`   
