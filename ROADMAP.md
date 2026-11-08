# OrchidOS Roadmap

This roadmap describes research goals, not promised delivery dates. A milestone is complete only when its results are documented and independently reproducible.

## Phase 0 — Project foundation

- [x] Establish project scope and target device.
- [x] Add initial documentation and contribution policies.
- [ ] Record authoritative references for the Moto G60 hardware.
- [ ] Establish a reproducible development environment.
- [ ] Review XNU source layout and its licensing requirements.

## Milestone 001 — XNU ARM64 feasibility

- [x] Review the upstream XNU project overview and confirm documented ARM64 support.
- [x] Identify public `hanoip` Android device-source repositories.
- [x] Record initial feasibility findings and major unknowns in [the report](docs/milestone-001-feasibility.md).
- [ ] Select and record an exact XNU source revision and license.
- [ ] Verify the exact Moto G60 model and regional variant.
- [ ] Build a source-linked hardware evidence register.
- [ ] Map XNU ARM64 platform requirements against verified device evidence.
- [ ] Select a documented virtual research target, if supported by the chosen XNU revision.

## Phase 1 — Architecture research

- [ ] Map the major XNU subsystems relevant to ARM64.
- [ ] Document the differences between XNU, Darwin user space, and Apple's proprietary platform components.
- [ ] Identify the boot and platform interfaces that a port would need.
- [ ] Complete an evidence-backed feasibility report with explicit unknowns.

## Phase 2 — Controlled test environment

- [ ] Select a documented emulator or virtual research target.
- [ ] Record toolchain versions and build prerequisites.
- [ ] Establish a minimal repeatable build/test workflow.
- [ ] Add diagnostic and test documentation.

## Phase 3 — Moto G60 platform investigation

- [ ] Verify the exact Moto G60 variant and board details.
- [ ] Document CPU, memory, interrupt, timer, clock, and power-management information from reliable sources.
- [ ] Map peripheral controllers and identify available documentation.
- [ ] Separate confirmed facts from inferred or unknown details.

## Phase 4 — Feasibility prototypes

- [ ] Define a minimal platform abstraction plan.
- [ ] Evaluate kernel build feasibility without claiming device boot support.
- [ ] Design safe diagnostic milestones and acceptance criteria.
- [ ] Publish results, blockers, and next steps.

## Phase 5 — Hardware and user-space research

- [ ] Assess display, input, storage, USB, networking, audio, and power support.
- [ ] Investigate driver architecture and licensing constraints.
- [ ] Study compatible Darwin user-space components.
- [ ] Evaluate graphical-environment requirements separately from kernel support.

## Non-goals and constraints

- This project does not contain Apple's proprietary iOS source code.
- A Darwin/XNU kernel is not equivalent to a complete iOS system.
- No specific hardware feature is considered supported until it has been tested and documented.
- Device-specific boot work is not a starting milestone; controlled research and verified documentation come first.
