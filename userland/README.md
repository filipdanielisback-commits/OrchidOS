# Darwin User-Space Research

This directory is for research into the user-space components needed above a Darwin/XNU kernel.

## Scope

A kernel alone is not a complete operating system. Research must distinguish:

- Kernel interfaces and system calls.
- Core Darwin user-space libraries and services.
- Shells and command-line tools.
- Service management and system initialization.
- Graphics and window-system components.
- Application frameworks and platform-specific services.

## Important distinction

Open-source Darwin components do not provide the complete proprietary iOS platform. SpringBoard, UIKit, many Apple frameworks, signing infrastructure, and device-specific services are not included simply by building XNU.

## Current status

No iOS compatibility or graphical iOS environment is claimed. Begin with a component inventory and dependency map.
