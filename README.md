# Install UTM + Kali Linux on MacBook (Apple Silicon)

**Hardware:** MacBook Pro M4  
**Goal:** Quick, free, high-performance Kali Linux using UTM virtualization

## Why This Setup?
- Native ARM64 performance 
- 100% free 
- Perfect for blue-team practice (Nmap, Wireshark, Metasploit, Burp Suite, etc.)

## Step-by-Step Installation Guide

### 1. Install UTM
1. Go to https://mac.getutm.app
2. Download and install (free from official site or Mac App Store)
3. Open UTM

### 2. Download Kali Linux ARM64
1. Go to https://www.kali.org/get-kali/
2. Choose **Apple Silicon (ARM64)**
3. Download the latest Kali Linux ISO

### 3. Create the Kali VM in UTM
1. In UTM click **Create a New Virtual Machine**
2. Select **Virtualize** -> **Linux** -> **CPU** -> **Boot ISO Imageand** choose the kali-linux-2025...staller-arm64.iso -> **Storage** -> **Continue** -> **Save** -> **Run**
Settings I recommend:
 - CPU Cores: 4–6
 - Memory: 4–8 GB RAM
- Storage: 30–50 GB

### 4. Working / 'Display output is not active.' Error?
   Working -> go to step 6
   
### 5. Fix 'Display output is not active.'
1. Stop VM
2. Right Click -> Edit
3. Go to 'Display' -> Choose 'Emulated Display Card' virtio-ramb
4. Under 'Devices' Tab click 'New...' add 'Serial' -> Save
5. Start install process via terminal windows
6. Eject ISO when done.

### 6. Kali installer 
GNU GRUB
version 2.12-9+kali1
1. Select a language
2. Select your location
3. Configure the keyboard
4. Waiting for install...
5. Configure the network - enter the hostname for this system / Domain name 
6. Set up users and passwords
7. Configure the clock
8. Waiting for install...
9. Partition disks - Write the changes to disks
10. Waiting for install...
11. Software selection
12. Waiting for install...
13. Finish the installation
14. Reboot

### 4. First Boot & Basic Setup
- Login: 'username' / 'password'
- Update system: 'sudo apt update && sudo apt upgrade -y'

## Screenshots 


## Usefull for
- Secure environment creation
- SOC Analyst / penetration testing practice


This repo show how I build modern cybersecurity environments.
