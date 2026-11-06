# Star PvP Kits

A public collection of kits for **Star PvP**.

This repository contains community-contributed kit configurations in JSON format. These kits are designed to be used across different game modes, including Duels, FFA, and other game modes supported by Star PvP.

## Repository Structure

```text
star-pvp-kits/
├── kits/
│   ├── sword.json
│   ├── nodebuff.json
│   └── boxing.json
│
├── schemas/
│   └── kit.schema.json
│
├── README.md
└── LICENSE
```

## Creating a Kit

All kits must be defined using JSON and follow the repository's JSON Schema.

Here is an example of a kit configuration:

**`kits/sword.json`**

```json
{
  "$schema": "../schemas/kit.schema.json",
  "id": "sword",
  "name": "Sword",
  "version": 1,
  "items": [
    {
      "type": "sword",
      "tier": "diamond",
      "count": 1,
      "enchantments": {
        "sharpness": 2,
        "unbreaking": 3
      }
    }
  ],
  "armour": {
    "helmet": {
      "tier": "diamond",
      "enchantments": {
        "protection": 2,
        "unbreaking": 3
      }
    },
    "chestplate": {
      "tier": "diamond",
      "enchantments": {
        "protection": 2,
        "unbreaking": 3
      }
    },
    "leggings": {
      "tier": "diamond",
      "enchantments": {
        "protection": 2,
        "unbreaking": 3
      }
    },
    "boots": {
      "tier": "diamond",
      "enchantments": {
        "protection": 2,
        "unbreaking": 3
      }
    }
  }
}
```

## Kit Properties

| Property  | Description                    |
|-----------|--------------------------------|
| `id`      | Unique identifier of the kit.  |
| `name`    | Display name of the kit.       |
| `version` | Kit configuration version.     |
| `items`   | List of inventory items.       |
| `armour`  | Player armour configuration.   |

### Items

Each item supports the following properties:

| Property       | Description                              |
|----------------|------------------------------------------|
| `type`         | Item type.                               |
| `tier`         | Item material or tier, when applicable.  |
| `count`        | Number of items.                         |
| `enchantments` | Item enchantments.                       |

### Armour

Armour is configured separately from inventory items.

Available slots:

- `helmet`
- `chestplate`
- `leggings`
- `boots`

Each armour piece supports:

- `tier`
- `enchantments`

Armour slots are optional.

## Validation

All kit configurations must comply with `schemas/kit.schema.json`.

The schema provides:

- Required property validation.
- Data type validation.
- Allowed tier validation.
- Item count validation.
- Enchantment structure validation.
- Unknown property detection.

Make sure your JSON files are valid before submitting a contribution.

## Contributing

Community contributions are welcome!

If you want to suggest a new kit or improve an existing one:

1. Fork this repository.
2. Create a new JSON file inside the `kits/` directory.
3. Follow the existing kit structure.
4. Make sure your configuration passes schema validation.
5. Open a Pull Request describing your changes.

### Contribution Guidelines

- Use lowercase IDs with hyphens when necessary.
- Give kits clear and descriptive names.
- Avoid duplicate kit IDs.
- Use valid item types and tiers.
- Keep configurations consistent with existing kits.
- Do not modify the schema unless the change is necessary and discussed.

All contributions are subject to review before being merged.

## License

See [LICENSE](LICENSE) for licensing information.
