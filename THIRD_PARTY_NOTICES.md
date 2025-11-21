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

No third-party runtime dependencies recorded yet in this repository.

### Automated scan (repo scan performed)

- Scanned for common manifest files: `package.json`, `package-lock.json`, `yarn.lock`, `requirements.txt`, `Pipfile`, `pyproject.toml`, `setup.py`, `Cargo.toml`.
- Result: No dependency manifest files were found in the repository at the time of the scan.

If your project uses a package manager, add the relevant manifest files (for example `package.json`, `requirements.txt`, or `pyproject.toml`) to the repository and I can re-run the scan and populate this file with detected dependencies and their license fields.

## How to produce a dependency inventory locally

Run one of the following in your project workspace and paste the output here, or commit the manifest files to the repo and I will scan them automatically:

- Node.js (npm):

```bash
npm ls --all --json > dependency-tree-npm.json
```

- Python (pip):

```bash
pipdeptree --json-tree > dependency-tree-pip.json
```

- Python (requirements):

```bash
pip freeze > requirements.txt
```

- Rust (cargo):

```bash
cargo tree --prefix none --format json > dependency-tree-cargo.json
```

After generating inventories, update this file with the dependency list and include license information for each entry. If you prefer, commit the generated manifests and I will update `THIRD_PARTY_NOTICES.md` automatically.

## Required steps before release

1. Run dependency inventory (e.g., `npm ls --all`, `pipdeptree`, `cargo tree`) and add every direct dependency.
2. For each dependency, confirm license compatibility with Apache-2.0.
3. For any dependency requiring attribution or NOTICE entries, add them to `NOTICE`.
4. If any dependency requires a contributor agreement or special redistribution permission, do not ship until the obligation is satisfied.

