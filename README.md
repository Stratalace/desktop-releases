# Stratalace desktop releases

Windows installers for the Stratalace desktop apps, plus the update feeds the installed apps check on launch.

| App | Latest installer | Update feed |
| --- | --- | --- |
| Anchor CRM | [Releases tagged `anchor-crm-v*`](https://github.com/Stratalace/desktop-releases/releases?q=anchor-crm-v) | `anchor-crm-feed` |
| ChickenScratch | [Releases tagged `chickenscratch-v*`](https://github.com/Stratalace/desktop-releases/releases?q=chickenscratch-v) | `chickenscratch-feed` |
| FluxCascade | [Releases tagged `fluxcascade-v*`](https://github.com/Stratalace/desktop-releases/releases?q=fluxcascade-v) | `fluxcascade-feed` |

## Installing

Download the newest `*_x64-setup.exe` for the app and run it. No admin rights are needed. The installers aren't code-signed yet, so Windows SmartScreen warns first: click **More info**, then **Run anyway**. Installed apps update themselves; when a new version is out, they offer to install it on next launch.

## Publishing

Releases are published from each app's `desktop/` folder with `npm run release`. Don't upload files here by hand. Each `*-feed` release holds a `latest.json` that installed apps read, and it has to match the signature of its installer.
