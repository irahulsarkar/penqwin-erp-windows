# Releasing Penqwin ERP

This repo (`penqwin-erp`) only holds GitHub releases — the real installers, their checksums and the release notes. The source lives in `sark-erp-windows` (Wails 2.17, shipped) and `penqwin-erp-wails3` (Wails 3 preview). Nothing here is committed to this repo's git history unless the person doing the release says so; the release itself (tag + uploaded assets) is a separate action from committing files in this working tree.

## What goes in a GitHub release

- The real Windows installer (`Penqwin-ERP-Windows-<version>.exe`).
- The real macOS and Linux builds, once CI produces them (`Penqwin-ERP-macOS-<version>.dmg`, and the four `Penqwin-ERP-<version>-linux-<arch>-<gtk>.deb`/`.tar.gz` variants).
- `RELEASE_NOTES.md`'s matching section, as the release body.

## What never goes in a GitHub release

- **The demo installer.** It is for local testing and for the website's own "try the demo" flow, never as a GitHub release asset. A release holds only the real, licensable app.
- Anything built with demo ldflags, or a build whose secrets/markers haven't been verified (see `INSTALLABLE_RITUALS.md`'s byte-search checks).

## Steps

1. Bump `VERSION` and `wails.json`'s `productVersion` in the source repo(s), build and verify the real installer(s) per `INSTALLABLE_RITUALS.md`.
2. Update this repo's `RELEASE_NOTES.md`, `CHANGELOG.md`, `README.md`, `SUPPORT.md`, `docs/INSTALL.md` and `release-assets/SHA256SUMS.txt` for the new version.
3. Create the GitHub release (tag `v<version>`) on `irahulsarkar/penqwin-erp-windows` via the REST API (no `gh` CLI installed — see the session's own credential-helper + curl pattern), upload the real installer(s) as assets.
4. If Linux/macOS are built by CI (`penqwin-erp-wails3`'s `desktop.yml`), download the successful build-job artifacts and upload them as additional assets to the same release once CI finishes.
5. Update `penqw.in-website`'s `src/config.ts` (`APP_VERSION`, installer filenames) and `src/platform.ts` (clear any `comingSoon` flag once that platform's asset is actually attached) to match, then commit that repo.
6. Never attach the demo installer to the release (see above).
