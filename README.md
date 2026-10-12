# VS Path Tracing: issues

Bug reports and suggestions for **VS Path Tracing**, real-time path tracing for Vintage Story on NVIDIA RTX graphics
cards. The mod's code is not public yet; this repository is only its issue tracker.

- **The mod:** `vspt`, with its two companions from the Mod DB, [VS Path Tracing: materials](https://mods.vintagestory.at/vsptmaterials) and [VS Path Tracing: runtime](https://mods.vintagestory.at/vsptruntime)
- **Needs:** Windows, an NVIDIA RTX card, Vintage Story 1.22.7

## Reporting a bug

1. **Make a report.** In the game, open *Settings → Path Tracing → Advanced* and press **Package logs for a bug report**,
   or type `.vspt report` in chat (this works even when the picture is black). Explorer opens with a zip selected:
   `vspt-report-<date>.zip`.
2. **[Open a bug report](../../issues/new?template=bug_report.yml)**, say what happened, and drag the zip into it.

The zip holds your game's logs, your VS Path Tracing settings, a short summary of your PC (graphics card, driver,
memory) and a few of the game's graphics settings. Your Windows user name is taken out of it, and the game's login is
never in it. Your in-game player name can appear in the logs.

If the game will not start at all, zip the `Logs` folder from your Vintage Story data folder
(`%APPDATA%\VintagestoryData\Logs` unless you moved it) and attach that instead.

No logs at all? Report it anyway and say so. Anything broken goes in a bug report, not a suggestion.

## Suggestions

[Suggest something](../../issues/new?template=suggestion.yml). Screenshots help, especially a comparison with how
you expected it to look.

## Before you post

- Search the [open issues](../../issues) first, and add to one if it is the same problem.
- One problem per issue.
- No other mod's files and no game files: just the report zip, screenshots and video.
