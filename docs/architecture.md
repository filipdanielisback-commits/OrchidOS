# OrchidOS Architecture — Initial Notes

**Status:** preliminary research outline  
**Target:** Motorola Moto G60 (`hanoip`)

## 1. What is being investigated?

OrchidOS investigates whether and how an open-source Darwin/XNU kernel could be adapted to the Moto G60 platform. This is a substantial porting and compatibility problem, not a matter of placing an existing kernel image on an Android device.

XNU combines Mach, BSD, and I/O Kit components with architecture- and platform-specific code. A usable operating-system environment also needs boot integration, drivers, system libraries, services, and applications. Apple's complete iOS platform includes proprietary components that are not supplied by the open-source XNU repository.

## 2. Conceptual layers

1. **Build environment:** pinned compiler, SDK/toolchain components, scripts, and reproducible build instructions.
2. **Kernel:** XNU source and any separately maintained, clearly licensed platform adaptations.
3. **Platform layer:** CPU setup, memory management, interrupt handling, timers, clocks, and power interfaces.
4. **Boot integration:** a documented handoff from the platform's boot environment to the kernel.
5. **Drivers:** hardware-specific support for peripherals and SoC blocks.
6. **User space:** compatible libraries, process startup, services, and command-line tools.
7. **Graphical environment:** display stack, compositor/windowing, input, and applications.

These are conceptual work areas. They are not implemented merely because directories exist in the repository.

## 3. Research sequence

The initial sequence is documentation-first and emulator-first:

- Understand the upstream XNU architecture and build system.
- Record the exact target hardware and available public documentation.
- Identify platform assumptions in the relevant XNU code.
- Define a controlled test target and diagnostic strategy.
- Evaluate feasibility before attempting any device-specific integration.

## 4. Evidence standard

Every technical note should distinguish:

- **Verified:** directly supported by a primary source or reproducible test.
- **Observed:** measured or inspected, with device/software details recorded.
- **Hypothesis:** plausible but not yet demonstrated.
- **Unknown:** insufficient information.

An emulator result must not be presented as physical-device support. A successful kernel build must not be presented as a successful boot.

## 5. Open questions

- Which XNU revision and license-compatible source baseline should be studied?
- Which ARM64 platform assumptions can be reused, and which are tied to Apple's hardware?
- What trustworthy public documentation exists for the Moto G60 board and its boot environment?
- Which required hardware interfaces are documented well enough to evaluate?
- What is the smallest meaningful and testable proof of feasibility?

## 6. Explicit boundary

OrchidOS is not an iOS 18 port, does not include proprietary Apple frameworks or firmware, and does not currently claim to boot XNU on the Moto G60.
