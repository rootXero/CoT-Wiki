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