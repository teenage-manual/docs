# Teenage Engineering Device Manuals

Community-maintained manuals for [teenage manual](https://teenagemanual.com) - an interactive guide for Teenage Engineering devices.

## Structure

```
docs/
├── images/                    # Shared images
│   └── ...
├── ep-133/                    # Device folder
│   ├── _meta.json             # Device metadata
│   ├── basics/                # Category folder
│   │   ├── getting-started.md
│   │   ├── workflow.md
│   │   └── ...
│   ├── sampling/
│   │   ├── sampling.md
│   │   ├── chop.md
│   │   └── ...
│   └── effects/
│       └── ...
└── ...
```

### Devices

| Folder | Device | Orientation |
|--------|--------|-------------|
| `ep-133/` | KO II | horizontal |
| `ep-1320/` | EP-1320 Medieval | horizontal |
| `ep-40/` | EP-40 Riddim | horizontal |
| `op-1/` | OP-1 | horizontal |
| `op-1f/` | OP-1 Field | horizontal |
| `op-xy/` | OP-XY | horizontal |
| `tx-6/` | TX-6 | horizontal |
| `tp-7/` | TP-7 | vertical |
| `cm-15/` | CM-15 | vertical |

### Categories

Place your topic file in the appropriate category folder:

| Folder | Description |
|--------|-------------|
| `basics/` | Getting started, core concepts |
| `sampling/` | Recording, editing, chopping samples |
| `sequencing/` | Patterns, recording, step editing |
| `effects/` | FX, filters, processing |
| `synthesis/` | Synth engines, sound design |
| `tape/` | Tape recording (OP-1 specific) |
| `mixing/` | Levels, EQ, compression |
| `recording/` | Audio input, mic setup |
| `connectivity/` | MIDI, USB, sync |
| `advanced/` | Power user features |

## Contributing

1. Fork this repo
2. Add or edit a markdown file in the appropriate `device/category/` folder
3. Submit a pull request

When a PR is merged, the site automatically rebuilds and deploys with your changes.

### Topic File Format

Each topic is a markdown file with YAML frontmatter:

```markdown
---
title: "Topic Title"
---

Your content here...
```

**Required fields:**
- `title` - Display title (use Title Case for SEO)

**Optional fields:**
- `image` - Filename of an image in the `images/` folder

The category is determined by which folder the file is in - no need to specify it!

### Device Metadata (`_meta.json`)

Each device folder contains a `_meta.json` file:

```json
{
  "name": "Device Display Name",
  "image": "te-device-slug.png",
  "orientation": "horizontal",
  "categoryOrder": ["basics", "sampling", "sequencing", "effects", "advanced"]
}
```

- `name` - Display name shown on the site
- `image` - Device image filename (in `images/` folder)
- `orientation` - Either `horizontal` or `vertical` (affects layout)
- `categoryOrder` - Order of categories in the sidebar (categories not listed appear at the end)

### Adding Images

1. Add your image to the `images/` folder
2. Reference it in the topic frontmatter: `image: "your-image.png"`
3. Keep images optimized (PNG or WebP, reasonable file size)

### Adding a New Topic

1. Pick the right device folder (e.g., `ep-133/`)
2. Pick the right category folder (e.g., `basics/`)
3. Create a new `.md` file (e.g., `my-topic.md`)

The URL will be: `teenagemanual.com/ep-133/my-topic`

### Adding a New Device

1. Create a new folder with the device slug (e.g., `ob-4/`)
2. Add a `_meta.json` file with device info
3. Create category subfolders as needed
4. Add topic markdown files
5. Add the device image to `images/`

### Content Guidelines

- Keep formatting consistent with existing content
- Use lowercase in content where possible (matches TE style)
- Use Title Case for topic titles (better for SEO)
- Be accurate - reference official TE documentation
- Focus on practical, actionable information

## License

Content is provided under MIT License. This project is not affiliated with Teenage Engineering.

## Credits

Maintained by [ivan.codes](https://ivan.codes)
