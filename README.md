# Kali Linux HomeLab (VirtualBox)

## 📌 Overview

This project documents the setup of a Kali Linux home lab using Oracle VirtualBox on a Windows host system. The goal of this lab is to build a foundational environment for hands-on cybersecurity practice, including Linux administration, resource monitoring, and future offensive/defensive security testing. </br>

This lab is designed as a starting point for SOC, Blue Team, and general cybersecurity learning. </br>

 <img src="https://github.com/niha-v/home-lab-kali-linux-virtualbox/blob/main/Image%201.png" width="500">

## 🎯 Objectives 

Set up a stable Kali Linux virtual machine
Understand VM resource allocation and performance
Configure usability features (display scaling, clipboard, shared files)
Practice basic Linux system administration commands

## 🖥️ System Requirements

- Host machine with minimum 8 GB RAM (recommended for smooth VM performance)
- Windows OS (host)
- Oracle VirtualBox (latest version)

## 🛠️ Tools & Technologies

- Oracle VirtualBox
- Kali Linux (Installer Image – Latest Version)
- Linux CLI utilities (apt, htop)

## ⚙️ Step-by-Step Setup
###  1️⃣ Install Oracle VirtualBox

- Download and install Oracle VirtualBox on the host system
- Ensure virtualization is enabled in BIOS
</br> </br> 
### 2️⃣ Install Kali Linux (Virtual Machine)

- Download the Kali Linux Installer ISO (latest version)
- Create a new VM in VirtualBox
- Allocate appropriate resources (RAM & CPU)
- Complete the Kali Linux installer setup
</br> </br>
### 🌐 Networking Configuration

For this lab, I chose a NAT (Network Address Translation) configuration. This setup provides several key benefits for a security environment:
- Isolated Environment: The Kali VM is on a separate private IP space from my host machine, preventing accidental exposure of the host to lab activities.
- Internet Connectivity: Allows for seamless updates (apt update) and tool installations without complex manual routing.
- DHCP Management: VirtualBox automatically assigns an IP address, ensuring consistent connectivity.
</br> </br>
### 3️⃣ Update the System

After logging into Kali Linux, run the following commands:
- sudo apt update && sudo apt upgrade -y
<img src= "https://github.com/niha-v/home-lab-kali-linux-virtualbox/blob/main/image%202.png" width="500">
Verify the installed Kali version:
- cat /etc/os-release
</br> </br>
 
### 4️⃣ Install Resource Monitoring Tool (htop)
- sudo apt install htop -y

<img src= "https://github.com/niha-v/home-lab-kali-linux-virtualbox/blob/main/image%203.png" width="500">

Why htop? </br>
Monitors CPU, RAM, and running processes in real time. Useful for understanding VM resource consumption

- Run htop using: htop command </br>

<img src= "https://github.com/niha-v/home-lab-kali-linux-virtualbox/blob/main/Image%204.png" width="500">
</br> </br>

### 5️⃣ Install VirtualBox Guest Additions

To improve performance and enable clipboard sharing, display scaling, and shared folders:
- sudo apt install -y virtualbox-guest-utils virtualbox-guest-x11

After installation, reboot Kali Linux to apply changes.
</br> </br>

### 6️⃣ Display Scaling & Resolution Configuration

Adjusted display scaling (eg. 1.25) for high DPI monitor compatibility
</br> </br>

### 7️⃣ Clipboard & File Sharing Tests

Test copy–paste functionality between Windows host and Kali VM
Configure Shared Folders in VirtualBox settings to enable file transfer between host and guest
</br> </br>

## 🧠 Key Learnings

Virtual machine resource management is critical for performance
Guest Additions significantly improve VM usability
Linux command-line proficiency is essential for cybersecurity roles


## 📬 Author

Niharika Umrani | *Cybersecurity Analyst* 

---
####  🔐 *This home lab is built strictly for educational and ethical cybersecurity practice.*



