# Networking-Lab
<p align="center">
<img src="https://i.imgur.com/UOlLgAX.png" alt="networking image"/>
</p>

<h1>Networking with virtual machines lab</h1>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
- Ubuntu Sever (Linux) 20.04

<h2>Setup Steps</h2>

1.Create a resource group in azure
2. Create a windows 10 virtual machine, it should be in the same region as the resource group, let it create a new virtual network (vnet)
3.Create A Ubuntu 20.04 Server (Linux), ensure that it is in the same previously created resource group and vnet as the windows 10 virtual machine

<h2>Observing ICMP Traffic</h2>
1. Use remote desktop to connect to the windows 10 virtual machine
2.Within your Windows 10 Virtual Machine, Install Wireshark
3.Open Wireshark and filter for ICMP traffic only
4.Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM. Observe ping requests and replies within WireShark
5.From The Windows 10 VM, open command line or PowerShell and attempt to ping a public website (such as www.google.com) and observe the traffic in WireShark
6.Initiate a perpetual/non-stop ping from your Windows 10 VM to your Ubuntu VM
7.Open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic
8.Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity
9.Re-enable ICMP traffic for the Network Security Group your Ubuntu VM is using
10.Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity (should start working)
11.Stop the ping activity

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
