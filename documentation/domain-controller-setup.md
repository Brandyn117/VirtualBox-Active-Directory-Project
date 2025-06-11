# 🎮 Domain Controller Setup

## VM Setup
After adding the ISO and configuring the necessary hardware specifications for the domain controller VM, I set the first network interface (NIC) to connect to my home internet. This NIC will serve as the external connection. 

<img src="../images/NIC Internet.png" alt="NIC" width="600">

Next, I configured a second NIC for internal communication. This NIC is attached to an internal VirtualBox network and will be used to communicate with the client VM.

<img src="../images/NIC Internal.png" alt="NIC" width="600">
