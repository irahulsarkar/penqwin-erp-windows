# Installing Penqwin ERP

## Requirements

| | Windows | Linux |
|---|---|---|
| System | Windows 10 or Windows 11, 64-bit | Ubuntu 24.04 or newer, Debian 13, Fedora 40 or newer, or another distribution with GTK 4 and WebKitGTK 6; 64-bit Intel/AMD |
| Rights | A standard user is enough. The installer does not need administrator rights | Installing the package needs administrator rights (`sudo`); running it does not |
| Display | The Microsoft Edge WebView2 Runtime, which is included with Windows 11 and with up-to-date Windows 10 | GTK 4 and WebKitGTK 6, which the package installs for you |
| Printing | Any Windows printer; receipt printers and cash drawers through the Windows spooler | Any CUPS printer; receipt printers and cash drawers through CUPS |
| Network | Needed to activate the licence and, optionally, for backup to Google Drive. Daily work does not depend on it | The same |

macOS is not available in this release.

## Install on Windows

1. Download `Penqwin-ERP-Windows-6.0.3.exe` from the [latest release](../../../releases/latest).
2. Run it and follow the steps. The app is installed for the signed-in Windows user.
3. Open Penqwin ERP. On the first start, activate it with your licence and complete the first-run setup.

## Install on Linux

1. Download `Penqwin-ERP-Linux-6.0.3.deb` from the [latest release](../../../releases/latest).
2. Install it: `sudo apt install ./Penqwin-ERP-Linux-6.0.3.deb`. This also installs GTK 4 and WebKitGTK if they are missing.
3. Open Penqwin ERP from the applications menu. On the first start, activate it with your licence and complete the first-run setup.

Without `apt`: unpack `Penqwin-ERP-Linux-6.0.3.tar.gz` anywhere and run `./penqwin-erp/penqwin-erp`.

## Verify the download

Each release lists the SHA-256 of every file. To check your copy:

```
certutil -hashfile Penqwin-ERP-Windows-6.0.3.exe SHA256     (Windows, in a command prompt)
sha256sum Penqwin-ERP-Linux-6.0.3.deb                       (Linux)
```

The result must match the release notes exactly. If it does not, download the file again.

## Upgrade

Run the new installer over the existing one. On Windows, an existing Penqwin ERP or SARK ERP installation is recognised and upgraded in place; your data, licence and settings are kept. On Linux, install the new package the same way as the first. There is no separate migration step.

## Your data

Records are stored on your own computer:

- Windows: `%LOCALAPPDATA%\PenqwinERP`
- Linux: `~/.local/share/PenqwinERP`

Keep your own backups:

- **Backup and Restore** in Settings makes and restores a backup file.
- **Cloud backup** can copy backups to your own Google Drive. See Settings, Cloud Backup.

Copy a backup to another drive or computer regularly. A backup that exists only on the computer it protects does not protect against that computer failing.

## The program's own window

On Windows and Linux the program draws its own title bar. It has a search box (Ctrl+K), back and forward buttons, an online / offline indicator, and an "Aa" menu for text size, higher contrast and reduce motion. Settings, Desktop chooses whether closing the window keeps the program in the tray, and whether it starts when you sign in.

## Licence

A licence is per computer. Moving the software to another computer needs the licence to be moved; write to [hello@penqw.in](mailto:hello@penqw.in) for help. For prices and how to buy, see [penqw.in](https://penqw.in).

## Uninstall

- Windows: open Settings, Apps, Installed apps, select Penqwin ERP and choose Uninstall.
- Linux: `sudo apt remove penqwin-erp`.

Your data folder is left in place, so a later reinstall finds it. Delete it only if you no longer need the data.

## For IT administrators

The Windows installer is an Inno Setup program and accepts its standard switches, for example `Penqwin-ERP-Windows-6.0.3.exe /VERYSILENT /SUPPRESSMSGBOXES /NORESTART`.
