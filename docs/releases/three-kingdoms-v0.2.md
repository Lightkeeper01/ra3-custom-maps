# Three Kingdoms: Mandate 219 v0.2

**Experimental terrain update — vanilla Red Alert 3, PC patch 1.12.** This is the first public release of Three Kingdoms in this repository; v0.1 was tested privately.

[Map guide and strategic atlas](../../maps/three-kingdoms/README.md) · [Release downloads](https://github.com/Lightkeeper01/ra3-custom-maps/releases/tag/three-kingdoms-v0.2)

## Why this update exists

A player confirmed v0.1 loaded and was playable, but ships could not navigate its shallow Yangtze. Visible water connectivity alone missed the depth problem. The same feedback requested a more defensible, mountainous Wei–Shu frontier with a few usable passages.

## Terrain changes

- Deepened submerged terrain after construction-apron flattening. The sampled Yangtze centerline now has a bed height of **95** below the water surface at **200**, giving **105 game height units of depth**.
- Added dense deep-water corridor checks from the upper river through its bends to the eastern sea. The checked route has at least approximately **82 game units of radial clearance** inside the region with at least 70 units of depth. These are map-data measurements, not an engine-certified ship draft or collision guarantee.
- Raised and widened the Qinling, Jianmen and Daba ridges. Retained the main Shu Road and a narrower Yinping flank for deliberate mountain crossings.
- Relocated one northern expansion ore site away from the Qinling crest, preventing its construction apron from making an unintended gap in the mountain barrier.
- Retained **27 ore nodes**, six player seats, dry shore heights, home economies and the existing supply-event rules. Refineries and placement aprons were revalidated.

## How to play

Use fixed teams and starts: **1+2 Wei vs 3+4 Shu vs 5+6 Wu**. The map includes Sichuan/Chengdu, Hanzhong, Jingzhou, the Yangtze and Jiangdong, compressed for RA3 gameplay. Vanilla factions remain selectable; historical kingdom labels do not add new factions or ancient unit models.

Capture flashing relays with an Engineer, hold them for 45 seconds, contest random salvage, and link two depots for team income. Custom map notifications use English ASCII.

## Installation and validation

Download **`Three-Kingdoms-Mandate-219-v0.2.zip`** to play. Extract it and run `Install-Map.cmd`, or follow the [manual guide](../INSTALL.md). **Restart RA3 and begin a new match** after updating. Old saves can retain old terrain, and all multiplayer participants need matching versions.

Native serialization, deep-water geometry, mountain passages and selected crest barriers, ore/refinery aprons, texture references and **20 event-model scenarios** passed. The source bundle rebuilt all four native files byte for byte, and the local Windows installation matched their SHA-256 hashes.

**The revised v0.2 naval and mountain movement has not yet been verified inside the game.** AI behavior, multiplayer synchronization and balance still need playtesting. Development checks are documented in the [validation directory](../../maps/three-kingdoms/validation/).

## Repository organization

The homepage now indexes four maps. Each map has its own guide and evidence directory; shared installation/development instructions and license notices have dedicated locations. Player and source archives are served through GitHub Releases. The original collection release and its assets are retained.
