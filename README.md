# sovra-installer-ci

Public GitHub Actions workflows that build Velopack installers for
**SovraHarness** (private) on macOS, Windows, and Linux runners.

Source never lives in this repository. Jobs check out `Sovra-AI/SovraHarness`
with `SOVRA_BUILD_TOKEN` and upload `.pkg` / Setup `.exe` / `.AppImage` to that
repo’s GitHub Release.

## Run

Actions → **Package installers** → Run workflow → tag `v0.2.0` (or newer).

Required secret: `SOVRA_BUILD_TOKEN` (PAT/OAuth with `repo` on SovraHarness).
