# ASUS VivoBook K15 OLED (K513EA) — macOS Sequoia

Community Hackintosh notes for the ASUS VivoBook K15 OLED K513EA.

## Target hardware

- Laptop: ASUS VivoBook K15 OLED K513EA
- CPU: Intel Core i5-1135G7 (Tiger Lake-U)
- iGPU: Intel Iris Xe
- RAM: 8 GB (reported configuration)
- Display: built-in OLED panel
- Wireless: Realtek (exact chipset must be identified before selecting a driver)

## Current project status

- Primary target: macOS Sequoia 15
- The supplied EFI was reported by the owner to boot Sequoia and to include a working graphics configuration.
- This report is user-provided; this repository has not independently certified every device, sleep/wake, power-management, audio, wireless, or graphics function.
- Metal 3 availability is not claimed.
- macOS Tahoe 26 and later versions are future, separately tested targets—not guaranteed by the Sequoia EFI.

## EFI archive

The sanitized EFI archive is prepared separately as `K513EA_Sequoia_EFI_Sanitized.zip`. It is not attached to this commit because the connected GitHub file-write interface supports text files, not direct binary archive transfer. Upload the ZIP through the GitHub web interface or attach it to a GitHub Release.

Before using the EFI, generate your own unique SMBIOS values (Serial Number, MLB, SystemUUID, and ROM) with the appropriate OpenCore tooling. The distributed archive has these values blanked/neutralized. Never reuse another person's identifiers.

## Important notes

- Back up your data and existing EFI before making changes.
- Do not overwrite Windows partitions or existing boot files without a verified backup.
- Confirm the exact Wi-Fi chipset, audio codec, touchpad, and other hardware IDs on your own unit.
- Review the OpenCore configuration and kext/ACPI compatibility before booting.
- Do not assume an EFI for Sequoia will work unchanged on macOS 26/27. Maintain separate version-specific configurations and validate each update.

## Disclaimer

This is an experimental, hardware-specific community project. No warranty or guarantee of functionality is provided. macOS is Apple software; use only in accordance with Apple's applicable terms and your local laws.
