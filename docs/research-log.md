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

### Next research tasks

- Verify the exact Moto G60 hardware variant and board identity.
- Identify maintained device-specific kernel/device-tree sources.
- Select an upstream XNU revision for source study and document its license.
- Write an evidence-backed ARM64/XNU feasibility report.
