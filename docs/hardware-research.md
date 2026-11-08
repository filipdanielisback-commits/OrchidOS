# Moto G60 Hardware Research

**Target codename:** `hanoip`  
**Status:** initial inventory; verify all details against the exact device variant.

## Known target identity

| Field | Current project target | Evidence status |
|---|---|---|
| Manufacturer | Motorola | Target identification |
| Device | Moto G60 | Target identification |
| Codename | `hanoip` | Commonly used device codename; verify against device-specific sources |
| SoC family | Qualcomm Snapdragon 732G | Preliminary; verify exact variant |
| CPU ISA | ARM64 | Expected for this platform; verify from authoritative documentation |
| GPU | Adreno 618 family | Preliminary; verify exact SoC/platform documentation |

This table is a starting inventory, not a validated board specification. Do not infer the complete memory map, interrupt controller configuration, firmware interface, or peripheral wiring from the SoC name alone.

## Information still needed

- Exact model/region variant and board revision.
- RAM configuration and physical memory layout.
- CPU topology and architectural feature set.
- Interrupt controller and interrupt routing.
- Generic and SoC-specific timers.
- Clock, reset, and power-management controllers.
- Storage controller and boot media arrangement.
- Display pipeline, panel, and refresh modes.
- Touch controller and input interfaces.
- Wi-Fi, Bluetooth, audio, USB, and sensor connectivity.
- Firmware interfaces and documented boot handoff.
- Existing device-tree and kernel configuration references.

## Source quality

Prioritize, in order:

1. Official Motorola documentation and support material.
2. Qualcomm platform documentation that is publicly available.
3. Maintained device trees and kernel source for the exact `hanoip` target.
4. Reproducible observations from the exact device variant.
5. Community reports, clearly labelled as secondary evidence.

For each finding, record the source URL, retrieval date, applicable device variant, software version, and confidence. Do not copy proprietary firmware or undocumented blobs into this repository.

## Research record template

For each hardware claim, record:

- **Claim:**
- **Status:** verified / observed / hypothesis / unknown
- **Device variant:**
- **Software or firmware version:**
- **Source(s):**
- **How it was checked:**
- **Limitations / open questions:**

## Safety and data integrity

Early research should remain in documentation, source review, and controlled test environments. Do not experiment with boot partitions or firmware on a daily-use device as an initial project step. Any future device testing requires a reviewed plan, reliable recovery documentation, and a clear understanding of the risks.
