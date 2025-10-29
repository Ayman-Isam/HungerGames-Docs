---
id: worlds
title: Worlds
slug: /setup/worlds
sidebar_position: 3
---

To function properly, the plugin requires at least 2 worlds dedicated to HungerGames, one lobby world and one arena. This page contains the instructions on how to set the worlds up.

## **General World Setup**
Before using the HungerGames plugin, you'll need to set up the worlds where players will interact. These include the **Lobby World**, where players gather before and after games, and the **Arena Worlds**, where the games take place. Follow the steps below to prepare your worlds.

### **Step 1: Creating world**
If you already have a world on your server that you want to use, you can move on to Step 2. Otherwise, you can:

- **Modify an Existing World:** Use the default world that is automatically created when the server starts, or generate a new world specifically for your needs. You can create the new world directly on the server or generate it in single-player mode and then upload it to your server. If desired, you can use world generation tools or plugins to customize the world during creation.

- **Download a Pre-Built World:** You can find pre-built worlds online that match your needs. After downloading, add the world folder to the root directory of your server.
The root directory is the main folder where all your server files are located. It typically contains subfolders like world, plugins, and logs. For example, if your server is named Server, the root directory might look like this:
```
Server/
├── world/
├── world_nether/
├── plugins/
├── logs/
├── libraries/
├── versions/
├── server.jar
├── eula.txt
├── whitelist.json
├── ops.json
├── spigot.yml
└── permissions.yml
└── ...
```
If you add a new world to the server, be sure to restart the server for the world to be tracked by the server.

:::warning

It is highly recommended to not have the name of the world folder as `world` as it can cause issues with the plugin. This is because Minecraft has limitations on what plugins can do with the world folder named `world`.

:::

:::info

If you have changed the world folder path in `bukkit.yml` using the `world-container` key, make sure to use that path instead of the default `world` folder path.

:::

### **Step 2: Teleport to the world**
To teleport to the world, use the command `/hg teleport <player-world> <world-name>`. For more information about this command, visit the [Commands](/docs/06-References/Commands.md) section.

### **Step 3: Set Spawn Location**
Set the spawn location of the world using the `/setworldspawn` command. This going to be the location players get teleported to when they join the world and when a game ends.

### **Step 4: Change Gamerules**
It is recommended to disable certain gamerules (using `/gamerule`) for a smooth experience. These are as follows:

#### **announceAdvancements: false**
Recommended to disable it to ensure that players aren't spammed with advancement notifications.

#### **doDaylightCycle: false**
Recommended to disable it to have a constant time of day to reduce distractions.

#### **doMobSpawning: false**
Recommended to disable it to ensure mobs don't disrupt gameplay.

#### **doMobSpawning: false**
Recommended to disable it to have a constant weather of day to reduce distractions.

## **Lobby world**
To set the lobby world up, first open the settings.yml file located inside the HungerGames folder inside the plugins' folder. The path is as follows:
```
Server/
├── plugins/
│   └── HungerGames/
│       └── settings.yml
│       └── ...
└── ...
```
Now change the `lobby-world` key to the name of the world you want to set as the lobby world. For example:
```yaml
lobby-world: "world"
```

For more information on how to edit yaml files, visit the [Editing Configs](/docs/06-References/Editing%20Configs.md) page.

## **Next Steps**
After configuring the settings, proceed to the [Arena](Arenas.md) section to set up the arenas for HungerGames.

---

If you have any more questions about this process or encounter issues related to this, visit our [Discord Server](https://discord.gg/qcRfPHnZtp)



