[All maps](../../README.md) · [Install guide](../../docs/INSTALL.md) · [Player ZIP](https://github.com/Lightkeeper01/ra3-custom-maps/releases/download/three-kingdoms-v0.2/Three-Kingdoms-Mandate-219-v0.2.zip) · [Source ZIP](https://github.com/Lightkeeper01/ra3-custom-maps/releases/download/three-kingdoms-v0.2/Three-Kingdoms-Mandate-219-v0.2-Source.zip)

# Three Kingdoms: Mandate 219

**Vanilla Command & Conquer: Red Alert 3, PC patch 1.12. Version 0.2 experimental.**

A six-player, 2v2v2 strategic map inspired by the situation in 219 CE, after Liu Bei acquired Hanzhong and before the loss of his western Jing province holdings. Wei, Shu and Wu are retrospective, convenient kingdom labels: this is before all three had formally become independent imperial states.

This is a new native map, not a replacement for Black Tide or the Strait maps. It retains Red Alert 3 units and technology. It does not add ancient soldier models or new playable factions. Terrain, starting seats and supply objectives provide the Three Kingdoms roles.

![Three Kingdoms strategic atlas](assets/atlas.png)

*Derived from the delivered terrain. A planning illustration, not an in-game screenshot.*

## Version 0.2 terrain update

- Excavated submerged terrain after all construction-apron flattening. The Yangtze centerline now has 105 height units of water above it; its deep-water corridor remains connected to the eastern sea. Shorelines and dry construction aprons retain their heights.
- Raised and broadened the Qinling, Jianmen and Daba ridges. Two deliberate mountain passages remain: the main Shu Road and the narrower Yinping flank. Air and amphibious units still use their normal RA3 movement rules.
- Moved one northern expansion ore site away from the Qinling crest so its construction apron no longer opens an unintended gap. All 27 ore nodes and six equal starting economies remain.
- Restart RA3 and begin a **new match** after updating. An existing saved/active match can retain the previous terrain. All multiplayer participants need the same version.

## Required lobby setup

Choose **Three Kingdoms - Mandate 219 [6P]**. Set starting positions manually:

| Kingdom | Starting seats | Role | Optional faction theme |
| --- | --- | --- | --- |
| Wei | 1 + 2, same team | Changan and Xuchang; northern armor and multiple fronts | Soviets |
| Shu | 3 + 4, same team | Chengdu and Jiangling/Jingzhou; divided fronts and difficult roads | Allies |
| Wu | 5 + 6, same team | Jianye and Kuaiji; Jiangdong, river movement and coast | Empire |

Use a different team number for each kingdom. Fill all six seats with people or AI. The **seat pairs**, not the selected faction, define supply-link beneficiaries; the script does not inspect lobby alliances. Random starting positions or free-for-all settings do not fit this design. AI can play ordinary skirmish but is not scripted to understand the custom objectives.

All factions remain selectable. Recommended initial settings: normal speed, standard starting credits and normal elimination victory. AI difficulty and team balance need playtesting.

## Install

Extract the complete player ZIP. Double-click `Install-Map.cmd`, or manually copy the `Three_Kingdoms_219_6P` directory into:

```text
%APPDATA%\Red Alert 3\Maps\Three_Kingdoms_219_6P\
```

That directory must directly contain the `.map`, two `.tga` previews and `map.str`. Restart the game and start a new skirmish. The installer verifies file hashes and backs up an existing copy of this map before updating it.

## Geography that changes the match

- **Wei:** the northern plain provides the broadest armor corridors. Changan can pressure Hanzhong; Xuchang can pressure Xiangfan or the lower river. Committing to one front exposes the other.
- **Shu:** Chengdu is the protected economic rear. Hanzhong lies beyond Jianmen; a narrow alternative route provides a flank. Jiangling is a separate forward start in western Jing province. The Han River and the Daba/Three Gorges approaches make reinforcement a real choice between detours, amphibious transport and air movement.
- **Wu:** both seats share the lower Yangtze/eastern coast. The deep-water Yangtze corridor is designed to connect the compressed upper gorge to the sea; v0.2 engine navigation still needs playtesting. Wu can move along the river, land behind Jingzhou, or raid Wei's eastern flank. Northern, western and southern map edges continue as land: there is no fictional western ocean around Sichuan.

The map is **760 x 760 cells**. Geography is compressed for travel time and unit footprints. The northern frontier, southern hinterland and coastline are cropped or simplified. Colored strategic regions are gameplay zones, not surveyed historical borders. In particular, this is not a claim that Wu held the largest historical land area. Wu has the largest combined river/coastal operational space in the design.

27 ore nodes: two equal home nodes per seat and 15 expansions. Six oil derricks and six capturable structures provide additional incentives. The same starting economy prevents a literal historical population imbalance from deciding the match before play begins.

## Supply objectives

The three front depots are **Hanzhong, Xiangfan and Jiangdong**. Their capturable relay is an Observation Post. Bring an Engineer; it does not fall merely because an army stands nearby.

1. The first contract opens at 85 seconds at a randomly chosen depot. Later contracts rotate across the three fronts.
2. Capture the flashing relay and keep the same owner for **45 seconds**. A capture by another player resets that owner's hold. The contract closes after 150 seconds if nobody succeeds.
3. The winner receives **$1,500 and a mixed strike squad** at reserved home muster points. At six minutes, contract cash becomes **$2,200** and squads strengthen. A winner has a 120-second personal contract cooldown.
4. The first contract victory at each depot also supplies a fixed river gun: Hanzhong supports the Baidi approach, Xiangfan supports the Jingzhou riverbank, and Jiangdong supports the lower-river channel. Each gun belongs to its first winner and has one authored bombardment point. It is not a player-targetable global artillery ability. Destroyed guns do not respawn; later relay captures do not transfer them.

Regional strike squads use vanilla units: Hanzhong provides a Twinblade and Tengus, Xiangfan provides Riptides and Stingrays, and Jiangdong provides Tengus and a Riptide. These are Red Alert adaptations, not historical unit claims.

### Linked supply network

If a kingdom's two seats jointly control **any two depots continuously for 90 seconds**, each commander receives **$250**. Both must still have a construction yard or MCV. Losing the two-depot link resets its progress. The two depots may be held by one teammate or split between teammates. Capture by the other teammate preserves the kingdom's link while changing the individual contract owner.

This is a territorial supply bonus; no physical convoy or simulated river current is implemented. It creates a reason for the Chengdu and Jingzhou commanders to support each other and for enemies to strike the less-defended depot.

### Random salvage

The first cache arrives in 60-75 seconds. Later deliveries have a randomized wait and a 10-second warning. One of three depot-side pickup pads is selected. A flashing crate and radar event mark the site; move a unit into the pickup zone within 70 seconds. There is at most one live cache.

Possible rewards: $1,000, $1,800, two Riptides, two Tengus, a Twinblade, or an Engineer plus a Riptide. Unit rewards appear at home muster points. Every occupied seat also receives two Riptides and one Engineer near the start so river raiding is available early.

## What has been checked

Native map serialization, six start areas, all ore/refinery grid positions, construction aprons, staging clearance, terrain texture references, deep-water Yangtze connectivity (bed at height 95 beneath the height-200 water surface), dense centerline depth/clearance checks, continuous mountain passes and mountain-crest breach checks, and event state models. `Validation.json`, `Geography-Validation.json` and `Event-Validation.json` contain the results. Notifications use ASCII English without a BOM and five-second military captions, not persistent dialog panels.

**The user confirmed v0.1 loads and is playable, but reported blocked naval movement in its shallow Yangtze. Version 0.2 addresses the terrain defect; its revised naval and mountain movement has not yet been verified in game.** Model tests do not prove engine pathfinding, UI rendering, AI objective handling, multiplayer synchronization, artillery behavior or balance. Aircraft can bypass terrain, as in normal Red Alert 3. There are no custom general powers, ancient armies, real-time diplomacy or scripted betrayal scenes in this version.

## Build from source

Python 3 with NumPy, SciPy and Pillow. From the extracted source root:

```sh
python3 work/three_kingdoms/configure.py
python3 work/three_kingdoms/build.py
python3 work/three_kingdoms/validate.py
python3 work/three_kingdoms/test_events.py
python3 work/three_kingdoms/preview.py
python3 work/three_kingdoms/package.py
```

## History and credits

- [Hanzhong official historical chronology](https://jhj.hanzhong.gov.cn/hzjhjwz/lswh/202606/e21a0ec512234aeda97bebb81b3aa63c.shtml): Liu Bei's acquisition of Hanzhong in 219.
- [Ezhou municipal historical article](https://www.ezhou.gov.cn/zjez/ezrw/ezss/202209/t20220908_496069.html): Sun Quan's takeover of Liu Bei's Jingzhou base later in 219.
- [ShuDao tentative-list submission, UNESCO](https://whc.unesco.org/en/tentativelists/5994): mountain routes connecting central China and northern Sichuan. Tentative-list status is not World Heritage inscription.
- [Three Kingdoms overview](https://en.wikipedia.org/wiki/Three_Kingdoms): broad regional and chronological context, used as a secondary cross-check.

Map design and authoring: Lightkeeper01's community map collection. Native scripting/serialization builds on the preceding Black Tide toolkit. Original game assets and relevant tools retain their respective rights and accompanying EA/OpenSAGE license notices. This package contains no copy of the game and is not endorsed by EA.

## Files and development evidence

[Update notes](../../docs/releases/three-kingdoms-v0.2.md) · [Native checksums](validation/Map-Checksums.json) · [Terrain validation](validation/Validation.json) · [River and mountain checks](validation/Geography-Validation.json) · [Event models](validation/Event-Validation.json) · [Source rebuild](validation/source-rebuild.json) · [Archive checksums](validation/SHA256SUMS.txt)

[Chinese historical design notes](DESIGN.zh-CN.md) · [Credits and licenses](../../docs/CREDITS.md)
