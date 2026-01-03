---
id: signs
title: Signs
slug: /setup/signs
---

In the plugin, signs are used to display information about different arena worlds. These signs also allow players to interact with them to join specific arenas. The command `/hg slot <create|assign|remove|list> <slot_name> [world_name]` is used to set up these signs.

## **Setting Up Signs**

### **Step 1: Create slots**
Slots are used as an intermediary layer between signs and worlds. They allow signs to reference a slot, rather than a specific world, making it easier to swap or reassign worlds without updating every sign. This also allows for multiple signs to reference the same world. To create a slot run the command `/hg slot create <slot_name> <world_name>`. The slot name can be any identifier you choose, and the world name must match the name of the world folder that will be linked to the slot. 

### **Step 2: Assign slots**
To assign slots, first place signs (can be hanging or wall signs too) around the lobby. Then run the command `/hg slot assign <slot_name>` while looking at the sign, which will assign the slot with the provided name to the sign. You can assign the same slot to multiple signs for multiple entry points to the same world.

### **Step 3: Verify Signs**
Check that the signs teleport players to the correct arena world when clicked. Also ensure that the correct information is displayed on the signs. If the number of players is incorrect, it may be because the world files have not been loaded yet. To fix this, simply just click on the sign to join the arena and the number will be updated.

## **Next Steps**
After setting up the signs, you are now ready to start the game. For more information on commands that can be run to manage the plugin, visit the [Commands Section](/docs/06-References/Commands.md).

---

If you have any more questions about this process or encounter issues related to this, visit our [Discord Server](https://discord.gg/qcRfPHnZtp)

