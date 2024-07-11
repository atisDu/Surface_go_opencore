![OpenCore logo](https://github.com/acidanthera/OpenCorePkg/raw/master/Docs/Logos/OpenCore_with_text_Small.png)

# Surface-Go-OpenCore
macOS on the Pentium Gold Y4415 Microsoft Surface Go (4gb / eMMC model)  thanks to [Acidanthera's OpenCore bootloader](https://github.com/acidanthera/OpenCorePkg).

# The big issues
macOS only works with eMMC storage with the [EmeraldSDHC kext](https://github.com/acidanthera/EmeraldSDHC) which as of writing this (11.07.2024) does not seem to work with the SD host controller found in the Surface Go (4gb / eMMC). Even legacy ATA controller kexts dont work.
The latest macOS recovery that is working is macOS 12 Monterey. 
The wifi card (Atheros QCA 6174) does not work in macOS, and since the Surface Go lacks an ethernet port your only option would be either an external ethernet dongle or usb wifi card.

# How to make it boot
Recovery boots with cpuid spoof, since cpu's outside the core series aren't officially supported and are not found in official intel macs.
Follow the [Dortania OpenCore install guide](https://dortania.github.io/OpenCore-Install-Guide/) for installation on laptop kaby lake cpu's or use the provided config.plist, but change the PlatformInfo SMBIOS, for which a guide can be found in the opencore install guide.



## Disclaimer
This repository is neither a howto nor an installation manual. Using these files requires at least basic knowledge of [Acidanthera's OpenCore bootloader](https://github.com/acidanthera/OpenCorePkg), ACPI, UEFI and the art of hackintoshing in general. I recommend reading the excellent [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide), as well as all its linked resources.
