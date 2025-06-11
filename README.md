# 🖱️VirtualBox-Active-Directory-Project

This project demonstrates setting up a Windows Server 2019 domain controller and Windows Client in VirtualBox, complete with:
<li> Active Directory </li>
<li> DHCP </li>
<li> NAT Routing (via RAS)</li>
<li> 1,000+ automated user creation (PowerShell) </li>
<li> Windows 10 client domain join </li>

## 🛠️ Tools Used
<li> VirtualBox </li>
<li> Windows Server 2019 ISO </li>
<li> Windows 10 ISO </li>
<li> PowerShell </li>

## 🚁 Project Overview
<img src="images/AD Diagram.drawio.png" alt="NIC" width="750">
<b> 1. Create the Domain Controller (VM1) </b>
<br>
VM1 will serve as the domain controller and host Active Directory. It will have two network adapters:
<ul style="margin-left: 20px;">
  <li>One connected to the internet (external)</li>
  <li>One connected to a VirtualBox internal network (for client communication)</li>
</ul>
<b> 2. Configure Network Settings </b>
<br>
<ul style="margin-left: 20px;">
  <li>The external NIC will automatically receive an IP address from my home network (via DHCP)</li>
  <li>I will assign a static IP to the internal NIC manually</li>
</ul>
<b> 3. Name the Server and Install Active Directory </b>
<br>
<ul style="margin-left: 20px;">
  <li>I’ll name the server and install Active Directory Domain Services (AD DS)</li>
  <li>Then I’ll create a new domain</li>
</ul>
<b> 4. Enable NAT and Routing </b>
<br>
<ul style="margin-left: 20px;">
  <li>I will configure Routing and Remote Access (RRAS) to enable NAT, allowing internal network clients to access the internet through the domain controller</li>
</ul>
<b> 5. Set Up DHCP </b>
<br>
<ul style="margin-left: 20px;">
  <li>I will install and configure DHCP on the domain controller so it can assign IP addresses to client machines</li>
</ul>
<b> 6. Create Users in Active Directory </b>
<br>
<ul style="margin-left: 20px;">
  <li>I will run a PowerShell script to automatically generate 1,000 user accounts in Active Directory</li>
</ul>
<b> 7. Create the Client VM (Windows 10) </b>
<br>
<ul style="margin-left: 20px;">
  <li>I’ll create a second VM, install Windows 10, and connect it to the internal network</li>
  <li>Then I’ll join the client to the domain and log in using one of the domain user accounts</li>
</ul>

## 🧱 Project Breakdown
- [Domain Controller Setup](documentation/domain-controller-setup.md)
- [RAS / NAT Setup](documentation/ras-nat-routing-setup.md)
- [DHCP Setup](documentation/dhcp-setup.md)
