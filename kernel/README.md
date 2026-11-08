# Kernel Research

This directory is reserved for OrchidOS-authored kernel research and future code that is appropriately licensed.

## Current status

No Moto G60 XNU port or working kernel configuration is present.

## Research priorities

- Select and record an exact upstream XNU revision.
- Map relevant Mach, BSD, I/O Kit, and ARM64 components.
- Identify assumptions tied to Apple's platform hardware.
- Document build prerequisites and configuration limitations.
- Keep upstream source separate unless importing it is necessary and its license obligations are satisfied.

## Licensing

Do not copy XNU source into this directory under the repository's MIT license. Preserve the applicable Apple Public Source License version, copyright notices, and source provenance for any imported or modified upstream files. See [../docs/licensing.md](../docs/licensing.md).
