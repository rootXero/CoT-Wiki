# Usage

1. Select "Ladder Collider (Inherited)" in the hierarchy of the Details panel .
1. Under *Transform*, the first category, set the Scale Z value to the height of the ladder needed.
1. Select "TopCollider (Inherited)" in the hierarchy.
1. Under *Transform* again, set the Location Z value to the same as your ladder's height. The TopCollider should sit on the top of the ledge you wish to have a character climb onto.
1. If you have a ladder mesh, place it on the side of the Ladder Collider that meets the TopCollider. It's important to note that for the time being, at least, this mesh is *not* part of Ladder_BP.
1. If you don't have a ladder mesh, the Blueprint will still show a panel on the floor in its location during play (the colliding mesh will be hidden).

# Variables

**Note:** Due to the current setup, the variables that need editing in this Blueprint are *not* labelled "SET TO PLAY" as usual. Steps for setup are above.

# In the Future

As is likely obvious from the slightly convoluted instructions and snapping issues, this is a very rough Blueprint. Long-term this will be remedied, hopefully with enough polish to set the location of top and bottom panels and have the engine automatically fit the appropriate number of modular pieces between them to build an actual ladder. The collider will be removed to only use the ladder mesh, and the hero character will snap to it properly regardless of approach angle (and thus allowed a controlled descent instead of having to leap back down again).



------------


# Summary

Pretty much what it says on the tin — these let the player travel up and down when they interact with them.

# Usage

Drag the Blueprint into the scene as you normally would. It will come in empty, like all Blueprints that don't have a default mesh.

## When using modular meshes:

* Under *SET BEFORE PLAY* in the Details panel, find **Ladder Sections** and hit the plus sign beside "0 Array elements." Add as many slots as you need, and load your ladder section meshes normally. If you accidentally add too many, click the smaller arrow next to the dropdown and choose "Delete."

***Note:*** *Due to the nature of how the Blueprint is set up, leaving blank elements in the Ladder Sections array will result in gaps in the resulting ladder. There are plans to fix this issue later, but as there's an easy workaround and it's been set to the back burner for the  time being in favor of finishing level mechanics.*
**AutoFill** is checked by default, but if for some reason it's become turned off, check the corresponding box.
* Scrub the **Ladder Height** value until the top of the ladder is just above the relevant platform, or hand-set it if a higher amount of precision is needed. Drop down the subsection labelled **Randomizer** and scrub **Initial Seed** to randomize the order of pieces in use until you're happy with the result.
* Test your ladder in-play to make sure that it's properly aligned to your geometry and that you don't run into any unknown bugs.

## When using a single static mesh:

* Uncheck **Auto Fill** under *SET BEFORE PLAY*
* Find and select **DefaultSection (Inherited)** in the component hierarchy of the Details panel.
* Set the Static Mesh and Materials as desired.

Test your ladder in-play to make sure that it's properly aligned to your geometry and that you don't run into any unknown bugs.

# Variables


| Name             | Details                                                                                                                 | Revision No. |
|------------------|-------------------------------------------------------------------------------------------------------------------------|--------------|
|                  | **SET BEFORE PLAY**                                                                                                     |              |
| LadderHeight     | The height from the base of the ladder to the desired step off point. Rounds up automatically to the next ladder piece. | 136          |
| LadderSections   | The sections of the ladder to be randomly selected from as the ladder builds.                                           | 136          |
| AutoFill         | Turn on to build ladders dynamically from modular pieces. Turn off to use one prebuilt mesh.                            | 136          |
| HideBasePlatform | Hides the tile at the base of the ladder Blueprint in-editor (it is always hidden in-game).                             | 136          |
| Randomizer       | Seed for the random stream. Change this value to change the random order of ladder sections.                            | 136          |

# Known Bugs

* *Editor Panel Adjustment:* The construction script is meant to work by simply dragging the top and bottom platforms into place in the editor, instead of having to scrub a variable in the Details panel, as it would be more precise and intuitive. An update in UE 4.9 introduced a bug that doesn't propagate editor component transformations into the construction script, however (See: [UE-21838](https://issues.unrealengine.com/issue/UE-21838 "Unreal Issue Report Page"))
* *Approach Velocity:* When approaching at certain angles, pressing the Interact key within range of a ladder will attempt to snap the player character to the root properly, but velocity is maintained leading to undesireable results (being snapped in place off the ladder, where there's no way down, or falling backwards off a ledge instead of locking on properly). This is most easily replicable by running backwards towards the top of a ladder and pressing Interact just before touching the ladder geometry, which results in the aforementioned snap/lock failure.
* *Ladder Gaps:* Leaving blank elements in the LadderSections array will result in gaps in the built ladder. This is due to a lack of a null check when pulling objects from the array, and will be resolved when there aren't so many immediate issues waiting to be addressed. There is also a related divide by zero issue that doesn't affect the result at all, but throws errors in the output log and will be addressed at the same time as the null check fix.