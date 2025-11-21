# Third-Party Notices

This file records third-party software included in this repository and the licenses that apply.

Before any public release or distribution, ensure this file is complete and accurate.

## How to maintain

- Add one line per dependency including package name, version, license, and a short justification for inclusion.
- For compiled/bundled artifacts include the upstream license text or a pointer if required.

## Example entry

| Component | Version | License | Notes |
| --- | --- | --- | --- |
| example-lib | 1.2.3 | MIT | Used for data formatting; include MIT text in `docs/third-party/` if required. |

## Current status

No third-party runtime dependencies recorded yet. Add entries here and include license texts under `docs/third-party/` when required.

## Required steps before release

1. Run dependency inventory (e.g., `npm ls --all`, `pipdeptree`, `cargo tree`) and add every direct dependency.
2. For each dependency, confirm license compatibility with Apache-2.0.
3. For any dependency requiring attribution or NOTICE entries, add them to `NOTICE`.
4. If any dependency requires a contributor agreement or special redistribution permission, do not ship until the obligation is satisfied.
