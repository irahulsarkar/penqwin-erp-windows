# Installing Penqwin ERP

## Requirements

| | |
|---|---|
| Operating system | Windows 10 or Windows 11, 64-bit |
| Rights | A standard user is enough. The installer does not need administrator rights |
| Display | The Microsoft Edge WebView2 Runtime, which is included with Windows 11 and with up-to-date Windows 10 |
| Network | Needed to activate the licence and, optionally, for backup to Google Drive. Daily work does not depend on it |

## Install

1. Download `Penqwin-ERP-Setup-6.0.0.exe` from the [latest release](../../../releases/latest).
2. Run it and follow the steps. The app is installed for the signed-in Windows user.
3. Open Penqwin ERP. On the first start, activate it with your licence and complete the first-run setup.

## Verify the download

Each release lists the SHA-256 of the installer. To check your copy, open a command prompt in the download folder and run:

```
certutil -hashfile Penqwin-ERP-Setup-6.0.0.exe SHA256
```

The result must match the release notes exactly. If it does not, download the file again.

## Upgrade

Run the new installer over the existing one. An existing Penqwin ERP or SARK ERP installation is recognised and upgraded in place; your data, licence and settings are kept. There is no separate migration step.

## Your data

Records are stored on your own computer, in `%LOCALAPPDATA%\PenqwinERP`. Keep your own backups:

- **Backup and Restore** in Settings makes and restores a backup file.
- **Cloud backup** can copy backups to your own Google Drive. See Settings, Cloud Backup.

Copy a backup to another drive or computer regularly. A backup that exists only on the computer it protects does not protect against that computer failing.

## Licence

A licence is per computer. Moving the software to another computer needs the licence to be moved; write to [hello@penqw.in](mailto:hello@penqw.in) for help. For prices and how to buy, see [penqw.in](https://penqw.in).

## Uninstall

Open Settings, Apps, Installed apps, select Penqwin ERP and choose Uninstall. Your data folder is left in place, so a later reinstall finds it. Delete `%LOCALAPPDATA%\PenqwinERP` only if you no longer need the data.

## For IT administrators

The installer is an Inno Setup program and accepts its standard switches, for example `Penqwin-ERP-Setup-6.0.0.exe /VERYSILENT /SUPPRESSMSGBOXES /NORESTART`.
