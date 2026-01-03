---
id: overview
title: Overview
slug: /configuration/overview
---

The plugin uses multiple configuration files to separate global settings for world-specific settings. This ensures that each arena world can be configured independently while keeping shared settings centralized.

:::warning
Note that some files are meant to be edited by running commands through the plugin itself. While they can be directly edited, unexpected errors can occur if done incorrectly
:::

## Configuration Files

Here's a table of the different configuration files and their properties. Please note that the destination is relative to the HungerGames directory, at `server/plugins/HungerGames/`

| File         | Scope     | Edit Method | Destination                 | Notes                                    |
|--------------|-----------|-------------|-----------------------------|------------------------------------------|
| arena.yml    | Per-arena | Commands    | `<world_name>/arena.yml`    | Configure bounds of the arena            |
| config.yml   | Per-arena | Text editor | `<world_name>/config.yml`   | World specific gameplay settings         |
| items.yml    | Per-arena | Text editor | `<world_name>/items.yml`    | Loot tables and item configuration       |
| settings.yml | Global    | Text editor | `settings.yml`              | Core plugin behaviour and global options |
| setspawn.yml | Per-arena | Commands    | `<world_name>/setspawn.yml` | Locaiton for spawnpoints in an arena     |
| signs.yml    | Global    | Commands    | `signs.yml`                 | Tracks assigned signs and slots          |

## Loading of files

When the server starts, it checks for missing config files and keys, and it adds them as required. After that, it loads the required files to memory for quick access. If you make any changes to the file you can apply them by restarting the server or running the command `/hg reloadconfig`.

---

If you have any more questions about this process or encounter issues related to this, visit our [Discord Server](https://discord.gg/qcRfPHnZtp)

