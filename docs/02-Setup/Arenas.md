---
id: arenas
title: Arenas
slug: /setup/arenas
---

Arenas are a crucial part of the plugin as they are where the games take place. You can set up multiple arenas but at least one is required for the plugin to function. The arenas dictate where supply drops are spawned, where chests are refilled along with other features of the plugin. This page contains the instructions on how to set up each arena for HungerGames.

## **Selecting an Arena World**
To set up an arena in a world, you need to first be in that arena world. To teleport to the world, run the `/hg teleport <player_name|all> <world_name>` command. 

## **Creating an Arena Region**
To create an arena, you need to follow the steps below:

### **Step 1: Selecting the Region**
To select the region for the arena, you can use the `/hg select` command. This command gives you an Arena Selector Tool (Blaze Rod) to select the region for the arena. The region should be a rectangle with the corners being the two points you select. To select the first point, left-click the block with the arena selector tool and for the second point, right-click. You can select each block multiple times to get the exact region you want. 

### **Step 2: Creating the Arena**
Once you're happy with the region, run the `/hg create` command to create the arena. You can also use this command multiple times until you're satisfied with the region. This saves the region to the `arena.yml` file in the folder `plugins/HungerGames/<world_name>/`. You can edit this file to change the region later on.

## **Setting Up the Arena**
After creating the arena, you can set up the arena by following the steps below:

### **Step 1: Set World Border**
To set the world border for the arena, run the `/hg border <num_blocks> <center_x> <center_z>` command. The `num_blocks` argument is the number of blocks from the center of the world to the edge of the border. The `center_x` and `center_z` arguments are the coordinates of the center of the world border. This can also be done in the config.yml file in the `plugins/HungerGames/<world_name>/` folder.

### **Step 2: Set Spawn Points**
Before selecting the spawn points for the arena, you need blocks to set them on. You can use any block for this purpose. Generally, players are spawned at the center of the arena on slightly elevated platforms.

To set the spawn points for the arena, you can use the `/hg setspawn` command. This command gives you a Spawn Point Selector Tool (Stick) to set spawn points for the arena. This is where players get teleported to when they join the game before starting the game. To select a spawn point, left-click the block with the spawn point selector tool. To remove a spawn point, right-click the block.

### **Step 3: Set up Chests**
Chests are an important part of the plugin as they contain items that players can use to survive. The plugin supports 3 different types of chests, regular chests, trapped chests, and barrels. Be sure to remove other types of chests, such as ender chests and shulker boxes from the arena to avoid confusion. Once you've placed the desired number of each type of chest, run the `/hg scanarena` command to save the locations of the chests in the arena for optimization purposes. This will ensure that the scanned chests are refilled throughout the game.

## **Next Steps**
After setting up the arena, proceed to the [Signs](Signs.md) section to configure your server settings for HungerGames

---

If you have any more questions about this process or encounter issues related to this, visit our [Discord Server](https://discord.gg/qcRfPHnZtp)
