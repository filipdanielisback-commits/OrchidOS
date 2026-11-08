# Boot Architecture Research

**Status:** conceptual notes only; no OrchidOS bootloader is implemented.

## Questions to answer

A future port would need a documented path from the device's existing boot environment to an ARM64 kernel. Research must establish, rather than assume:

- What firmware and boot stages are present on the exact Moto G60 variant?
- Which stage loads the operating-system kernel and supplies its entry state?
- How are memory regions and reserved areas described?
- How are device information and hardware descriptions passed forward?
- What exception level and processor state does the kernel receive?
- How are caches, MMU state, interrupts, and timers expected to be configured?
- Which verified recovery mechanisms exist for the target?

## Required deliverables before implementation

1. A source-backed diagram of the existing boot flow.
2. A glossary for the platform's boot terminology.
3. A documented kernel handoff contract.
4. A list of unresolved assumptions and risks.
5. A controlled test plan with clear stop conditions.

## Important distinction

A bootloader, a kernel, and an operating-system user space are separate components. Loading a kernel is not proof that the kernel can initialize the platform, and kernel initialization is not proof that a complete operating-system environment is available.

This document intentionally avoids device-modification instructions. No boot-chain changes should be attempted as part of the initial research phase.
