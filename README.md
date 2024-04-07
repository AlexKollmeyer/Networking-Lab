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
<p>
1.Create a resource group in azure
<br/>
2. Create a windows 10 virtual machine, it should be in the same region as the resource group, let it create a new virtual network (vnet)
<br/>
  <img src="https://imgur.com/ZKrTS07.png" alt="networking image"/>
  <img src="https://imgur.com/wQEw6b4.png" alt="networking image"/>
</p>
3.Create A Ubuntu 20.04 Server (Linux), ensure that it is in the same previously created resource group and vnet as the windows 10 virtual machine
</p>
<img src="https://imgur.com/gIm94qR.png" alt="networking image"/>

<h2>Observing ICMP Traffic</h2>
1. Use remote desktop to connect to the windows 10 virtual machine
<img src="https://imgur.com/22rWHJY.png" alt="networking image"/>
<br/>
2.Within your Windows 10 Virtual Machine, Download and Install Wireshark 
<img src="https://imgur.com/Ku4LroD.png.png" alt="networking image"/>
<img src="https://imgur.com/8nFRIcf.png" alt="networking image"/>
<br/>
3.Open Wireshark and filter for ICMP traffic only
<br/>
4.Retrieve the private IP address of the Ubuntu VM and attempt to ping it from within the Windows 10 VM. Observe ping requests and replies within WireShark
<img src="https://imgur.com/3DOgzaZ.png" alt="networking image"/>
<img src="https://imgur.com/VbeOOrQ.png" alt="networking image"/>
<br/>
5.From The Windows 10 VM, open command line or PowerShell and attempt to ping a public website (such as www.google.com) and observe the traffic in WireShark
<img src="https://imgur.com/ONG9XRu.png" alt="networking image"/>
<br/>
6.Initiate a perpetual/non-stop ping from your Windows 10 VM to your Ubuntu VM. Command is ping (private ip address) -t
<img src=https://imgur.com/4lI2ZA4".png" alt="networking image"/>
<br/>
7.Open the Network Security Group your Ubuntu VM is using and disable incoming (inbound) ICMP traffic
<img src="https://imgur.com/Lk92QGZ.png" alt="networking image"/>
<br/>
8.Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity
<img src="https://imgur.com/flloi1o.png" alt="networking image"/>
<br/>
9.Re-enable ICMP traffic for the Network Security Group your Ubuntu VM is using
<img src="https://imgur.com/OHzi2Pi.png" alt="networking image"/>
<br/>
10.Back in the Windows 10 VM, observe the ICMP traffic in WireShark and the command line Ping activity (should start working)
<br/>
11.Stop the ping activity

<h2>Observing SSH Activity</h2>
1. In Wireshark filter for SSH Traffic
<br/>
2. From your windows 10 VM, "SSH into" your Ubuntu virtual machine via it's private IP Address
<br/>
<img src="https://imgur.com/tDbKOzU.png" alt="networking image"/>
3. Type and use linux commands (id,uname -a, pwd) into the linux SSH connection and obeserve the SSH traffic in wireshark as you type.
<img src="https://imgur.com/pELtaKi.png" alt="networking image"/>
<br/>
4. Exit the SSH By typing exit and then pressing the enter key.


<h2>Observing DHCP Traffic</h2>
1. In wireshark filter for DHCP traffic
<br/>
2. In the command line for the windows 10 VM, attempt to issue your VM a new IP Address using ipconfig/renew
<br/>
3. Observe the DHCP traffic appearing in wireshark as your VM is assigned a new IP address
<img src="https://imgur.com/OStUfYQ.png" alt="networking image"/>

<h2>Observing DNS Traffic</h2>
1. In Wireshark filter for DNS Traffic only
<br/>
2. From the command line, use the command nslookup to see the ip addresses for any sites (google.com, disney.com)
<br/>
3. Observe the DNS traffic in Wireshark
<img src="https://imgur.com/c4Kcu7l" alt="networking image"/>

<h2>Observing RDP Traffic</h2>
1. In Wireshark filter for RDP Traffic only (tcp port 3389)
<br/>
2. You will immedietly notice a non stop spam of traffic. This is because RDP (Remote Desktop Protocol is what is currently being used to connect from whatever computer you are physically to a livestream of the Windows 10 virtual machine, so there should constantly be traffic back and forth between your computer and the VM.
<img src="https://imgur.com/h4QV5zU.png" alt="networking image"/>


<h2>Cleanup</h2>
1. Close the Remote desktop connection
2. Delete the resouce group (important so as not to continue to incur costs from the VM) and verify it was deleted.
<img src="https://imgur.com/h4QV5zU.png" alt="networking image"/>


