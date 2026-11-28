# Releasing Penqwin ERP

This repo (`penqwin-erp`) only holds GitHub releases: the real installers, their checksums and the release notes. The source and the build steps are in the suite repository, `penqwin-suite/windows` (see its `INSTALLABLE_RITUALS.md`). Files here are committed only when the person doing the release says so; the release itself (tag and uploaded files) is a separate action.

## What goes in a GitHub release

- The real Windows installer (`Penqwin-ERP-Windows-<version>.exe`).
- The real macOS and Linux builds, once CI produces them (`Penqwin-ERP-macOS-<version>.dmg`, and the four `Penqwin-ERP-<version>-linux-<arch>-<gtk>.deb`/`.tar.gz` variants).
- `RELEASE_NOTES.md`'s matching section, as the release body.

## What never goes in a GitHub release

- **The demo installer.** It is for local testing and for the website's own "try the demo" flow, never as a GitHub release asset. A release holds only the real, licensable app.
- Anything built with demo ldflags, or a build whose secrets/markers haven't been verified (see `INSTALLABLE_RITUALS.md`'s byte-search checks).

## Steps

Follow `penqwin-suite/windows/INSTALLABLE_RITUALS.md`: version, tests, builds, checks, a draft release, publishing, and then, as a separate decision, the update list (`latest-windows.json` on the `windows-latest` release). Never attach the demo installer.
