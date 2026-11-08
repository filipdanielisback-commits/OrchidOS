# OrchidOS Research Log

This log records project findings and decisions. Add dates in ISO format (`YYYY-MM-DD`) and link evidence for technical claims.

## 2026-11-08 — Project baseline

- Established the project name: OrchidOS.
- Scope set to Motorola Moto G60 (`hanoip`) only.
- Main research goal: investigate the feasibility and requirements of a genuine Darwin/XNU port.
- Clarified that open-source XNU is not the complete iOS operating system.
- Set a documentation-first, controlled-test-first approach.
- Added initial project policies and architecture notes.

### Current state

No kernel port, bootloader, device driver, bootable image, or iOS-compatible user environment is claimed.

## 2026-11-08 — Milestone 001 initial desk research

- Reviewed the upstream Apple XNU repository README; it documents ARM64 support, but does not establish Moto G60 platform support.
- Identified public Android device-tree material for the Moto G40 Fusion / Moto G60 family under the `hanoip` codename.
- Identified an archived `moto-hanoip` source organization; archived material is historical reference, not evidence of active maintenance.
- Recorded Snapdragon 732G / Adreno 618 as preliminary platform-family identification requiring exact model and source-revision verification.
- Added [the initial feasibility report](milestone-001-feasibility.md).

### Initial assessment

ARM64 source support makes further research reasonable. It does not mean XNU can boot on an arbitrary ARM64 phone. The major unknowns are platform initialization, memory layout, interrupts, timers, clocks, power management, boot integration, and driver availability. Android/Linux device sources are evidence about the hardware and existing software ecosystem, not ready-made XNU drivers.

### Current state

The project remains in research/planning. No kernel port, bootloader, device driver, bootable image, or iOS-compatible user environment is claimed.

### Next research tasks

- Identify the exact Moto G60 retail model and regional variant.
- Locate the matching kernel source and device-tree revisions, and record their licenses.
- Select an exact upstream XNU release/tag or commit and record its license.
- Build a source-linked hardware inventory.
- Map XNU ARM64 platform assumptions against verified device evidence.
- Identify a documented virtual research target supported by the selected XNU revision.
