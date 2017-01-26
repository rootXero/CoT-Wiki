This is only a bare-bones template. If you have questions, I recommend looking at existing pages on this wiki for examples. This wiki uses Markdown formatting—if you aren't familiar with it, check the bottom right of the editing pane for the "Syntax" link for explanation.

# Summary

A brief summary of what this Blueprint is, what it does, and any important notes the level designers should know about how it functions.

# Usage

Explain how to use this Blueprint, especially any special instructions if multiple pieces are needed or if there are things that need to be set in the Details panel that aren't immediately obvious (static meshes are a common culprit).

# Variables

A table of all the publicly editable variables in this Blueprint, organized under the correct category names and ordered as they are in the Details pane. Explain in as much detail as possible what they do and any relevant data needed to use them properly, and include the number of the SVN revision in which each variable was introduced or updated.

I recommend using a site like http://www.tablesgenerator.com/markdown_tables to generate these tables, as it's faster than typing out the code yourself.

Example: 

| Name               | Details                                                                                                                                                                                                                                                                                                                                                    | Revision No. |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
|                    | **SIMPLE MOVEMENT**                                                                                                                                                                                                                                                                                                                                            |              |
| ObjectFinalOffset  | The number of units that the object will move along each axis to its final destination from its initial location, set in the details panel of the editor per instance. If IsElevator is set to True, this value is ignored.                                                                                                                                |              |
|                    | **ACTIVATORS**                                                                                                                                                                                                                                                                                                                                                 |              |
| IsInteractable     | If checked, this mesh's effects can be triggered by interacting with it directly.                                                                                                                                                                                                                                                                          | 71           |
| TakesActivation    | If checked, this mesh is locked until an activation switch is triggered. This is different from normal switch interaction in that "activator" switches only unlock effects, they don't directly cause them in any way. It is primarily intended to allow objects that use direct interaction (see IsInteractable) to still require an activator elsewhere. | 71           |
| TakesMultiSwitches | If checked, this mesh requires a set number of corresponding switches to be activated before it will execute its actions. The number must be set in MultiSwitchCount.                                                                                                                                                                                      | 71           |
| MultiSwitchCount   | The number of ObjectMoveSwitch_BP instances in the level that must be activated in order for it to execute. Obviously, that many must be set up accordingly to trigger this Blueprint.                                                                                                                                                                     | 71           |
|                    | **ELEVATOR**                                                                                                                                                                                                                                                                                                                                                   |              |
| IsElevator         | Check if this object is an elevator that should only move up and down, reversing on each switch press.                                                                                                                                                                                                                                                     |              |
| ElevatorOffset     | The Z-offset of the elevator from its initial position. If the elevator starts at the top of its movement range and goes down, this value should be negative.                                                                                                                                                                                              |              |
|                    | **BEACON EFFECTS**                                                                                                                                                                                                                                                                                                                                             |              |
| AffectsCollision   | If checked, turning on this beacon will switch the mesh's collision off.                                                                                                                                                                                                                                                                                   | 71           |
| AffectsVisibility  | If checked, turning on this beacon will switch the mesh's visibility off.                                                                                                                                                                                                                                                                                  | 71           |

# In the Future

Explain anything that you plan to do with this Blueprint in the future that is relevant to know. 