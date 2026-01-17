# Teenage Engineering Device Manuals

Community-maintained manuals for [teenage manual](https://teenagemanual.com) - an interactive guide for Teenage Engineering devices.

## Structure

```
docs/
├── images/                    # Device images
│   ├── te-ep-133.png
│   └── ...
├── ep-133/                    # Device folder
│   ├── _meta.json             # Device metadata
│   ├── workflow.md            # Topic file
│   ├── sampling.md
│   └── ...
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

## Contributing

1. Fork this repo
2. Edit or add a markdown file in the relevant device folder
3. Submit a pull request

When a PR is merged, the site automatically rebuilds and deploys with your changes.

### Topic File Format

Each topic is a markdown file with YAML frontmatter:

```markdown
---
title: "Topic Title"
category: "basics"
image: "optional-image.png"
---

Your content here...
```

**Required fields:**
- `title` - Display title (use Title Case for SEO)
- `category` - One of: `basics`, `sampling`, `sequencing`, `effects`, `advanced`, `synthesis`, `tape`, `mixing`, `recording`, `connectivity`

**Optional fields:**
- `image` - Filename of an image in the `images/` folder (for topic-specific illustrations)

### Device Metadata (`_meta.json`)

Each device folder contains a `_meta.json` file:

```json
{
  "name": "Device Display Name",
  "image": "te-device-slug.png",
  "orientation": "horizontal"
}
```

- `name` - Display name shown on the site
- `image` - Device image filename (in `images/` folder)
- `orientation` - Either `horizontal` or `vertical` (affects layout)

### Adding Images

1. Add your image to the `images/` folder
2. Reference it in the topic frontmatter: `image: "your-image.png"`
3. Keep images optimized (PNG or WebP, reasonable file size)

### Adding a New Topic

Create a new `.md` file in the device folder. The filename becomes the URL slug:
- `ep-133/my-topic.md` → `teenagemanual.com/ep-133/my-topic`

### Adding a New Device

1. Create a new folder with the device slug (e.g., `ob-4/`)
2. Add a `_meta.json` file with device info
3. Add topic markdown files
4. Add the device image to `images/`

### Content Guidelines

- Keep formatting consistent with existing content
- Use lowercase where possible (matches TE style)
- Be accurate - reference official TE documentation
- Focus on practical, actionable information
- Use Title Case for topic titles (better for SEO)

## License

Content is provided under MIT License. This project is not affiliated with Teenage Engineering.

## Credits

Maintained by [ivan.codes](https://ivan.codes)
