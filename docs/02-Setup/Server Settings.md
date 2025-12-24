---
id: server-settings
title: Server Settings
slug: /setup/server-settings
---

Since this plugin modifies the game in a major way, it is recommended to change some server settings to ensure the plugin runs optimally. These changes can be made by editing the `server.properties` file. Further instructions on editing config files can be found in the [Editing Config Files](/docs/06-References/Editing%20Configs.md) section. This page contains the recommended settings for the HungerGames plugin.

:::info
Certain forks of Spigot, including Paper, provide additional performance-focused configuration options that can influence particle and entity visibility distances. Server administrators may adjust these settings as required.
:::

:::warning
Some keys in the file may differ between Minecraft Versions. Please refer to the [Minecraft Wiki](https://minecraft.wiki/w/Server.properties) latest updates and defaults.
:::

### **Allow Flight**
```yaml
allow-flight=true
```
Setting this to true ensures that players don't get kicked from the server when they're jumping in the spawnpoints before a game.

### **Entity Broadcast Range**
```yaml
entity-broadcast-range-percentage=500
```
A high value ensures that the **Supplydrop Fireworks**, which indicate the locations of supplydrops that spawned, can be visible from a distance.

### **Force Gamemode**
```yaml
force-gamemode=true
```
Setting this to true ensures that when players join the game, their Gamemode is set to the correct one.

### **Gamemode**
```yaml
gamemode=adventure
```
Recommended to have it at Adventure since it doesn't allow players to break blocks. Can also be set to Survival to allow players to break certain blocks. For more info on allowing certain blocks to be broken, visit [Plugin Settings](/docs/04-Configuration/Plugin%20Settings.md).

### **Spawn Protection**
```yaml
spawn-protection=0
```
Setting this to 0 disables Spawn Protection, which is needed so that players can click on signs, open chests and break blocks near the world spawn.

## **Next Steps**
After configuring the settings, proceed to the [Worlds](Worlds.md) section to set up the worlds for HungerGames.

---

If you have any more questions about this process or encounter issues related to this, visit our [Discord Server](https://discord.gg/qcRfPHnZtp)




