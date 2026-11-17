# Compatibility and validation matrix

This document separates owner-reported behavior from independently verified results. Unknown means not yet tested—not supported or unsupported.

## Target device

- ASUS VivoBook K15 OLED K513EA
- Intel Core i5-1135G7 (Tiger Lake-U)
- Intel Iris Xe iGPU
- 8 GB RAM (owner-reported)

## Operating-system targets

| OS | Role | Status | Evidence required |
|---|---|---|---|
| macOS Sequoia 15 | Primary | Owner reports supplied EFI is working; exact build not yet recorded here | Boot log, About This Mac, hardware test checklist |
| macOS Tahoe 26 | Secondary/future | Not validated | Version-matched OpenCore, kext and graphics tests |
| macOS 27 | Future | Unknown | Upstream support and physical-device tests |

## Feature matrix

| Feature | Current evidence | Status |
|---|---|---|
| EFI boot | Owner reports working original EFI | Reported working |
| Intel Iris Xe acceleration | Owner reports graphics fix working | Reported working; not independently benchmarked |
| Metal 3 | Owner says unavailable | Not available per owner report; exact Metal feature set unverified |
| Wi-Fi / Bluetooth | Realtek family reported; exact IDs unknown | Needs identification |
| Audio | Not documented | Unknown |
| OLED brightness | Not documented in this release | Unknown |
| USB mapping | Not independently checked | Unknown |
| Battery reporting | Not documented | Unknown |
| Sleep / wake | Not documented | Unknown |
| CPU power management | Not independently checked | Unknown |

## Required validation before calling a release "working"

1. Record the exact macOS version and build.
2. Record OpenCore and kext versions.
3. Confirm the exact PCI IDs and internal device IDs.
4. Verify boot, graphics acceleration, display output and brightness.
5. Test audio, Wi-Fi, Bluetooth, USB ports and input devices.
6. Test battery reporting, CPU power management, sleep and wake.
7. Review logs for recurring errors.
8. Test from a separate USB EFI and retain a known-good backup.

## Graphics and Metal terminology

Graphics acceleration, Metal API availability, and support for specific Metal feature families (including Metal 3 capabilities) are distinct. Do not claim Metal 3 support solely because the desktop is accelerated. Record the actual OS-reported GPU and Metal capabilities from the target installation.

## Privacy

Never commit a real SMBIOS Serial Number, MLB, SystemUUID, ROM, personal account identifiers, Wi-Fi credentials, or unredacted logs. The sanitized distribution EFI uses neutralized SMBIOS fields; generate unique local values before use.
