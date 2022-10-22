# Thinkpad-T460-MacOS-BigSur-OC
EFI folder for installing MacOS Big Sur on Thinkpad T460 with Intel Wifi

Based on [hasodikis's](https://github.com/Hasodikis/ThinkPad_t460_Hackintosh_OpenCore) release for OC v0.7.5 with [quakehc`s](https://www.tonymacx86.com/members/quakehc.2619209/) instructions for adapting to Intel Wifi cards(with Airportitlwm.kext).

This version is adapted for multibooting another Windows/Linux OS by adding ext4_x64.efi driver and configuring OC bootloader to properly show up at each boot.
Multiboot tested with Windows 10 and Linux Mint 20 simultaneously.

**Before doing anything please backup your data!!!**

Make sure your drive is GPT partitioned and EFI partition is at least 200MB.
USB drive for installation should also be GPT partitioned.

Add your platformInfo into config.plist(can be done semi-automatically with GenSMBIOS or manually with ProperTree/any text editor). 

For downloading MacOS image, bootable USB creation, install process and troubleshooting refer to [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/). 

# Laptop's Hardware
- <b>Model</b>: Thinkpad T460 (20FMS1JA00)
- <b>Bios</b>: 1.45
- <b>CPU</b>: Intel(R) Core(TM) i5-6300U CPU @ 2.40GHz
- <b>GPU</b>: Intel HD Graphics 520
- <b>Storage</b>: Crucial MX500 512GB SSD
- <b>RAM</b>: 8 GB PC3L-12800 1600MHz DDR3L
- <b>Screen</b>: 14" FHD (1920x1080) IPS
- <b>Wi-Fi</b>: Intel Wireless - AC 8260
- <b>Ethernet</b>: Intel I219-V PCIe Gigabit Ethernet
- <b>Sound</b>: Realtek ALC3245 (same as ALC239)
- <b>Camera</b>: 720p
- <b>Battery</b>: 3-cell (23Wh) + 3-cell (23Wh)

# Bios settings

<b>Security</b>
- `Security Chip` **Disabled**
- `Memory Protection -> Execution Prevention` **Enabled**
- `Virtualization -> Intel Virtualization Technology` **Enabled**
- `Virtualization -> Intel VT-d Feature` **Enabled**
- `Anti-Theft -> Computrace -> Current Setting` **Disabled**
- `Secure Boot -> Secure Boot` **Disabled**
- `Intel SGX -> Intel SGX Control` **Disabled**
- `Device Guard` **Disabled**

<b>Startup</b>
- `UEFI/Legacy Boot` **UEFI Only**
- `CSM Support` **No**

# What's Working?
- [x] Intel HD 520 Graphics (incuding graphics acceleration)
- [x] CPU Power Management
- [x] Battery
- [x] All USB ports
- [x] HDMI port (including HDMI Audio)
- [x] Intel I219V Ethernet port
- [x] Realtek ALC239 Audio (including headphones jack)
- [x] Wi-Fi & Bluetooth (including Apple services)
- [x] Internal camera (including Facetime)
- [x] Trackpad, Trackpoint and physical buttons (including gestures)
- [x] Sleep / Wake / Shutdown / Reboot (lid sleep and lid wake)
- [x] Keyboard (incuding all fn Keys using [ThinkpadAssistant](https://github.com/MSzturc/ThinkpadAssistant))
- [x] iMessage, FaceTime, App Store, iTunes Store (with valid smbios)
- [x] DRM support (iTunes Movies, Apple TV+, Amazon Prime and Netflix, and others)
- [x] SD Card Reader (v2.2 works but still a bit unstable)

# What's not working ⚠️
- [ ] Fingerprint Reader (will never work since no drivers available)
- [ ] Sidecar Wireless (doesn't work without apple native WIFI card)
