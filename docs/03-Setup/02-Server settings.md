Since this plugin modifies the game in a major way, it is recommended to change some server settings to ensure the plugin runs optimally. These settings are located in the `server.properties` file located in the root folder of the server.

### Allow-flight
```yaml
allow-flight: true
```
Setting this to true ensures that players don't get kicked when they're jumping in the spawnpoints before a game

### Entity Broadcast Range
```yaml
entity-broadcast-range-percentage=500
```
A high value ensures that the supplydrop fireworks, which indicate the locations of supplydrops that spawned.

### Force Gamemode
```yaml
force-gamemode=true
```
Setting this to true ensures that when players join the game, their gamemode is set to the correct one.

### Gamemode
```yaml
gamemode=adventure
```
Recommended to have it at adventure since it doesn't allow players to break blocks. Can also be set to survival to allow players to break certain blocks. For more info on allowing certain blocks to be broken, visit [Plugin Settings](/docs/04-Configuration/01-Plugin%20Settings.md).

### Spawn Mobs
```yaml
spawn-animals=false
spawn-monsters=false
spawn-npcs=false
```
Recommended to have these as false to ensure that mobs don't destroy maps or distract players during the game.

### Spawn Protection
```yaml
spawn-protection=0
```
Setting this to 0 disables spawn protection which is needed so that players can click on signs, open chests and break blocks near the center.





