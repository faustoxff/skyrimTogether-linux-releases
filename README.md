# Skyrim Together Linux Launcher

A Linux launcher for **Skyrim Together Reborn**, built to work around common issues
when running the mod through Proton (executable detection, registry state, and
Steam Compat Data paths).

This repo only contains **releases** (prebuilt AppImages). Source code is kept
in a separate private repository.

## Requirements

- Skyrim Special Edition (Steam, AppID 489830) installed via Proton
- [Skyrim Together Reborn](https://www.nexusmods.com/skyrimspecialedition/mods/69993) installed as a mod
- SKSE64 installed and working

## How to use

1. Go to the [Releases](../../releases) page and download the latest `.AppImage`
2. Give it execute permission:
   ```bash
   chmod +x SkyrimTogetherLauncher-x86_64.AppImage
   ```
3. Run it by double-clicking, or from a terminal:
   ```bash
   ./SkyrimTogetherLauncher-x86_64.AppImage
   ```
4. The launcher will auto-detect your Skyrim SE installation and Proton prefix,
   validate the game executable, and launch Skyrim Together Reborn correctly.

## Troubleshooting

- **"Detected SKSE loader instead of the real game executable"**: this happens
  if your mod manager swapped `SkyrimSELauncher.exe` with the SKSE loader
  (e.g. Amethyst Mod Manager's "Swap launcher with script extender" option).
  This is expected and handled automatically — the launcher targets the real
  `SkyrimSE.exe` directly.
- If detection fails, use the manual path override in the launcher's settings.

## Notes

- Tested on Nobara Linux (KDE Plasma) with Amethyst Mod Manager.
- Not an official Skyrim Together Reborn tool — this is a community workaround
  for launching it on Linux/Proton.
