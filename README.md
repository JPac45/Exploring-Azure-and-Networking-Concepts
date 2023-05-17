<img src="https://i.imgur.com/bxunY9z.png">
</p>

<h1>Exploring Azure and Networking Concepts</h1>
  
This tutorial will allow you to observe several types of network traffic between virtual machines in Azure. To observe the network communications, we will install Wireshark .<br />


<h2>Video Demonstration - Probably will delete this section</h2>

- ### [YouTube: How To Configure osTicket, post-installation](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Wireshark (Network Traffic Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
- Linux (Ubuntu)

<h2>Post-Install Configuration Objectives</h2>

- Observe ICMP (Internet Control Messaage Protocol) Traffic
- Observe SSH (Secure Shell ; Port 22) Traffic
- Observe DHCP (Dynamic Host Configuration Protocol; Port 67 & 68) Traffic
- Observe DNS (Domain Name System; Port 53) Traffic
- Observe RDP (Remote Desktop Protocol; Port 3389) Traffic

<h2>Configuration Steps</h2>

<p>
<p>
We will need two VMs in Azure - one with Windows 10 and the other with Ubuntu. This tutorial assumes the two VMs have already been created. Click here for the VM Creation Tutorial. 
</p>
<br />
Installing Wireshark
<p>
Once in thw Windows VM, download Wireshark via Microsof Edge.
<img src="https://i.imgur.com/iXq2YUF.png">
  
<img src="https://i.imgur.com/hXRR8WF.png">
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

<h2>Post-Install Configuration Objectives</h2>

- Observe ICMP Traffic
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Use Remote Desktop to connect to your Windows 10 Virtual Machine
<p>

 
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2. Within your Windows 10 Virtual Machine, Install Wireshark.
<p>  
3. Open Wireshark and filter for ICMP traffic only.
</p>
<br />

- Observe SSH Traffic
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Back in Wireshark, filter for SSH traffic only
<p>  
2. From your Windows 10 VM, “SSH into” your Ubuntu Virtual Machine (via its private IP address)
<p>  
 A. Type commands (username, pwd, etc) into the linux SSH connection and observe SSH traffic spam in WireShark
</p>
 B. Exit the SSH connection by typing ‘exit’ and pressing [Enter]
</p>
<br />

- Observe DHCP Traffic
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Back in Wireshark, filter for DHCP traffic only
<p>  
2. From your Windows 10 VM, attempt to issue your VM a new IP address from the command line (ipconfig /renew)
<p>  
A. Observe the DHCP traffic appearing in WireShark.
</p>
<br />

- Observe DNS Traffic
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Back in Wireshark, filter for DNS traffic only
<p>  
2. From your Windows 10 VM within a command line, use nslookup to see what google.com and disney.com’s IP addresses are
<p>  
A. Observe the DNS traffic being show in WireShark.
</p>
<br />

- Observe RDP Traffic
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Back in Wireshark, filter for RDP traffic only (tcp.port == 3389)
<p>  
2. Observe the immediate non-stop spam of traffic? Why do you think it’s non-stop spamming vs only showing traffic when you do an activity?
<p>  
A. Answer: because the RDP (protocol) is constantly showing you a live stream from one computer to another, therefor traffic is always being transmitted
</p>
<br />
