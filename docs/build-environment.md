# Build Environment Plan

## Goal

Create a repeatable, documented environment for source study and controlled experiments. A successful toolchain setup does not demonstrate that XNU can boot on the Moto G60.

## Initial host requirements

Choose a supported Linux distribution or another environment documented by the selected upstream project. Record the exact release and architecture rather than relying on a floating "latest" setup.

Track these items:

- Host operating system and version.
- CPU architecture and available memory.
- Compiler and linker versions.
- Build utilities and scripting-language versions.
- Source repository URL and exact commit.
- Configuration files and build options.
- Checksums for downloaded release archives where applicable.

## Suggested repository organization

Keep downloaded upstream source outside the OrchidOS repository unless there is a clear licensing and maintenance reason to include it. Prefer scripts and documentation that identify reproducible source revisions.

Example local workspace:

```text
workspace/
  upstream/
    xnu/
  build/
  logs/
  orchid-notes/
```

This is an example directory layout only; it does not imply that a Moto G60 build configuration exists.

## Reproducibility record

Every experiment should include:

| Field | Value |
|---|---|
| Date | YYYY-MM-DD |
| Host OS | Exact name and version |
| Toolchain | Compiler / linker versions |
| Upstream source | URL and commit |
| Configuration | Exact config name and options |
| Command | Full command, excluding secrets |
| Result | Pass / fail / blocked |
| Logs | Relative path or artifact link |

## Safety and scope

Start with source inspection and controlled builds. Do not experiment on a daily-use phone or make boot-chain changes as part of the initial setup. Keep personal data and credentials out of logs and commits.

## First milestone

Produce a short report showing that the chosen upstream source revision can be fetched, inspected, and its documented build prerequisites understood. Do not mark the milestone complete merely because a compiler is installed.
