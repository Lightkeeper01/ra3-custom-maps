# Sources and validation

[Map catalog](../README.md) · [Install guide](INSTALL.md)

## Source bundles

Each map guide links to a versioned **`-Source.zip`** release asset. Extract it into an empty directory and follow its bundled README. The packages include generators and the asset/file-format references needed by their build; they retain original project-relative paths and some Chinese developer notes.

The browsable repository contains guides, previews, license notices and validation evidence. Its automatic GitHub source-code archive is not a replacement for the named map source bundles.

| Map | Source and evidence |
| --- | --- |
| Three Kingdoms v0.2 | [Source ZIP](https://github.com/Lightkeeper01/ra3-custom-maps/releases/download/three-kingdoms-v0.2/Three-Kingdoms-Mandate-219-v0.2-Source.zip) · [Evidence](../maps/three-kingdoms/validation/) |
| Black Tide v1.0 | [Source ZIP](https://github.com/Lightkeeper01/ra3-custom-maps/releases/download/collection-2026-09-13/Black-Tide-v1.0-Source.zip) · [Evidence](../maps/black-tide/validation/) |
| Strait Storm v1.2 | [Source ZIP](https://github.com/Lightkeeper01/ra3-custom-maps/releases/download/collection-2026-09-13/Strait-Storm-v1.2-Source.zip) · [Evidence](../maps/strait-storm/validation/) |
| Strait Reunification v0.9.2 | [Source ZIP](https://github.com/Lightkeeper01/ra3-custom-maps/releases/download/collection-2026-09-13/Strait-Reunification-v0.9.2-Source.zip) · [Evidence](../maps/strait-reunification/validation/) |

## Verify a download

Each release includes `SHA256SUMS.txt`; each map's `validation/` directory contains checksums for its player and source bundles. Compare the expected checksum with:

```powershell
Get-FileHash -Algorithm SHA256 .\Three-Kingdoms-Mandate-219-v0.2.zip
```

On macOS or Linux, use `shasum -a 256 <archive>` or `sha256sum <archive>`. Per-native-file hashes are in each player's `Map-Checksums.json`.

## What the evidence means

- All four published source bundles have clean-directory rebuild evidence for the native `.map`. Three Kingdoms v0.2 additionally reproduces all four native files, including both preview TGAs and `map.str`, byte for byte.
- Three Kingdoms v0.2 tests densely sampled Yangtze depth/clearance, river-to-sea connectivity, continuous mountain passages, selected ridge crests, 27 ore/refinery placements, terrain material references, file serialization and 20 event behavior-model scenarios.
- Black Tide includes 19 event behavior-model scenarios. Other map evidence reflects its own generation and validation workflow.
- Model tests and raster clearance checks **do not execute RA3's engine**. They do not certify large-unit movement, AI objective handling, match completion, multiplayer synchronization, UI behavior or balance.
- Three Kingdoms v0.1 was reported playable but had a shallow-river naval blockage. The v0.2 correction has passed development checks and local installation checks; its revised movement remains unverified in game.

## Publishing layout

Keep each map's current guide, available images and evidence under `maps/<map-id>/`. Keep shared instructions in `docs/`, version notes in `docs/releases/`, and original license notices in `licenses/`. Add the new version to `maps/catalog.json` and `CHANGELOG.md`.

Upload player/source ZIPs and checksums to a separate versioned GitHub Release. Preserve prior release assets. Before publishing, check archive integrity, native-file hashes, source reproducibility and relative documentation links. Keep workstation paths, credentials and installation-session logs out of public packages.
