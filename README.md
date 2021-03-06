# Lenovo-M435-Hackintosh
## Just for backup

## Specification
| **Component** | **Model** |
| ------------- | --------- |
| CPU | Intel i5-10500 |
| Motherboard | Intel B460 |
| RAM | 16GB DDR4-2933 |
| GPU | Intel® UHD Graphics 630 + NVIDIA GeForce GT 710(HDMI, DIV, VGA) |

**macOS version**: 11.2.3
**OpenCore version**: 0.6.7

## How to use

1. Make your USB installer with [**this guide**](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
2. Clone the repository and paste "BOOT" and "OC" directories into your's pendrive "EFI" folder
3. Download [**GenSMBIOS**](https://github.com/corpnewt/GenSMBIOS) to generate unique SMBIOS information. Run it and select **Generate SMBIOS**, as the model select **iMac20,1**.
4. Open config.plist with [**ProperTree**](https://github.com/corpnewt/ProperTree) and go to PlatformInfo > Generic. Set MLB (Board Serial), SystemSerialNumber (Serial) and SystemUUID (SmUUID) to generated values. Change ROM to your network card's MAC address without the `:` character. [**How to get MAC Address?**](https://www.wikihow.com/Find-the-MAC-Address-of-Your-Computer)
5. Boot it!

## All work

- CPU
- Dual monitors (HDMI & DIV & VGA)
- Audio
- Ethernet
- USB
- App store, iCloud, iMessage, iTunes, FaceTime, etc
- Sleep, Wakeup, Shutdown, Restart

## HIDPI fix

```bash
git clone https://github.com/mlch911/one-key-hidpi.git
cd one-key-hidpi
./hidpi.command
```

# Solve the problem of not being able to add applications to "Privacy-Accessibility"

```bash
sudo chmod 777 /Library/Application\ Support/com.apple.TCC
sudo rm -rf /Library/Application\ Support/com.apple.TCC/TCC.db
```