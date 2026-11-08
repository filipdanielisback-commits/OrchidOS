# Contributing to OrchidOS

Thank you for your interest in OrchidOS. At this stage, careful research and accurate documentation are especially valuable.

## Good first contributions

- Verify Moto G60 (`hanoip`) hardware facts with primary sources.
- Improve architecture, terminology, or licensing documentation.
- Add reproducible research notes with source links and dates.
- Review assumptions and identify unknowns.
- Propose small, independently testable experiments.

## Before opening a pull request

1. Check existing issues and pull requests to avoid duplicate work.
2. Explain the question or problem being addressed.
3. Link primary sources for hardware and kernel claims.
4. Clearly label facts, hypotheses, and unknowns.
5. Keep changes focused and include validation steps.
6. Preserve all upstream copyright notices and license files.

## Code and licensing

By submitting original code or documentation, you confirm that you have the right to contribute it under the repository's stated license. Original OrchidOS contributions are intended to be MIT-licensed unless a different license is agreed and clearly recorded.

Do not copy code from projects with incompatible or unclear licensing. Do not remove copyright headers. Imported XNU or other third-party files must retain their applicable upstream license and notices; see [docs/licensing.md](docs/licensing.md).

## Research quality

Prefer official documentation, source code, device trees, and reproducible measurements. Record the exact device variant and software/firmware version when relevant. A result from an emulator is not proof that the same feature works on physical hardware.

## Scope

This repository targets the Motorola Moto G60 (`hanoip`). General Darwin/XNU research is welcome when it directly supports that goal.
