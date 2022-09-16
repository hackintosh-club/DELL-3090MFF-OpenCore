# DELL 3090 MFF Hackintosh OpenCore EFI

### [简体中文](README.zh_CN.md)

### OpenCore

[OpenCore 0.8.4](https://github.com/acidanthera/OpenCorePkg)

### OS Version Tested

- macOS Monterey 12.x
- macOS Ventura  13.x 

### Hardware

- Motherboard: DELL Q470
- Bios Version: 2.4.0
- CPU: i5-10500t
- RAM: Samsung 2x16GB DDR4 3200
- SSD: West Digital SN750 500G
- iGPU: Intel UHD Graphic 630
- Audio: Realtek ALC256
- Ethernet Card: Intel I219-LM
- Wireless: BCM94360CS2
- PSU: DELL 65W 

### Bios Setup

| Name | Option |
| ----- | --- |
| System Configuration → SATA Operation | AHCI |
| Security → PTT Security/PTT On | Disabled |
| Secure Boot → Secure Boot Enable | Disabled |
| PSecure Boot → Secure Boot Mode | Audit Mode |
| Intel Software Guard Extensions → Intel SGX Enable | Disabled |
| Power Management → Deep Sleep Control | Disabled |
| Power Management → USB Wake Support | Disabled |
| Power Management → Wake on LAN/WLAN | Lan only |
| Power Management → Block Sleep | Disabled |
| POST Behavior → Fastboot | Minimal |
| Virtualization Support → VT For Direct I/O | Disabled |

### Notes
 - Use [OpenCore Configurator](https://mackie100projects.altervista.org/opencore-configurator/) build your own SMBIOS
 
 - Use [RU.efi](http://ruexe.blogspot.com/) Unlock CFG LOCK , Change DVMT = 64MB
 
| Option | UEFI Variable Name | Address | Default | Replace |
| --- | --- | --- | --- | --- |
| CFG LOCK | CPUSetup | 0x3E | 0x1 | 0x0 |
| DVMT | SaSetup | 0xF5 | 0x0 | 0x2 |

- Unlock CFG LOCK Address:0x3E  01 (Enabled) Replace 00（Disabled）
![image](https://github.com/hackintosh-efi/DELL-3090MFF-OpenCore/blob/main/RU/cpusetup.png)

- Change DVMT Address:0xF5  00（Default） Replace 02（64MB）
![image](https://github.com/hackintosh-efi/DELL-3090MFF-OpenCore/blob/main/RU/sasetup.png)


### ScreenShot 

- About This Mac
![image](https://github.com/hackintosh-efi/DELL-3090MFF-OpenCore/blob/main/ScreenShot/关于本机.png)