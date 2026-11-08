# Hardware Evidence Register

## Purpose

This register defines how OrchidOS records hardware facts about the Motorola Moto G60 (`hanoip`). It prevents assumptions based on a similarly named phone or a related Qualcomm platform from becoming project facts.

## Evidence levels

| Level | Meaning |
|---|---|
| Confirmed | Supported by a primary device-specific source or repeatable, documented observation |
| Corroborated | Supported by multiple independent, credible sources |
| Tentative | Plausible, but based on incomplete or indirect evidence |
| Unknown | Not yet established |
| Contradicted | Reliable evidence conflicts with the current claim |

## Initial target identity

| Field | Current entry | Confidence |
|---|---|---|
| Commercial device | Motorola Moto G60 | Project target |
| Device codename | `hanoip` | To be cross-checked against device-specific sources |
| SoC family | Qualcomm Snapdragon 732G | Preliminary; verify exact variant |
| CPU architecture | ARM64 | Expected from the SoC platform; verify |
| GPU | Qualcomm Adreno 618 | Preliminary; verify |

These entries are starting hypotheses for research, not a verified board specification.

## Required evidence

- Exact model number and regional variant.
- Board/platform identifiers and revision information.
- SoC and CPU configuration.
- Physical memory size and memory layout.
- Interrupt controller and timer information.
- Storage controller and boot-storage arrangement.
- Display pipeline, panel identity, and touch controller.
- Wi-Fi, Bluetooth, audio, camera, USB, and sensor components.
- Power-management IC, regulators, clocks, and thermal sensors.
- Firmware interfaces and documented boot architecture.

## Source quality

Prefer, in order:

1. Manufacturer documentation and official source releases.
2. Device-specific kernel source and device trees from the manufacturer or maintainers.
3. Reproducible observations with commands, tool versions, and redaction of personal data.
4. Multiple independent technical references.

Avoid treating forum posts, generic SoC marketing pages, or device-family assumptions as definitive board documentation.

## Evidence entry template

For each claim, record:

- Claim:
- Value:
- Source URL or repository path:
- Exact source revision / publication date:
- Date checked (UTC):
- Evidence level:
- Notes and unresolved questions:

Do not publish serial numbers, IMEIs, account identifiers, Wi-Fi credentials, or other personal device data.
