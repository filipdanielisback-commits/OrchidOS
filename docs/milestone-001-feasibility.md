# Milestone 001 — XNU ARM64 Feasibility Report

**Status:** Initial desk research  
**Date:** 2026-11-08  
**Target:** Motorola Moto G60 (`hanoip`)  
**Decision:** Continue research; do not claim a port or begin device boot experiments.

## Executive summary

The upstream XNU project documents ARM64 support, and public Android device-source repositories exist for the Moto G60 / Moto G40 Fusion platform family identified as `hanoip`. This is enough to justify further architecture research, but it is not evidence that XNU supports the Moto G60.

The main gap is platform integration. ARM64 is an instruction-set architecture, not a guarantee that a kernel supports every ARM64 phone. OrchidOS would need to establish how the selected XNU revision expects its platform to provide early boot, memory management, interrupt handling, timers, clocks, power management, storage, and device-driver services. The Android device trees found in this review are useful evidence sources, but they are not XNU platform ports.

## Findings

### 1. XNU has ARM64 source support

Apple's public XNU README describes XNU as a hybrid kernel combining Mach, components from FreeBSD, and the I/O Kit driver API. It states that XNU runs on x86_64 and ARM64, and outlines major source-tree areas including configuration, kernel bootstrap, I/O Kit support, and syscall interfaces.

**What this establishes:** ARM64 is a supported architecture in the upstream XNU project.

**What it does not establish:** that a generic ARM64 configuration exists for the Moto G60, that the kernel supports Qualcomm's phone platform interfaces, or that an unmodified XNU build can boot on this device.

Source: https://github.com/apple-oss-distributions/xnu

### 2. Public Moto G60 / hanoip Android device sources exist

The public `motorola-sm6150-devs/android_device_motorola_hanoip` repository describes itself as an Android device tree for the Motorola Moto G40 Fusion / Moto G60 (`hanoip`). It includes Android build configuration, product files, and device-specific configuration.

A separate public `moto-hanoip` organization describes its repositories as device sources for the G40 Fusion and G60, but the organization is marked archived. This is useful historical material, not a guarantee of current maintenance.

Sources:
- https://github.com/motorola-sm6150-devs/android_device_motorola_hanoip
- https://github.com/moto-hanoip/

### 3. Preliminary hardware identification is corroborated, not fully verified

A public device-tree reference lists the platform as Qualcomm Snapdragon 732G, Kryo 470 CPU cores, and Adreno 618 graphics. The source covers the G40 Fusion / G60 family, so it should not be treated as proof of every regional G60 variant or board detail.

Source: https://github.com/TeamWin/android_device_motorola_hanoip

**Current confidence:** preliminary/corroborated for platform-family identification. Exact retail model, regional variant, board revision, memory layout, peripheral components, and firmware interfaces remain open research items.

### 4. Android device configuration is not an XNU port

Android device trees and kernel sources can help identify hardware, partition naming, firmware dependencies, and existing Linux driver coverage. They do not provide equivalent XNU drivers or prove that Android/Linux device interfaces can be reused by XNU.

OrchidOS must keep these categories separate:
- Hardware facts inferred from device-specific Android sources.
- Linux kernel implementation details.
- XNU architecture and platform requirements.
- OrchidOS hypotheses that still need testing.

## Initial feasibility assessment

| Area | Assessment | Reason |
|---|---|---|
| ARM64 architecture source | Promising starting point | Upstream XNU documents ARM64 support |
| Exact Moto G60 platform support in XNU | Not established | No Moto G60 XNU platform support identified in this review |
| Hardware documentation | Partial | Public Android device-source material exists |
| Driver availability | Major unknown | Android/Linux drivers are not automatically XNU drivers |
| Boot integration | Major unknown | Device-specific XNU boot path and platform initialization are not established |
| Darwin user space | Separate workstream | Kernel support alone does not supply a complete operating system |
| iOS compatibility | Not established / not claimed | Proprietary iOS components are outside the open-source XNU repository |

**Overall conclusion:** Research feasibility is plausible; a working port is unproven and likely requires substantial platform-specific engineering. No reliable basis exists yet for promising a bootable system or iOS application compatibility.

## Key blockers to investigate next

1. Select an exact XNU release/tag or commit and record its license.
2. Identify the exact Moto G60 retail model and regional variant.
3. Locate and inspect the matching device kernel source and device-tree source revisions.
4. Build a hardware inventory from source-backed evidence: CPU, RAM reservations, interrupt controller, timers, clocks, storage, display, touch, wireless, audio, and power management.
5. Map XNU's ARM64 platform assumptions against that inventory.
6. Identify a documented virtual research environment supported by the selected XNU revision; do not assume that ARM64 source support implies an available emulator target.
7. Publish a subsystem-by-subsystem gap analysis before proposing implementation work.

## Research boundaries

- No device flashing, bootloader modification, or boot-chain changes are part of this milestone.
- Do not copy Android device-tree content into OrchidOS without checking its license and provenance.
- Do not import XNU source under the repository's MIT license. Preserve the applicable upstream Apple license and notices.
- Do not claim iOS, SpringBoard, UIKit, or proprietary Apple framework support.
- Treat all device-specific assumptions as provisional until tied to the exact model and source revision.

## Milestone acceptance criteria

Milestone 001 is complete only when OrchidOS has:
- An exact XNU source revision and license record.
- An exact target-device identity record.
- A source-linked hardware evidence register.
- A documented XNU ARM64 platform-requirements map.
- A feasibility matrix identifying confirmed support, unknowns, and blockers.

This report is an initial baseline and does not by itself complete the milestone.
