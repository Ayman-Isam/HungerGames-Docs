---
id: commands
title: Commands
slug: /references/commands
---

This page provides detailed information about the commands available in the HungerGames plugin, along with their required permissions.

## **Main Command**

### **`/hg <subcommand> [args]`**

- **Description**: Main command for HungerGames. Subcommand is required, for example `join`, `lobby`, `start`, etc. Args optional, for example `player_names`, `world_name`, etc. 
- **Permissions**: Varies by subcommand.

## **Subcommands**

### **`/hg join <world_name>`**

- **Description**: Allows you to join the game in HungerGames. Alternative to clicking on signs in the lobby. Argument `world_name` is required, which is the name of the world you want to join.
- **Permission**: `hungergames.join` (default: true)
- **Example Usage**: `/hg join seacliff`

### **`/hg lobby`**

- **Description**: Allows you to return to the lobby in HungerGames.
- **Permission**: `hungergames.lobby` (default: true)
- **Example Usage**: `/hg lobby`

### **`/hg start`**

- **Description**: Allows you to start the game in HungerGames.
- **Permission**: `hungergames.start` (default: op)
- **Example Usage**: `/hg start`

### **`/hg spectate`**

- **Description**: Opens a gui that allows you to teleport to players while spectating after death.
- **Permission**: `hungergames.spectate` (default: true)
- **Example Usage**: `/hg spectate`

### **`/hg teamchat`**

- **Description**: Allows you to toggle team chat in HungerGames, which ensures that only your team can see your messages. Disabled by default.
- **Permission**: `hungergames.teamchat` (default: true)
- **Example Usage**: `/hg spectate`

### **`/hg select`**

- **Description**: Gives you an arena selector tool to select a region for an arena in HungerGames.
- **Permission**: `hungergames.select` (default: op)
- **Example Usage**: `/hg spectate`

### **`/hg end`**

- **Description**: Allows you to forcefully end the game in HungerGames.
- **Permission**: `hungergames.end` (default: op)
- **Example Usage**: `/hg spectate`

### **`/hg teleport <player_name|all> <world_name>`**

- **Description**: Allows you to teleport players to arenas in HungerGames. Argument `player_name` is required, which is the name of the player you want to teleport or `all` which teleports all players. Argument `world_name` is required, which is the name of the world you want to teleport the player to.
- **Permission**: `hungergames.teleport` (default: op)
- **Example Usage**: `/hg teleport steve seacliff`

### **`/hg slot <create|assign|remove> <slot_name> [worldname]`**

- **Description**: Allows you to create slots to setup signs in HungerGames. Argument `slot_name` is required, which is the name of the slot you want to create. Argument `world_name` is required for the option `create`, which is the name of the world you want to assign to the slot.
- **Permission**: `hungergames.slot` (default: op)
- **Example Usage**: `/hg slot assign seacliff`

### **`/hg chestrefill`**

- **Description**: Allows you to refill chests in HungerGames. Mainly used for testing and debugging purposes.
- **Permission**: `hungergames.chestrefill` (default: op)
- **Example Usage**: `/hg chestrefill`

### **`/hg supplydrop`**

- **Description**: Allows you to drop a supply crate in HungerGames. Mainly used for testing and debugging purposes.
- **Permission**: `hungergames.supplydrop` (default: op)
- **Example Usage**: `/hg supplydrop`

### **`/hg setspawn`**

- **Description**: Gives you a spawn point selector tool to set spawn points for arenas in HungerGames. This is where players get teleported to when they join the game before starting the game.
- **Permission**: `hungergames.setspawn` (default: op)
- **Example Usage**: `/hg setspawn`

### **`/hg create`**

- **Description**: Allows you to create an arena in HungerGames from the selected region from the select command.
- **Permission**: `hungergames.create` (default: op)
- **Example Usage**: `/hg create`

### **`/hg scanarena`**

- **Description**: Allows you to scan the arena for chests in HungerGames. This saves the locations of the chests in the arena for optimization purposes. Should be run after changing type or location of chests.
- **Permission**: `hungergames.scanarena` (default: op)
- **Example Usage**: `/hg scanarena`

### **`/hg border <num_blocks> <center_x> <center_z>`**

- **Description**: Allows you to change the size of the world border, along with its center in HungerGames.
- **Permission**: `hungergames.border` (default: op)
- **Example Usage**: `/hg border 600 0 0`

### **`/hg reloadconfig`**

- **Description**: Allows you to reload the config file for HungerGames.
- **Permission**: `hungergames.reloadconfig` (default: op)
- **Example Usage**: `/hg reloadconfig`

### **`/hg saveworld`**

- **Description**: Allows you to save the world to separate folder. Used with the `reset-world` option enabled to save the world before resetting it.
- **Permission**: `hungergames.saveworld` (default: op)
- **Example Usage**: `/hg saveworld`

### **`/hg team <player_name|all> <world_name>`**

- **Description**: Allows you to teleport players to arenas in HungerGames. Argument `player_name` is required, which is the name of the player you want to teleport or `all` which teleports all players. Argument `world_name` is required, which is the name of the world you want to teleport the player to.
- **Permission**: `hungergames.teleport` (default: op)
- **Example Usage**: `/hg teleport steve seacliff`

## **Understanding Permission Keys**
Each permission entry consists of the following keys:
- **Permission Node**: A unique identifier for the permission, usually in the format `pluginname.permission`. This node is used to reference the permission in configuration files and commands.
- **Description**: A brief explanation of what the permission allows the player to do.
- **Default**: The default value for the permission. This can be:
    - `true`: The permission is granted to all players by default.
    - `op`: The permission is granted only to server operators (players with operator status).

## **Editing Permissions**
To manage and edit permissions, you can use a permissions management plugin like [LuckPerms](https://luckperms.net/). **LuckPerms** is a powerful and flexible permissions plugin for Minecraft servers.

Once you have installed **LuckPerms**, visit the [LuckPerms Documentation](https://luckperms.net/wiki/Home) for detailed instructions on how to set up and configure permissions for HungerGames.

---

If you have any more questions about this process or encounter issues related to this, visit our [Discord Server](https://discord.gg/qcRfPHnZtp)
