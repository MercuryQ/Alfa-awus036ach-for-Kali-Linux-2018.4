# Alfa-awus036ach-for-Kali-Linux-2018.4
Install Alfa awus036ach using Kali Linux 2018.4 on Virtual Box
## How to install Alfa awus036ach using Kali Linux 2018.4 on Virtual Box?
### Before beginning
##### Make sure you have the correct virtual extensions in your Virtual Box to enable USB 3.0
##### I did this on fresh Kali Linux 2018.4 installation
##### Keep Alfa adapter unplugged until the steps say to connect the adapter
### Steps
##### Once your Kali Linux VM is running open the terminal to install the headers (This could take a while)
##### Follow these steps (Enter the commands in the kali terminal):
##### 1.	sudo apt-get dist-upgrade –y
##### 2.	Then reboot your VM and open terminal again
##### 3.	sudo apt-get install linux-headers-$(uname –r)
##### 4.	sudo apt-get upgrade linux-headers-$(uname –r) 
### Next, you need to install the support for RTL8812AU Wireless Card Injection
##### Link: https://www.kali.org/news/kali-linux-20171-release/
##### In the Kali terminal enter the following commands:
##### 1.	apt-get update
##### 2.	apt install realtek-rt188xxau-dkms
### Now power off your VM and return to Virtual Box
### Connect your Alfa awus036ach adapter
### Within Virtual Box go to the settings of your Kali VM, and select the USB tab
##### Follow these steps inside the USB tab:
##### 1.	Check Enable USB Controller
##### 2.	Select USB 3.0 (xHCI) Controller
##### 3.	Within the USB Device Filters add the Realtek 802.11n NIC (Click on the usb plus symbol to locate this device)
##### 4.	Make sure this device is checked
### Now start up your Kali VM
### Lastly, check to see if your Kali now recognizes a wlan0
##### Type these commands in the Kali terminal:
##### •	ifconfig
##### •	iwconfig
### After
##### 	Make sure you unlick the USB adapter within Kali Linux before powering off the VM or you will experience minor technical difficulties. If you do forget, you must start your VM, unlick the USB adapter, and power off the VM. This will make your device recognizable once you restart your Kali VM. 
