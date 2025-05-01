🚀 Initial Router Configuration Steps:
1. Open Cisco Packet Tracer
○ Add a router (e.g., Cisco 2911) to the workspace.
○ Add a PC and connect it to the router with a straight-through Ethernet cable.
○ Go to the router’s CLI (Command Line Interface) tab.

Enter Privileged EXEC Mode
Router> enable
2.
Enter Global Configuration Mode
Router# configure terminal
3.
Set the Hostname
Router(config)# hostname R1
4.
Set Console Password
R1(config)# line console 0
R1(config-line)# password cisco
R1(config-line)# login
R1(config-line)# exit
5.
Set Enable Password (for Privileged EXEC Mode)
R1(config)# enable secret class
6.

Set VTY Password (for remote access)
R1(config)# line vty 0 4
R1(config-line)# password cisco
R1(config-line)# login
R1(config-line)# exit
7.
Configure Interface (e.g., FastEthernet0/0)
R1(config)# interface fastEthernet0/0
R1(config-if)# ip address 192.168.1.1 255.255.255.0
R1(config-if)# no shutdown
R1(config-if)# exit
8.
Save Configuration
R1# write memory
or
R1# copy running-config startup-config
9.

✅ Optional: Test Connectivity
● Configure the PC’s IP address as 192.168.1.2 / 255.255.255.0 with gateway
192.168.1.1.

Use the ping command from the PC’s command prompt to test connectivity:
ping 192.168.1.1
