# XNU Subsystem Research Notes

## Purpose

This document identifies major XNU areas that OrchidOS should study before attempting platform-specific work. It is a research map, not a porting recipe or a claim of compatibility.

## High-level structure

XNU combines several major technologies:

- **Mach:** tasks, threads, virtual memory, scheduling, and low-level kernel abstractions.
- **BSD layer:** process and credential models, file systems, networking interfaces, and POSIX-facing kernel services.
- **I/O Kit:** an object-oriented driver framework used by Apple's systems.
- **Architecture-specific code:** CPU setup, exception handling, memory management, timers, and interrupt handling for supported architectures.
- **Kernel support components:** synchronization, IPC, security mechanisms, and other shared facilities.

The exact layout and supported configurations depend on the selected upstream XNU revision.

## Questions to answer

1. Which XNU revision is being studied, and what architectures does that revision support?
2. Which ARM64 platform assumptions are generic and which are tied to Apple's hardware?
3. What platform services are expected before general kernel services can operate?
4. Which I/O Kit services or driver families are available in source, and which depend on unavailable components?
5. What user-space services are required for a useful Darwin environment?

## Research method

For every finding, record the source file or official document, upstream revision, date checked, and confidence level. Do not infer that a subsystem is portable merely because source code is present.

## Important boundary

XNU is not the complete Darwin user space and is not the complete iOS operating system. SpringBoard, UIKit, proprietary frameworks, signing services, and device-specific Apple components are separate matters and are not supplied by an open-source XNU checkout.

## References to add

- Official Apple Open Source XNU source repository and the license file for the exact revision studied.
- XNU source documentation and architecture-specific source comments.
- Public ARM architecture documentation relevant to the target CPU.
- Device-specific Moto G60 documentation, where available.
