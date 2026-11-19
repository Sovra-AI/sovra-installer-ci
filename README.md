# sovra-installer-ci

Public GitHub Actions workflows that build Velopack installers for
**SovraHarness** on macOS, Windows, and Linux runners.

Source never lives in this repository. Jobs check out `Sovra-AI/SovraHarness`
with `SOVRA_BUILD_TOKEN` and upload `.pkg` / Setup `.exe` / `.AppImage` to that
repo’s GitHub Release.

The download site now links directly to the official SovraHarness release. Existing
mirror download links remain available here. **Mirror latest release** is scheduled
to check the public SovraHarness releases twice an hour. It publishes a draft after
all three installers are uploaded and resumes interrupted drafts on the next run.
It reads releases with the workflow's own GitHub token.

## Run

Actions → **Package installers** → Run workflow → tag `v0.2.0` (or newer).

Required secret: `SOVRA_BUILD_TOKEN` (PAT/OAuth with `repo` on SovraHarness).
