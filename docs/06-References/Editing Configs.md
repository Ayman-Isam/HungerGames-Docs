---
id: editing-configs
title: Editing Config Files
slug: /references/editing-configs
sidebar_position: 2
---

When using Minecraft plugins, it's common to edit configuration files to customize gameplay, mechanics, or features. These files often come in two main formats: YAML (.yml) and Properties (.properties). Below is a guide on understanding and safely editing these files.

## **Configuration Formats**
YAML and Properties files are the two primary formats for configuring Minecraft servers and plugins:

YAML and Properties files are the two primary formats for configuring Minecraft servers and plugins:

- **YAML**: This format is the most commonly used in Minecraft plugins due to its flexibility and ability to organize settings in a clear and readable way. YAML files are used for plugin settings and feature customization.
- **Properties**: This format is less common and primarily used for the server's `server.properties` file, which contains basic server settings like player limits and game modes.

###

### **YAML Files**

YAML ("YAML Ain't Markup Language") is a human-readable format designed for easy configuration. The key features of these files are as follows:

1. **Settings as Key-Value Pairs**: YAML uses pairs like `setting: value` to specify settings.

   Example:
   ```yaml
   plugin-enabled: true
   max-players: 50
   world-name: "example_world"
   ```

2. **Organizing Information with Indentation**: Use spaces (never tabs) to group related settings. Think of it like a folder structure.

   Example:
   ```yaml
   teams:
     red:
       color: "red"
       max-players: 5
     blue:
       color: "blue"
       max-players: 5
   ```

3. **Lists for Multiple Items**: Lists start with a dash (`-`).

   Example:
   ```yaml
   enabled-worlds:
     - "world1"
     - "world2"
     - "world3"
   ```

4. **Adding Notes with Comments**: Start comments with `#`. These lines are ignored by the game.

   Example:
   ```yaml
   # Enable or disable the plugin
   plugin-enabled: true
   ```

### **Properties Files**

Properties files are simple text files used for basic server settings, like the `server.properties` file. While less common than YAML, they're essential for setting up your Minecraft server. The key features of these files are as follows:

1. **Settings as Key-Value Pairs**: Use `setting=value` to specify settings.

   Example:
   ```properties
   max-players=20
   level-name=world
   allow-flight=true
   ```

2. **Adding Notes with Comments**: Start comments with `#`. These lines are ignored by the game.

   Example:
   ```properties
   # Minecraft server properties
   max-players=20
   ```

3. **No Advanced Features**: Properties files are straightforward and don't support lists or grouping settings like YAML does.

## **Editing Files**

:::danger

Before making any changes to your configuration files, **always create a backup**. This ensures that you can restore the original version if anything goes wrong. Many Minecraft server hosting providers offer automated backup options, or you can manually copy files to a separate location.

:::

When editing configuration files, such as YAML or Properties files for Minecraft servers, it's important to use the right tools to avoid errors and maintain proper formatting. Below is a guide on how to safely edit configuration files, including a comparison of IntelliJ IDEA, VS Code, and Notepad, as well as insights on editing files directly through hosting providers' online file systems.

### **Online vs Offline**

Many Minecraft server hosting providers offer tools to manage and edit configuration files directly in the file system. These tools typically include:

- **File Manager:** Most hosting companies provide a web-based file manager. This allows you to edit configuration files directly through a browser, making it quick and convenient. However, these online editors are often limited in functionality — they lack advanced features like syntax highlighting, error checking, and auto-completion. Furthermore, there's no easy "undo" feature, making it riskier for complex edits, as mistakes are harder to reverse.

- **File Download and Upload:** You can download configuration files from your server, edit them locally using a desktop editor, and then upload the updated files back to the server. This method provides more control over the editing process, allowing you to use full-featured editors to ensure the files are correctly formatted. Some editors, offer version control features which track changes, allowing you to revert to earlier versions of the file if needed, providing extra safety during the editing process.

### **Text Editors**

Using the right text editor is crucial when editing configuration files. Below is a breakdown of three commonly used editors:

| Feature                       | **IntelliJ IDEA**                                                                                                   | **VS Code**                                                                                | **Notepad**                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| **Platform Support**          | Windows, macOS, Linux                                                                                               | Windows, macOS, Linux                                                                      | Windows only                                                              |
| **Syntax Highlighting**       | Yes (built-in)                                                                                                      | Yes (with extensions)                                                                      | Limited (basic text)                                                      |
| **Error Checking/Validation** | Yes (built-in validation)                                                                                           | Yes (with extensions)                                                                      | No                                                                        |
| **Auto-completion**           | Yes (built-in)                                                                                                      | Yes (with extensions)                                                                      | No                                                                        |
| **Ease of Use**               | Easy (feature-rich, with built-in features)                                                                         | Easy (lightweight and user-friendly)                                                       | Very Easy (basic editor)                                                  |
| **Customization**             | High (extensive plugin support)                                                                                     | High (extensions for YAML, themes, etc.)                                                   | None                                                                      |
| **File Management**           | Integrated with project files (best for development)                                                                | Good, can handle local files and remote editing                                            | Simple file editing, no project management                                |
| **Ideal Use Case**            | Large projects, plugin development                                                                                  | General use, lightweight editing, project management                                       | Quick edits, simple tasks                                                 |
| **Validation and Formatting** | Advanced (syntax errors, structure errors, and indentations are highlighted, and automatic formatting is available) | Good (YAML validation, indentation, and automatic formatting available through extensions) | Limited (manual validation and formatting required)                       |
| **Undo/Redo**                 | Multiple undo levels with easy access, enhanced with local automatic version control for easier recovery            | Multiple undo levels with easy access                                                      | Limited or no undo capabilities                                           |
| **Installation and Setup**    | Easy (built-in features for YAML, no extra setup required)                                                          | Moderate (requires extensions for full YAML support)                                       | Quick and easy to use, but lacks features for complex YAML configurations |

## **Common Mistakes**

- **YAML**:
   - Using tabs instead of spaces for indentation.
   - Misaligned indentation levels.
   - Forgetting colons (`:`) or quotes around strings with special characters.

- **Properties**:
   - Adding extra spaces around `=`.
   - Forgetting to escape special characters using a backslash (e.g., `\u0023` for `#`).

## **Final Tips**

- **Restart Your Server**: After editing configuration files, restart the server to apply changes. Alternatively, if it's a HungerGames config file, you can run the command `/hg reloadconfig` to apply changes.
- **Check the Logs**: If something breaks, review the server logs to identify errors related to misconfigured files.
- **Refer to Documentation**: Always refer to the plugin’s official documentation for specific settings and examples. 

---

If you have any more questions about this process or encounter issues related to this, visit our [Discord Server](https://discord.gg/qcRfPHnZtp)





