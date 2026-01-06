---
id: placeholders
title: Placeholders
slug: /references/placeholders
---
[PlaceholderAPI](https://wiki.placeholderapi.com/) allows for other plugins to display data provided by Hungergames. With its current implementation, you can use placeholders to show per-player statistics as well as global game statistics inside scoreboards, chat formats, holograms, and other supported plugins. You can also use it in place of signs for displaying info about arenas.

### Enabling placeholders
To enable the use of placeholders, simply download [PlaceholderAPI](https://modrinth.com/plugin/placeholderapi/versions), place it in your `plugins` directory. After you restart the server, HungerGames will automatically detect the presence of the plugin.

:::warning
To enable placeholders, you must first set up a database connection in settings.yml. The database acts as persistent storage for player data which serves PlaceholderAPI information to display.
:::

## Main Identifier
The PlaceholderAPI identifier for this plugin is `hungergames`. This means that all placeholders for this plugin must start with `hungergames_`, and the wiki will assume this prefix is added when retrieving.

## Individual Player Placeholders
If you'd like to view statistics about a specific player, you can use individual placeholders. This returns the same results as players running /hg stats. 

| Placeholder               | Description                                                                          | Example Output                         |
|---------------------------|--------------------------------------------------------------------------------------|----------------------------------------|
| `uuid`                    | UUID of player                                                                       | `6b05687f-3c9e-356f-b709-c63a9b0c71d7` |
| `username`                | Username of Player                                                                   | `CantankerousAlly`                     |
| `deaths`                  | Number of deaths during games                                                        | `5`                                    |
| `kills`                   | Number of kills during games                                                         | `12`                                   |
| `kill_assists`            | Number of assists (damaged player but not killed) during games                       | `7`                                    |
| `solo_games_started`      | Number of solo games started using the `/hg start` command                           | `3`                                    |
| `solo_games_played`       | Number of solo games played                                                          | `10`                                   |
| `solo_games_won`          | Number of solo games won                                                             | `2`                                    |
| `team_games_started`      | Number of team games started using the `/hg start` command                           | `4`                                    |
| `team_games_played`       | Number of team games played                                                          | `8`                                    |
| `team_games_won`          | Number of team games won                                                             | `1`                                    |
| `chest_opened`            | Number of chests opened during games                                                 | `45`                                   |
| `supply_drops_opened`     | Number of deaths during games                                                        | `6`                                    |
| `environment_deaths`      | Number of deaths during games to environmental reasons (fall_damage, drowning etc.)  | `2`                                    |
| `border_deaths`           | Number of deaths during games to world border damage                                 | `0`                                    |
| `player_deaths`           | Number of deaths during games to other players                                       | `9`                                    |
| `arrows_shot`             | Number of arrows shot during games                                                   | `30`                                   |
| `arrows_landed`           | Number of arrows hitting players during games                                        | `18`                                   |
| `fireworks_shot`          | Number of fireworks shot during games                                                | `8`                                    |
| `fireworks_landed`        | Number of fireworks hitting players directly during games                            | `3`                                    |
| `attacks_blocked`         | Number of attacks blocked using a sheild durin games                                 | `5`                                    |
| `potions_used`            | Number of potions used during games                                                  | `3`                                    |
| `food_consumed`           | Number of food items (including liquids excluding potions) consumed during games     | `20`                                   |
| `totems_popped`           | Number of Totem of Undyings used during games                                        | `1`                                    |
| `damage_dealt`            | Amount of damage dealt to living entities (players and mobs) during games            | `178.5`                                |
| `projectile_damage_dealt` | Amount of projectile damage dealt to living entities (players and mobs) during games | `64.0`                                 |
| `damage_taken`            | Amount of damage taken during games                                                  | `142.33`                               |
| `projectile_damage_taken` | Amount of projectile damage taken during games                                       | `55.0`                                 |
| `health_regenerated`      | Amount of health regenerated during games                                            | `72.5`                                 |
| `solo_percentile`         | Average player placement percentile during solo games                                | `75.4`                                 |
| `team_percentile`         | Average player placement percentile during solo games                                | `62.1`                                 |
| `last_login`              | Date of last login                                                                   | `2026-01-03`                           |
| `last_logout`             | Date of last logout                                                                  | `2026-01-03`                           |
| `seconds_played`          | Number of seconds spent alive during games                                           | `5187`                                 |
| `seconds_played_month`    | Number of seconds spent alive during games this month                                | `732`                                  |

*Note: Floating point numbers are rounded to 2 decimal points*

## Global Player Placeholders

Global placeholders use the same keys as individual ones, but uses more parameters for the position and type of data. It follows the following command

```leaderboard_top_<rank>_<stat>_<name|value>```

- Replace <rank> with the position on the leaderboard to display, for example `leaderboard_top_**1**_<stat>_<name|value>`
- Replace <stat> with the stat to display, for example `leaderboard_top_<rank>_**kills**_<name|value>`
- Replace <name|value> with either `name` or `value` depending on whether you want to display the stat or player with said stat, for example `leaderboard_top_<rank>_<stat>_**name**`

## Slot Placeholders
If you'd like to use custom signs in your plugins, you can use these to display information about arenas.

| Placeholder                 | Description                                      | Example Output |
|-----------------------------|--------------------------------------------------|----------------|
| `slot_<slot_name>_world`    | Name of arena related to slot                    | `Seacliff`     |
| `slot_<slot_name>_progress` | Whether the game is in progress or waiting       | `In Progress`  |
| `slot_<slot_name>_players`  | Numbers of players alive or spawnpoints occupied | `13 Alive`     |

- Replace <slot_name> with the name of the slot, for example `slot_seacliff_progress`
