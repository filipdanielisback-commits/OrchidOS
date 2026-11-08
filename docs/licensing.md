# Licensing and Third-Party Code Policy

## Original OrchidOS work

Unless a file or directory says otherwise, original material authored for OrchidOS is intended to be licensed under the MIT License in the repository root.

Contributors should only submit material they have the right to license under those terms. Keep copyright and SPDX notices accurate.

## Imported and adapted code

The root MIT license does **not** automatically apply to third-party code. Before importing or adapting any component:

1. Identify the exact upstream project, version, and source URL.
2. Read the license that applies to the specific files.
3. Preserve copyright headers and required notices.
4. Include the required license text and attribution.
5. Record local modifications where required or useful.
6. Confirm that redistribution and the intended combination are permitted.

## XNU

Apple publishes open-source XNU under the Apple Public Source License (APSL), with the exact license version and notices determined by the upstream source revision. XNU files must retain their applicable upstream licensing and notices. Do not remove headers or label imported XNU code as MIT.

Before adding XNU source, record the upstream repository URL, commit or release identifier, exact license version, and required notices. This repository's MIT license is not a substitute for the APSL.

## Other components

Device-tree material, Linux-derived driver code, firmware interfaces, tools, and libraries may each have different licenses. Review them individually. Do not commit proprietary firmware, proprietary iOS components, or files whose redistribution rights are unclear.

## File-level clarity

Use file-level SPDX identifiers where appropriate and permitted, for example:

- Original OrchidOS source: `SPDX-License-Identifier: MIT`
- Imported source: retain its upstream header and applicable SPDX identifier.

If licensing is unclear, do not merge the material until it has been reviewed.
