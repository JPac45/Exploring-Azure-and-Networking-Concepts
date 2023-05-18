<img src="https://i.imgur.com/bxunY9z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/xjc1vr1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h1>Exploring Networking Concepts</h1>
  
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
<b>Installing Wireshark:</b>
<p>
Once in the Windows VM, download Wireshark via Microsof Edge.
<img src="https://i.imgur.com/iXq2YUF.png">
  
<img src="https://i.imgur.com/hXRR8WF.png">
</p>
<p>

<br />

<h2>Post-Install Configuration Objectives</h2>

<b>Observe ICMP Traffic</b>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>

 
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>  
1. Open Wireshark and filter for ICMP traffic only.
</p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<br />

<b>Observe SSH Traffic</b>
<p>

<p>
1. Back in Wireshark, filter for SSH traffic only
<p>
<img src="https://i.imgur.com/K2pCppV.png">
</p>
2. From your Windows 10 VM, “SSH into” your Ubuntu Virtual Machine (via its private IP address).
<p>
<img src="https://i.imgur.com/2NPbhFp.png">
</p>
3. Type commands (username, pwd, etc) into the linux SSH connection and observe SSH traffic spam in WireShark. Exit the SSH connection by typing ‘exit’ and pressing [Enter] Time 25:55
<p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<b>Observe DHCP Traffic</b>
<p>
</p>
<p>
1. Back in Wireshark, filter for DHCP traffic only
<p>
<img src="https://i.imgur.com/2Fb7hI6.png">
</p>
2. From your Windows 10 VM, attempt to issue your VM a new IP address from the command line <b>(ipconfig /renew)</b>
<p>  
A. Observe the DHCP traffic appearing in WireShark.
</p>
<img src="https://i.imgur.com/ClgFH8B.png" height="93%" width="93%" alt="Disk Sanitization Steps"/>
</p>
<br />

<b>Observe DNS Traffic</b>
<p>

<p>
1. Back in Wireshark, filter for DNS traffic only
<p>
<img src="https://i.imgur.com/62VBXJh.png">
</p>
2. From your Windows 10 VM within a command line, use command <b>nslookup</b> to see what google.com and disney.com’s IP addresses are.
<p>  
A. Observe the DNS traffic being show in WireShark.
<p>  
<img src="https://i.imgur.com/1jZYmvf.png">
</p>
<br />

<b>Observe RDP (Remote Desktop Protocol) Traffic</b>
<p>
<p>
1. Back in Wireshark, filter for RDP traffic only (tcp.port == 3389)
<p>
<img src="https://i.imgur.com/iPdafxc.png">
</p>
You will observe that there is non-stop communication of data happening. This is because the Remote Desktop Protocol is constantly showing you live data from the Remote VM to your desktop machine. 
<p>  
</p>
<br />
