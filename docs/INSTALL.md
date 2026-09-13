# Install, update and troubleshoot

[Map catalog](../README.md) · [Release downloads](https://github.com/Lightkeeper01/ra3-custom-maps/releases)

## Requirements

Use vanilla **Command & Conquer: Red Alert 3 for Windows, patch 1.12**. You need your own copy of the game. These packages are not for Uprising, Red Alert 2 or other C&C games.

Choose a named **Player ZIP** from the catalog. Do not install a `-Source.zip` bundle or GitHub's automatic source-code archive.

## Automatic installation

1. Extract the entire player archive into a normal folder.
2. Double-click `Install-Map.cmd` under the Windows user account that runs RA3.
3. Restart the game and create a **new skirmish**.

The installer checks hashes and backs up an existing copy of the same map into `%APPDATA%\Red Alert 3\CodexMapBackups`. Other map folders are preserved. If the installer is blocked or hangs, use manual copying; no system-wide PowerShell policy change is required.

## Manual installation

Press **Win+R**, enter `%APPDATA%\Red Alert 3\Maps`, then press Enter. Create `Maps` if necessary. Copy the complete map folder from the player ZIP into it.

| Map | Folder | Exact name in RA3 |
| --- | --- | --- |
| Three Kingdoms | `Three_Kingdoms_219_6P` | `Three Kingdoms - Mandate 219 [6P]` |
| Black Tide | `Black_Tide_6P` | `Black Tide - Salvage Wars [6P]` |
| Strait Storm | `Strait_Storm_6P` | `Strait Storm - Wild Supplies [6P]` |
| Strait Reunification | `Strait_Reunification_6P` | `Strait Reunification [6P]` |

For example, the Three Kingdoms directory must contain these files directly:

```text
%APPDATA%\Red Alert 3\Maps\Three_Kingdoms_219_6P\
    Three_Kingdoms_219_6P.map
    Three_Kingdoms_219_6P_art.tga
    Three_Kingdoms_219_6P_pic.tga
    map.str
```

Do not nest an extra map directory inside it. All four maps can coexist.

## Updating an existing map

Back up the old map outside the `Maps` directory, then replace all four native files together. Avoid mixing versions. Restart RA3 and start a new match; an active match or saved game may still contain the previous terrain. Every multiplayer participant needs the same version.

For Three Kingdoms, set fixed starting seats **1+2 vs 3+4 vs 5+6**. These pairs determine Wei, Shu and Wu supply bonuses, regardless of the vanilla faction selected.

To uninstall, remove only that map's directory from `Maps`.

## Troubleshooting

| Symptom | Check |
| --- | --- |
| Map is missing from the list | Use the correct Windows user's `%APPDATA%`, remove extra folder nesting, verify all four files, then restart RA3. |
| Three Kingdoms river still seems unchanged | Confirm v0.2 files are installed and create a new match; do not load the v0.1 save. |
| A ship or ground unit still cannot pass | Record the map version, exact unit, route and starting seat. v0.2 deep-water and mountain checks are geometric; engine movement still needs testing. |
| Refinery placement stays red | Record faction and ore location, and rotate the placement preview. Report reproducible failures with a screenshot. |
| Captions are garbled | Three Kingdoms and Black Tide use English ASCII. Strait Storm retains legacy Chinese event text. |
| Black terrain, crash or mismatched multiplayer map | Verify the complete package checksums and matching game/map versions, then report reproduction details. |

[Open an issue](https://github.com/Lightkeeper01/ra3-custom-maps/issues) with the map and game versions, any mods, player seat, faction, team settings and approximate in-game time.
