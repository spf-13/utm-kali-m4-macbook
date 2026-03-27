# Install UTM + Kali Linux on MacBook (Apple Silicon)

**Hardware:** MacBook Pro M4  
**Goal:** Quick, free, high-performance Kali Linux using UTM virtualization

## Why This Setup?
- Native ARM64 performance 
- 100% free 
- Perfect for cybersecurity practice (Nmap, Wireshark, Metasploit, Burp Suite, etc.)

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

### 4. Working / "Display output is not active." Error?
<img width="787" height="631" alt="error_screen" src="https://github.com/user-attachments/assets/1d83bf0c-3ccc-4531-8a97-50075e11c6cf" />
<img width="1285" height="840" alt="install_screen_3" src="https://github.com/user-attachments/assets/37af739d-9996-4daf-867c-75d7b618efd1" />

   Working -> go to step 6
   
### 5. Fix "Display output is not active."
1. Stop VM
2. Right Click -> Edit
3. Go to "Display" -> Choose "Emulated Display Card" virtio-ramb
4. Under "Devices" Tab click "New..." add "Serial" -> Save
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
- Login: "username" / "password"
- Update system: "sudo apt update && sudo apt upgrade -y"

## Screenshots 
<img width="1303" height="959" alt="utm_page_download" src="https://github.com/user-attachments/assets/c1fa7415-3a83-4267-b347-9c65911591db" />
<img width="897" height="646" alt="utm_screen" src="https://github.com/user-attachments/assets/ab0f7e8c-a5ff-4964-974a-a0ad691361f1" />
<img width="1357" height="962" alt="kali_page_download" src="https://github.com/user-attachments/assets/592f9956-0c30-4f22-85da-83c0bbcc01f7" />
<img width="897" height="646" alt="utm_screen" src="https://github.com/user-attachments/assets/c29052bc-9e91-4fd9-88ee-5c679f786ffc" />
<img width="793" height="633" alt="install_screen_1" src="https://github.com/user-attachments/assets/99c1e939-5b64-4ff7-a697-7d1ca0f1ecea" />
<img width="903" height="663" alt="workover_6" src="https://github.com/user-attachments/assets/551735a3-43a0-46bb-9c3d-625fa0d97ecb" />
<img width="1119" height="753" alt="workover_8" src="https://github.com/user-attachments/assets/86a76123-0fd6-4ccb-be13-431bf66b1b7e" />
<img width="1153" height="784" alt="install_process_8" src="https://github.com/user-attachments/assets/9b47abc6-5921-49eb-9a6e-296cbd6f1be9" />
<img width="916" height="725" alt="install_process_27" src="https://github.com/user-attachments/assets/e1c6385e-c554-430f-8320-dbedcc4e3e80" />
<img width="996" height="676" alt="first_boot_1" src="https://github.com/user-attachments/assets/5313463f-9ab3-4834-8a7c-00ccd6776690" />
<img width="1449" height="847" alt="first_boot_3" src="https://github.com/user-attachments/assets/95cc7979-6069-46c0-8593-4a73c420d1e2" />
<img width="1300" height="844" alt="first_boot_5" src="https://github.com/user-attachments/assets/0a9e508d-5ab6-4697-aad4-d0d25fdcf86a" />
<img width="1282" height="834" alt="update_install_1" src="https://github.com/user-attachments/assets/3c97ee2e-1ce4-467e-898b-9f3211a14e14" />
<img width="1283" height="842" alt="update_install_6" src="https://github.com/user-attachments/assets/7e3353f3-a613-4596-add5-b9d989bf4692" />

## Useful for
- Secure environment creation
- SOC Analyst / penetration testing practice


This repo shows how I built modern cybersecurity environments.
