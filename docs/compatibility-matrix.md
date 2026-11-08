# Compatibility Matrix

## Status definitions

- **Unknown:** no adequate evidence yet.
- **Researching:** sources and requirements are being investigated.
- **Prototype:** a limited experiment exists; not production support.
- **Working in test environment:** repeatable tests pass in a named environment.
- **Working on Moto G60:** demonstrated on the exact target device with reproducible evidence.
- **Not applicable:** the feature is outside project scope.

No feature should be marked "working on Moto G60" without test evidence tied to an exact hardware variant and software revision.

## Current matrix

| Area | Status | Evidence needed |
|---|---|---|
| XNU ARM64 source study | Researching | Selected upstream revision and subsystem report |
| ARM64 kernel build | Unknown | Reproducible build record for a named configuration |
| Emulator / virtual target | Unknown | Selected target and documented repeatable test |
| Moto G60 board description | Researching | Device-specific sources and verified identifiers |
| Boot integration | Unknown | Architecture report and controlled proof of concept |
| Memory management | Unknown | Platform-specific requirements and test evidence |
| Interrupts and timers | Unknown | Controller and timer documentation |
| Display | Unknown | Display-controller and panel research |
| Touch and input | Unknown | Controller and input-stack research |
| Storage | Unknown | Controller, media, and filesystem research |
| Wi-Fi / Bluetooth | Unknown | Chipset identity, firmware requirements, and driver research |
| Audio | Unknown | Codec and audio-path research |
| Power / thermal | Unknown | PMIC, regulator, thermal, and clock documentation |
| Darwin user space | Unknown | Component inventory and dependency analysis |
| iOS application compatibility | Not a current claim | Proprietary platform dependencies are outside open XNU scope |

## Updating this matrix

When changing a status, link the relevant report, test log, source revision, and date. A successful build on a host or emulator must not be presented as proof of support on physical hardware.
