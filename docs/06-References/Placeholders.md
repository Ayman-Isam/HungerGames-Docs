---
id: placeholders
title: Placeholders
slug: /references/placeholders
---
[PlaceholderAPI](https://wiki.placeholderapi.com/) allows for other plugins to display data provided by Hungergames. With its current implementation, you can use placeholders to show per-player statistics as well as global game statistics inside scoreboards, chat formats, holograms, and other supported plugins.

### Enabling placeholders
To enable the use of placeholders, simply download [PlaceholderAPI](https://modrinth.com/plugin/placeholderapi/versions), place it in your `plugins` directory. After you restart the server, HungerGames will automatically detect the presence of the plugin.

:::warning
To enable placeholders, you must first setup a database connection in settings.yml. The database acts as persistent storage for player data which serves PlaceholderAPI information to display.
:::

