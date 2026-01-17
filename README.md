# Teenage Engineering Device Manuals

Community-maintained manuals for [teenage manual](https://teenagemanual.com) - an interactive guide for Teenage Engineering devices.

## Structure

Each device has its own folder with one markdown file per topic:

```
ep-133/
├── workflow.md
├── sampling.md
├── effects.md
└── ...
```

| Folder | Device |
|--------|--------|
| `ep-133/` | KO II |
| `ep-1320/` | EP-1320 Medieval |
| `ep-40/` | EP-40 Riddim |
| `op-1/` | OP-1 |
| `op-1f/` | OP-1 Field |
| `op-xy/` | OP-XY |
| `tx-6/` | TX-6 |
| `tp-7/` | TP-7 |
| `cm-15/` | CM-15 |

## Contributing

1. Fork this repo
2. Edit or add a markdown file in the relevant device folder
3. Submit a pull request

### File Format

Each markdown file should have YAML frontmatter:

```markdown
---
title: "Topic Title"
---

Your content here...
```

### Adding a New Topic

Create a new `.md` file in the device folder. The filename becomes the URL slug (e.g., `ep-133/my-topic.md` becomes `/ep-133/my-topic`).

### Adding a New Device

Create a new folder with the device slug (e.g., `ob-4/`) and add topic files inside.

### Guidelines

- Keep formatting consistent with existing content
- Use lowercase where possible (matches TE style)
- Be accurate - reference official TE documentation
- Focus on practical, actionable information

## License

Content is provided under MIT License. This project is not affiliated with Teenage Engineering.

## Credits

Maintained by [ivan.codes](https://ivan.codes)
