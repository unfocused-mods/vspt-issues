# VS Path Tracing: issues

Bug reports and suggestions for **VS Path Tracing**, real-time path tracing for Vintage Story on NVIDIA RTX graphics
cards. The mod's code is not public yet; this repository is only its issue tracker.

- **The mod:** `vspt`, with its companions from the Mod DB, [VS Path Tracing: materials](https://mods.vintagestory.at/vsptmaterials) and [VS Path Tracing: runtime](https://mods.vintagestory.at/vsptruntime) ([runtime for Linux](https://mods.vintagestory.at/vsptruntimelinux) on Linux). Setup downloads them for you
- **Needs:** Windows or Linux, an NVIDIA RTX card with NVIDIA's own driver, Vintage Story 1.22.7

## On Linux: which installs of the game work

Setup patches the game's own files, so it needs a game folder you can write. On Linux that is only the game's own
download:

| How you installed the game | Works with VS Path Tracing |
| --- | --- |
| The Linux `.tar.gz` from your account on vintagestory.at, with its `install.sh` | Yes |
| The Flatpak | No: its game folder is read-only, and nothing can change that |
| The AUR's `vintagestory` (in `/opt/vintagestory`), or another distribution's package | No: the folder belongs to root |
| Nix | No: the Nix store is read-only |

To switch to the game's own download:

1. Get the Linux `.tar.gz` from your account on vintagestory.at, unpack it and run `./install.sh` from its folder.
2. It needs the .NET 10 runtime from your distribution's packages. A package from the AUR has already installed it; the
   Flatpak brought its own, so coming from the Flatpak you need to install it.
3. Your worlds and mods: a package normally keeps them in `~/.config/VintagestoryData`, where the download looks too. The
   Flatpak keeps them in `~/.var/app/at.vintagestory.VintageStory/config/VintagestoryData`: copy that folder to
   `~/.config/VintagestoryData` before you first start the new install.
4. Start the game from the new install, open a world, and press **Set up and restart**.

## Reporting a bug

1. **Make a report.** In the game, open *Settings → Path Tracing → Advanced* and press **Package logs for a bug report**,
   or type `.vspt report` in chat (this works even when the picture is black). Explorer opens with a zip selected:
   `vspt-report-<date>.zip`.
2. **[Open a bug report](../../issues/new?template=bug_report.yml)**, say what happened, and drag the zip into it.

The zip holds your game's logs, your VS Path Tracing settings, a short summary of your PC (graphics card, driver,
memory) and a few of the game's graphics settings. Your Windows user name is taken out of it, and the game's login is
never in it. Your in-game player name can appear in the logs.

If the game will not start at all, zip the `Logs` folder from your Vintage Story data folder
(`%APPDATA%\VintagestoryData\Logs` on Windows, `~/.config/VintagestoryData/Logs` on Linux, unless you moved it) and
attach that instead.

No logs at all? Report it anyway and say so. Anything broken goes in a bug report, not a suggestion.

## Suggestions

[Suggest something](../../issues/new?template=suggestion.yml). Screenshots help, especially a comparison with how
you expected it to look.

## Before you post

- Search the [open issues](../../issues) first, and add to one if it is the same problem.
- One problem per issue.
- No other mod's files and no game files: just the report zip, screenshots and video.
