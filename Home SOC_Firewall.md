# Home SOC/Firewall Project

This project was built and documented by I, Jonathan King on October 29th 2023. This project is still currently being worked on as I aim to continually improve and develop on it, however this is the most current version of the project.
## Goal of this Project

The Goal of this project is to:
* To have fun and expand my knowledge and skill base in SIEM and Firewalls tools.
* Attempt at making a more secure and personalized home network.

## Steps to Virtualizing pfSense on VMWare

1.	In the virtual network editor, I created two networks:
    * Network 1: VMnet0 is bridged to the ethernet adapter.(Will be used for the LAN)
    * Network 2: VMnet8 is set to NAT.(Will be used for the WAN)
2.	I Created a new virtual machine.
3.	I installed pfSense via ISO onto VM.
4.	I set the first network adapter to custom VMnet8.
5.	I added an additional network adapter and set to Bridged(Automatic).
6.	On first boot set WAN to em0 DHCP.
7.	Set LAN to em1 and set static IP to match local network e.g 192.168.1.254.
8.	It is important to disable DHCP services on the LAN network when another DHCP server is present.
9.	Now devices can use pfSense as the firewall by setting the gateway and DNS to 192.168.1.254.
10.	Alternatively, you can configure the local DHCP server to serve 192.168.1.254 as the gateway.

## Software Used

* Router/Firewall - pfSense
* Virtual Machine - VMWare
* Monitoring Network Traffic - WireShark and pfSense

## Hardware Used

* Lenovo Ideapad 3
* Realtek USB Hub as network adapter