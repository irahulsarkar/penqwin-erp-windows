# Installing Penqwin ERP

## Requirements

| | Windows | Linux |
|---|---|---|
| System | Windows 10 or Windows 11, 64-bit | Ubuntu 24.04 or newer, Debian 13, Fedora 40 or newer, or another distribution with GTK 3 and WebKitGTK 4.1 and glibc 2.39 or newer; 64-bit Intel/AMD |
| Rights | A standard user is enough. The installer does not need administrator rights | Installing the package needs administrator rights (`sudo`); running it does not |
| Display | The Microsoft Edge WebView2 Runtime, which is included with Windows 11 and with up-to-date Windows 10 | GTK 3 and WebKitGTK 4.1, which the package installs for you |
| Printing | Any Windows printer; receipt printers and cash drawers through the Windows spooler | Any CUPS printer; receipt printers and cash drawers through CUPS |
| Network | Needed to activate the licence and, optionally, for backup to Google Drive. Daily work does not depend on it | The same |

Linux and macOS are not available in this release.

## Install on Windows

1. Download `Penqwin-ERP-Windows-6.3.3.exe` from the [latest release](../../../releases/latest).
2. Run it and follow the steps. The app is installed for the signed-in Windows user.
3. Open Penqwin ERP. On the first start, activate it with your licence and complete the first-run setup.

## Linux

The Linux package is not part of release 6.3.3. It will come in a later release.

## Verify the download

Each release lists the SHA-256 of every file. To check your copy:

```
certutil -hashfile Penqwin-ERP-Windows-6.3.3.exe SHA256     (Windows, in a command prompt)
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

## The free trial and activation

A copy with no licence runs on a free trial: 24 hours from its first start, with 5 sales and 5 purchase entries, and the AI features locked. Everything you enter is kept when you activate, and you carry on exactly where you left off. Installing again does not give another trial. When it ends the program shows "Your free trial has ended" with how to reach us for an activation key; press Activate, download the activation request, send it to us, and import the licence file we send back.

## Licence

A licence is per computer. Moving the software to another computer needs the licence to be moved; write to [hello@penqw.in](mailto:hello@penqw.in) or call +91 84312 93339 for help. For prices and how to buy, see [penqw.in](https://penqw.in).

## Uninstall

- Windows: open Settings, Apps, Installed apps, select Penqwin ERP and choose Uninstall.
- Linux: `sudo apt remove penqwin-erp`.

Your data folder is left in place, so a later reinstall finds it. Delete it only if you no longer need the data.

## For IT administrators

The Windows installer is an Inno Setup program and accepts its standard switches, for example `Penqwin-ERP-Windows-6.3.3.exe /VERYSILENT /SUPPRESSMSGBOXES /NORESTART`.
