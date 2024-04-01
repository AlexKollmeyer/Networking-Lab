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
<br/ >
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

<h2>Observing SSH Activity</h2>
1. In Wireshark filter for SSH Traffic
2. From your windows 10 VM, "SSH into" your Ubuntu virtual machine via it's private IP Address
3. Type and use commands (username, pwd, etc) into the linux SSH connection and obeserve the SSH traffic in wireshark as you type.
4. Exit the SSH By typing exit and then pressing the enter key.


<h2>Observing DHCP Traffic</h2>
1. In wireshark filter for DHCP traffic
2. In the command line for the windows 10 VM, attempt to issue your VM a new IP Address using ipconfig/renew
3. Observe the DHCP traffic appearing in wireshark as your VM is assigned a new IP address

<h2>Observing DNS Traffic</h2>
1. In Wireshark filter for DNS Traffic only
2. From the command line, use the command nslookup to see the ip addresses for any sites (google.com, disney.com)
3. Observe the DNS traffic in Wireshark

<h2>Observing RDP Traffic</h2>
1. In Wireshark filter for RDP Traffic only (tcp port 3389)
2. You will immedietly notice a non stop spam of traffic. This is because RDP (Remote Desktop Protocol is what is currently being used to connect from whatever computer you are physically to a livestream of the Windows 10 virtual machine, so there should constantly be traffic back and forth between your computer and the VM.


<h2>Cleanup</h2>
1. Close the Remote desktop connection
2. Delete the resouce group (important so as not to continue to incur costs from the VM) and verify it was deleted.


