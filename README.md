<img src="https://raw.githubusercontent.com/acidanthera/OpenCorePkg/master/Docs/Logos/OpenCore_with_text_Small.png" width="200" height="48"/>

#  MSI GL62M 7RDX Hackintosh Laptop 

This is an Opencore 0.6.6 install for MacOS Big Sur 11.2 .

It only boot for macos Big Sur , Windows would be crash .


## How to boot in Windows

Switch boot drive from BIOS .

## Screenshots

<img src=https://raw.githubusercontent.com/vincent-chang-rightfighter/GL62M-7RDX-Hackintosh/main/Screenshots/About.png width="600"/>

## Specifications

**[ MSI GL62M 7RDX ](https://www.msi.com/Laptop/GL62M-7RDX/Specification)**

| Basic | Spec Sheet | Details |
|:--:|:--|:--:|
| CPU | Intel i7-7700HQ ||
| GPU | HD630 ||
| RAM | DDR4 2400Mhz 8GB * 2 ||
| Chipset | Intel HM175 ||
| Audio | Realtek ALC898 ||
| Ethernet | Atheros AR8175 ||
| Display | 15.6" 1920x1080 (eDP) ||
| WiFi | Broadcom DW1820A/BCM94350ZAE ||
| Drive 1 | Samsung 860 EVO 500GB 2.5" SSD | MacOS boot drive |
| Drive 2 | Adata SU800 256GB M.2 SSD | Windows boot drive |
| dGPU | GeForce® GTX 1050 with 2GB GDDR5 | MacOS not work |


## Need to Upgrade

### Wifi and Bluetooth

Replace the built-in intel Wifi Card to Broadcom DW1820A/BCM94350ZAE .

###  Samsung 860 EVO 500GB 2.5" SSD - Sata III 6 Gb/s

MacOS boot drive

### Adata SU800 256GB M.2 SSD - Sata III 6 Gb/s

Windows boot drive

## BIOS Configuration

The section below adapted from @0ranko0P's [MSI-GL62M 7RD Hackintosh](https://github.com/0ranko0P/GL62M-7RD-Hackintosh#bios-configuration). 


**Some options only available in advanced mode:**

In BIOS, hold **Shift ( Right ) + Ctrl ( Right ) + Alt ( Left )** together then press **F2**

| Settings |  |
|--|--|
| `CFG Lock` | Disable |
| `CSM` | Disable |
| Fast Boot | Disable |
| `Intel Speed Shift`(aka. HWP) | Enable |
| Secure Boot | Disable |
| Enable Hiberation | Disable |
| DVMT Pre-Allocated | 64M |

<pre>
[Advanced] tab
├─ Power & Performance
│  └─ CPU-Power Management Control
│     ├─ <b>Intel(R) Speed Shift Technology</b>
│     └─ CPU Lock Configuration
│        └─ <b>CFG Lock</b>
├─ System Agent (SA) Configuration
│  └─ Graphics Configuration
│     └─ DVMT Pre-Allocated
├─ CSM Configuration
│  └─ <b>CSM Support</b>
│   
└─ ACPI Settings
   └─ <b>Enable Hibernation</b>
</pre>

## Get Start

### [ Opencore Guide ](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html)


## Add Platforminfo Yourself

After install MacOS

You need to manually add [Platforminfo](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/kaby-lake.html#platforminfo) 
with [OpenCore Configurator](https://mackie100projects.altervista.org/download-opencore-configurator/)

<img src=https://raw.githubusercontent.com/vincent-chang-rightfighter/GL62M-7RDX-Hackintosh/main/Screenshots/Editinfo.png width=900/>

- Serial Number
- UUID
- MLB
- ROM

## Useful Info
- [Vanilla Laptop Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [MSI GP62 Hackintosh by Chuxubank](https://github.com/chuxubank/MSI-GP62-Hackintosh)
- [Hackintosh--MSIGL62M-7RDX by ForceGT](https://github.com/ForceGT/Hackintosh--MSIGL62M-7RDX)
- [GL62M-7RD-Hackintosh by 0ranko0P](https://github.com/0ranko0P/GL62M-7RD-Hackintosh)
- [hackintosh-msi-GL72M-7RDX by jbwharris](https://github.com/jbwharris/hackintosh-msi-GL72M-7RDX)