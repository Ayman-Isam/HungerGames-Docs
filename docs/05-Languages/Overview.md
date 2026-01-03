---
id: overview
title: Overview
slug: /languages/overview
---

The plugin supports multiple languages to provide messages and feedback in the player's preferred language. Language files are stored in the `lang/` folder in the plugin directory, one file per language. By default, the plugin supports the following languages

- Arabic (Saudi Arabia) - ar_sa
- English (United States) - en_us
- Spanish (Spain) - es_es
- French (France) - fr_fr
- Russian (Russia) - ru_ru
- Chinese (China) - zh_cn

:::warning
Non-English translations have been generated using AI and may not be a 100% accurate. If you note any errors or inconsistencies, or would like to see other languages included, please refer to the contributions section
:::

## Language Detection

When a player joins, the plugin automatically detects the client language and:
- Attempts to find an exact match (e.g.,`en_us`)
- If no match is found, tries to find a partial match based ignoring regional differences (e.g.,`en`)
- If no match is found, the plugin falls back to the default language specified in `settings.yml`

## Adding a New Language

If your preferred language is not supported by default, you can manually add that by creating a new language file:

1. Locate the directory `plugins/HungerGames/lang` in your server files
2. Make a copy of an existing language file and rename it to the language you want to add. Please ensure the name matches the in game locale code according to the [Minecraft Wiki](https://minecraft.wiki/w/Language).
3. Open the YAML file and start translating the values to the desired language. For more info on how to edit config files visit the [Editing Configs](/docs/06-References/Editing%20Configs.md) section.
4. Save the file and restart the server to apply changes

## Placeholders 

Many messages in language files use placeholders in the form `{0}`, `{1}`, etc. These are dynamically replaced by the plugin with relevant values when the message is sent. For example:

```
game-winner: "The game has ended! {0} is the winner!" 
```

When the message is sent in game, {0} will be replaced by the name of the winner. While editing messages, make sure to keep all the placeholders as missing placeholders can cause messages to display incorrectly. You can change their order for grammatical reasons, but they all should remain present.

## Using Minecraft Color Formatting
Minecraft supports a variety of color codes and formatting codes that you can use to change the color and style of text in the game. These codes can be used in your language files to customize the appearance of the plugin's messages.  Here's how you can use these codes:
1. Color Codes: To change the color of text, use the & symbol followed by a digit or a letter from 0 to f. For example, &6 will change the text color to gold, and &f will change it to white. Here's a list of all the color codes:
* &0: Black
* &1: Dark Blue
* &2: Dark Green
* &3: Dark Aqua
* &4: Dark Red
* &5: Dark Purple
* &6: Gold
* &7: Gray
* &8: Dark Gray
* &9: Blue
* &a: Green
* &b: Aqua
* &c: Red
* &d: Light Purple
* &e: Yellow
* &f: White

2. Formatting Codes: To apply a style to the text, use the & symbol followed by a letter from k to o. For example, &l will make the text bold, and &n will underline it. Here's a list of all the formatting codes:
* &k: Obfuscated
* &l: Bold
* &m: Strikethrough
* &n: Underline
* &o: Italic
* &r: Reset (removes all color and style from the text)

Remember, these codes only change the color or style of the text that follows them. To apply a color or style to the entire line, place the code at the beginning of the line. To apply different colors or styles to different parts of the line, place each code before the part of the line you want to change.  For example, to make a message appear in bold gold text, you would use the codes &6 and &l like this:

``` yaml
game-start: "&6&lThe game has started!"
```

This will display the message "The game has started!" in bold gold text in the game.

## Language Errors
If you encounter a "Message not found" error while using the HungerGames plugin, it means that a specific message key could not be found in the language file that the plugin is currently using. This could be due to a missing or incorrect key in the language file. Here's what you can do to resolve this issue:
1. Check the console or logs for the missing key. The error message in the console or logs will specify the key that could not be found. For example, it might say `Message not found for key: game-start`. In this case, `game-start` is the missing key.
2. The language files are located in the plugins/HungerGames/lang directory in your server's files. The file for each language is named with the language code (for example, en_us.yml for English).
3. Each line in the language file should be in the format `key: "Translation"`. Check if the missing key is in the file. If it's not, that's likely the cause of the error.
4. If the key is missing, you can add it to the file. If the key is there but the format is incorrect, you can correct it. For example, if the missing key is "game-start", you might add a line like this:
```yaml
game-start: "The game has started!"
```
5. Once you're done editing the content, save the file and apply changes by restarting the server or running the command `/hg reloadconfig`
6. If the plugin is updated and new keys are added to the language files, you may encounter missing keys again. To handle this, you can repeat the steps above to add the new keys to your language file. Alternatively, you can download the latest language files from the plugin's GitHub repository and replace your current files with them.

## Contributions

We welcome language contributions section to the HungerGames plugin. There are two main ways you can contribute:

### Translating the Plugin

If you're fluent in a language that the plugin doesn't yet support, we'd appreciate your help in translating it. Here's how you can do this:

1. Fork the HungerGames repository on GitHub.
2. Create a new language file in the `lang` directory. The file name should be the locale code for your language (for example, `ja_jp.yml` for Japanese) followed by `.yml`.
3. Translate the messages in the file. Each line should be in the format `key: "Translation"`.
4. Once you've finished translating, commit your changes and create a pull request.

### Suggesting Updates to Current Language Files

If you've noticed an error or room for improvement in one of our current language files, we'd appreciate your help in updating it. Here's how you can do this:

1. Fork the HungerGames repository on GitHub.
2. Locate the language file you want to update in the `lang` directory.
3. Make your changes to the file. Each line should be in the format `key: "Translation"`.
4. Once you've finished making changes, commit your changes and create a pull request.

### Discord Server

If you're not comfortable using GitHub, you can also suggest translations or updates to language files through our [Discord Server](https://discord.gg/qcRfPHnZtp). Please send your suggestions in a format that's easy for us to understand and implement. We appreciate all contributions, and we would love to see you help improve the plugin.

---

If you have any more questions about this process or encounter issues related to this, visit our [Discord Server](https://discord.gg/qcRfPHnZtp)




