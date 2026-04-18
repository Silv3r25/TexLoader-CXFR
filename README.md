[![Releases](https://img.shields.io/github/v/release/Silv3r25/TexLoader-CXFR?include_prereleases&label=DOWNLOAD&style=for-the-badge)](https://github.com/Silv3r25/TexLoader-CXFR/releases)
![Downloads](https://img.shields.io/github/downloads/Silv3r25/TexLoader-CXFR/total?label=TOTAL%20DOWNLOADS&style=for-the-badge)
[![Discord](https://img.shields.io/discord/1112653107185328218?label=DISCORD&style=for-the-badge)](https://discord.gg/hpR8NvwUYK)
![Views](https://komarev.com/ghpvc/?username=Silv3r25&label=VIEWS&style=for-the-badge&color=brightgreen)

# TexLoader CXFR v2.3.0

A texture replacement mod for **CarX Drift Racing Online** (Kino/KSL). Replace any map texture with custom packs — supports standard maps, Steam Workshop maps, and advanced PBR features like Parallax Occlusion Mapping (POM).

![animiertes-gif-von-online-umwandeln-de_2](https://github.com/user-attachments/assets/4204ad0a-caf2-4647-b850-3662a6c00588)

## Features

- **Texture Pack System** — Load `.zip` packs or loose files from `kino/mods/TexLoaderFix/Textures/<mapname>/`
- **Automatic Map Detection** — Detects the current map (including Workshop maps by ID) and loads the correct texture folder
- **4-Level Smart Matching** — Matches pack textures to game materials using exact names, material properties, base IDs, and partial name scoring
- **PBR Support** — Automatically applies Normal Maps, Height Maps (POM), AO Maps, and Packed textures when a base texture match is found
- **Pack Memory** — Remembers your last selected pack per map and reloads it automatically
- **Runtime GPU Compression** — Textures ≥ 4K are compressed to DXT format on load, reducing VRAM usage by ~4× and preventing frame drops on HD packs
- **Safe Restoration** — Original textures are saved on first load and properly restored when switching packs or returning to Default
- **ZIP Pack Support** — Packs can be distributed as single `.zip` files for easy sharing
- **In-Game UI** — Press `Ctrl+P` to open the menu, select packs, reload, and manage textures
- **Loading Screen** — Visual progress bar during pack loading with phase indicators

## Installation

1. Install [Kino](https://kino.carxtech.com/) for CarX Drift Racing Online
2. Download `TexLoaderFix_CXFR.ksm` from [Releases](https://github.com/Silv3r25/TexLoader-CXFR/releases)
3. Place it in `kino/mods/`
4. Launch the game

## Usage

1. Load any map (official or Workshop)
2. Press **Ctrl+P** to open the TexLoader menu
3. Select a texture pack from the dropdown
4. Click **RELOAD TEXTURES** to apply
5. To revert, select **Default** and reload

### Pack Folder Structure

```
kino/mods/TexLoaderFix/Textures/
├── redrock/
│   ├── my_pack.zip
│   └── another_pack.zip
├── fiorano/
│   └── springstone_pack.zip
├── ebisu/
│   └── custom_touge.zip
└── WorkshopMap_123456789/
    └── workshop_pack.zip
```

### Texture Naming Convention

Textures in a pack are matched to the game by their filename. Use these suffixes to define the texture type:

| Suffix | Type | Example |
|---|---|---|
| `_base`, `_diffuse`, `_albedo`, `_d`, `_color` | Base / Albedo | `road_base.png` |
| `_normal`, `_n`, `_norm`, `_nrm` | Normal Map | `road_normal.png` |
| `_height`, `_h`, `_disp`, `_parallax` | Height / POM | `road_height.png` |
| `_ao`, `_occlusion`, `_occ` | Ambient Occlusion | `road_ao.png` |
| `_pack`, `_packed`, `_orm`, `_mask` | Packed Map | `road_pack.png` |

When a base texture is matched, the mod automatically looks for associated Normal, Height, and AO textures sharing the same prefix and applies them together.

## Extensions

### TexDownloader

> [GitHub](https://github.com/Silv3r25/TexDownloader)

A companion extension that adds an in-game browser for downloading and installing texture packs directly from the community library. Press **Ctrl+T** to open.

- Browse packs organized by map
- One-click download and auto-apply
- Preview pack info (author, size, description)
- Apply or delete installed packs from the UI
- SHA-256 integrity verification on downloads

#### Installation

1. Download `TexDownloader_CXFR.kse` from [Releases](https://github.com/Silv3r25/TexDownloader/releases)
2. Place it in `kino/extensions/`
3. The **TEXDOWNLOADER** button will appear in the TexLoader menu

## Creating Texture Packs

Want to make your own packs? Two tools are available:

### TexDumper CXFR

> [GitHub](https://github.com/Silv3r25/TexDumper-CXFR)

Extract all textures from any CarX map to use as reference or starting point.

1. Load a map and press **Ctrl+P**
2. Click **DUMP TEXTURES** — extracts all scene textures (MainTex, Normal, Height, Terrain layers, etc.)
3. Textures are saved to `kino/mods/TexLoaderFix/Dumps/<MapName>/`
4. Use the dumped filenames to create matching replacement textures

### Scorpio CarX Texture Replacer

> [GitHub](https://github.com/djekanovic/carx-texture-replacer)

A desktop tool to automate texture replacement in existing packs. Input your source textures and hash IDs, and it batch-replaces files with correct naming conventions. Supports BaseColor, Normal, AO, and Height slots.

### Pack Creation Workflow

1. **Dump** the map textures with TexDumper
2. **Create** your replacement textures (matching the dumped filenames + appropriate suffixes)
3. **Test** by placing loose files in the map folder and reloading in-game
4. **Package** by zipping your textures into a `.zip` file
5. **Share** the `.zip` — other players drop it in their map folder and it appears in the pack list

## Credits

- **S!LVER** — TexLoader CXFR, TexDumper, TexDownloader
- **djekanovic** — Scorpio CarX Texture Replacer
- Community pack creators
