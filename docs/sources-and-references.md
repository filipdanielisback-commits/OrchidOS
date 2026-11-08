# Sources and References

## Purpose

This file is the index for technical references used by OrchidOS. Each project claim should point to a specific source and, where possible, an exact source revision.

## Primary upstream sources

- Apple Open Source: https://opensource.apple.com/
- XNU source repository: https://github.com/apple-oss-distributions/xnu
- Android Open Source Project: https://source.android.com/
- Linux kernel documentation: https://docs.kernel.org/
- Arm developer documentation: https://developer.arm.com/documentation

These sources provide background and source material. They do not establish that a given XNU revision supports the Moto G60.

## Device-specific sources to collect

- Motorola support and product documentation for the exact Moto G60 model.
- Manufacturer-published kernel source corresponding to the device's software release.
- Device-specific kernel and device-tree repositories, with exact commits.
- Public hardware documentation for identified controllers and components.

## Citation record format

For each reference, record:

| Field | Description |
|---|---|
| Title | Document or repository name |
| URL | Canonical URL |
| Publisher | Organization or maintainer |
| Revision | Commit, tag, document version, or release |
| Date checked | YYYY-MM-DD |
| Supports | Exact claim(s) supported |
| Limitations | What the source does not establish |

## Evidence discipline

Do not cite a generic Snapdragon specification as proof of the Moto G60's full board layout. Do not cite an Android device tree as proof that XNU has equivalent driver support. Keep upstream facts, target-device facts, and OrchidOS hypotheses clearly separated.
