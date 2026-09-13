[All maps](../../README.md) · [Install guide](../../docs/INSTALL.md) · [Player ZIP](https://github.com/Lightkeeper01/ra3-custom-maps/releases/download/collection-2026-09-13/Black-Tide-v1.0.zip) · [Source ZIP](https://github.com/Lightkeeper01/ra3-custom-maps/releases/download/collection-2026-09-13/Black-Tide-v1.0-Source.zip)

# Black Tide - Salvage Wars [6P]

A compact six-player island arena with an opening raid squad, rotating relay contracts, random salvage, mixed-faction reinforcements and coastal artillery.

## Requirements

Command & Conquer: Red Alert 3, vanilla PC version 1.12. A separate copy of the game is required. These packages do not contain the game. Maps are not intended for Uprising, Red Alert 2 or other C&C titles. No additional mod is required.

## Install

1. Extract the entire ZIP.
2. Either run `Install-Map.cmd`, or use the manual steps below.
3. Restart RA3 and start a new skirmish. Select **Black Tide - Salvage Wars [6P]**.

Manual installation: press Win+R, enter `%APPDATA%\Red Alert 3\Maps` and press Enter. Create the Maps folder if necessary. Copy the complete `Black_Tide_6P` directory into it. Inside that directory must be one same-name `.map`, two `.tga` previews and `map.str`; avoid a second nested directory. Install under the Windows account that runs the game. The installer backs up an existing same-name map; other map folders are preserved.

If the installer does not run or appears stuck, use manual copying. You do not need to change system-wide script execution policy. To uninstall, remove only the `Black_Tide_6P` folder from Maps.

## Play

Start with 2 Riptides and 1 Engineer. The first salvage arrives in 60-75 seconds. Capture the flashing Observation Post with an Engineer and hold it for 45 seconds to earn $1500 plus reinforcements. Targets rotate between AIRFIELD, SHIPYARD and ARSENAL. A winner has a 120-second contract cooldown. At 6 minutes, the reward becomes $2200 with stronger squads. The first completed contract on each island also grants a coastal gun. All custom notifications use English ASCII text.

All maps retain the standard skirmish elimination win condition. Choose teams, factions and AI difficulty in the lobby. Six starting positions do not add six new playable national factions. Country labels in the original strait theme are fictional scenario roles. Use identical map versions on every machine for multiplayer.

## Validation status

Experimental release. Geometry and 19 event-model scenarios passed; a source archive rebuild was byte-identical. In-game rendering, balance and multiplayer behavior still need playtesting.

Automated script simulation is not the actual RA3 engine. Please report the map version, game version, player slot, faction, AI/team setup, exact steps and approximate match time with any bug report.

## Credits and licensing

Made available by Lightkeeper01. Uses native RA3 objects and format references from EA's CnC_Modding_Support and OpenSAGE. Preserve the accompanying license notices. Source bundles are supplied separately in the same GitHub repository. This is an unofficial community map project, not endorsed by Electronic Arts.

## Detailed objectives

**Raid early.** About seven seconds after the match begins, active players with a construction yard or MCV receive **two Riptides and one Allied Engineer**. Put the Engineer into a Riptide and head toward a central island. Your chosen vanilla faction does not restrict these bonus units.

**Watch for salvage.** The first cache appears after roughly 60-75 seconds, with a 10-second warning. Move any unit close to the flashing cache to claim it. A cache lasts 70 seconds; an unclaimed or destroyed cache is removed. After each event ends, a new 45-75 second random wait begins, followed by the next warning.

Salvage can award **$1000, $1800, two Riptides, two Tengus, a Twinblade, or an Engineer plus a Riptide**. Cash is immediate; bonus units arrive at your original home island's landing area facing the center. Keep that area clear and move reinforcements out promptly.

**Capture the active relay.** The first contract opens around 85 seconds. Use an Engineer to capture the flashing **Observation Post**, then keep it under your ownership for **45 uninterrupted seconds**. Losing control resets the attempt. Capturing the nearby support building is useful, but does not complete the relay contract.

| Objective island | Reward before 6 minutes | Reward after 6 minutes | Nearby capturable support |
| --- | --- | --- | --- |
| AIRFIELD, north | 1 Twinblade + 1 Tengu | 1 Twinblade + 2 Tengus | Veteran Academy |
| SHIPYARD, southwest | 1 Stingray + 2 Riptides | 2 Stingrays + 1 Riptide | Dry Dock |
| ARSENAL, southeast | 2 Tengus + 1 Riptide | 3 Tengus + 1 Riptide | Hospital |

A successful contract also pays **$1500**, increasing to **$2200 after six minutes**. The winner has a personal **120-second contract cooldown**. Contracts rotate between the three islands; each has a 150-second window, followed by a 20-second transition after completion or expiry. Destroyed relay buildings are skipped in later rotations.

The first successful contract on each island additionally creates a player-owned **coastal gun**. It bombards a fixed point in the central sea. There are at most three guns; destruction does not respawn them, and later relay captures do not automatically transfer existing guns. These native guns have limited firing arcs and can cause friendly fire; they are not automatic 360-degree naval turrets.

All maps retain **standard skirmish elimination**. Contracts help fund your attacks; they are not an alternative victory condition. Select factions, teams and AI difficulty in the lobby. Human opponents can intentionally contest objectives; the standard AI has no custom contract-planning logic.


![Terrain-derived tactical overview](assets/overview.png)

*Planning illustration, not an in-game screenshot.*

## Verification and credits

[Native file checksums](validation/Map-Checksums.json) · [Geometry checks](validation/Validation.json) · [Source rebuild](validation/source-rebuild.json) · [Credits and licenses](../../docs/CREDITS.md)
