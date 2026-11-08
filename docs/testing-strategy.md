# Testing Strategy

## Principles

1. Prefer low-risk, repeatable tests.
2. Separate source-level analysis, host builds, virtualized experiments, and physical-device results.
3. Record exact source revisions and tool versions.
4. Make failures and unknowns visible.
5. Never infer hardware support from a successful compile alone.

## Test stages

### Stage A — Source and configuration review

- Identify the selected XNU revision.
- Review its license and supported architectures.
- Record relevant ARM64 platform assumptions.
- Compare the source configuration with documented target requirements.

### Stage B — Host-side checks

- Validate documentation links and repository structure.
- Run static checks on OrchidOS-authored scripts and configuration.
- Record tool versions and complete logs.

### Stage C — Controlled virtual research

Only use a virtual target that is explicitly documented as supported by the chosen source revision. Record what the virtual target proves and what it does not prove. A virtual boot is not evidence of Moto G60 hardware support.

### Stage D — Hardware feasibility review

Before any physical-device experiment is considered, require a reviewed hardware evidence register, a clear recovery and data-protection plan, and a narrowly scoped test objective. Initial OrchidOS work does not require changing a phone's boot configuration.

## Result record

For every test, capture:

- Test ID and date.
- Question being tested.
- Environment and hardware identity.
- Source commit and configuration.
- Steps performed at a high level.
- Expected and observed results.
- Logs and relevant artifacts.
- Limitations and follow-up work.

## Acceptance rule

A test passes only when its expected result is defined in advance and the result can be reproduced. "It compiled" and "it did not crash immediately" are not sufficient acceptance criteria for platform support.
