# The Basics

## Using Blueprints

1. Drag the Blueprint you want to use into your level (as always, be sure you're working on the proper level and not somebody else's).
1. With the object still selected in the viewport, look in the Details panel (pinned to the lower right of the editor by default) and find the section labeled, "SET BEFORE PLAY".
1. Set all variables in this section as needed. Hover over the variable names for tooltips explaining them, and anything important you need to know about how they function.
1. Some Blueprints require multiple parts to function, or variables that are found elsewhere in the Details panel. This is especially true for high-flexibility Blueprints that can be used for multiple related tasks (ex. [ObjectToMove_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/ObjectToMove_BP), which can serve as anything from a door to an elevator), so checking the documentation for anything you haven't used before is a good habit to get into. 
1. Scale and rotate your mesh as needed in the level.
1. If you're still unsure of anything, check the Blueprint's wiki documentation.
1. If that doesn't help, get in touch with someone on the Tech team.

## The Documentation

Generally speaking, finished Blueprints should be easy and quick to use. That said, sometimes there may be a variable that needs clarification or something which needs to be adjusted that isn't in the SET BEFORE PLAY section of the Details panel.

The Blueprint section of this wiki aims to serve as a thorough explanation of every finished Blueprint that's been finished and approved for use in CoT, to minimize confusion and provide a one-stop destination to clarify any issues that might arise during the game's development. It's intended to be a supplement to the tooltips the Tech team provides in-engine.

Each page is broken down into sections explaining the purpose, expected behavior, publicly editable variables, and future plans for the code.

## Troubleshooting

Before asking the Tech team for help, you are expected to follow a few basic troubleshooting steps that should fix most basic problems:

1. Look up the documentation for the Blueprint you're using, and read through it fully.
1. Check that *all* variables in SET BEFORE PLAY are assigned, and assigned to valid values/objects. Some Blueprints, like [ObjectMoveSwitch_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/ObjectMoveSwitch_BP), only take certain types of actors. When in doubt, check the tooltips. 
1. Check that any required variables _not_ included in SET BEFORE PLAY (for instance, Static Mesh Components or nav meshes) are properly assigned. The documentation will list where any such variables can be found, and how to set them properly. 
1. Make sure you don't have an inverted numeric value — many translations or status adjustments require a negative value to lower, and a positive to raise. It's easy to tell a Blueprint to alter your health by five and accidentally give Ammon a health boost when he falls into a pit.  


## Red Flags

If you find yourself doing any of these things, stop and run through the troubleshooting steps above. If none of them solve your problem, contact Jordan:

* Creating a new Blueprint, or child of an existing Blueprint  
* Editing variables not mentioned in the documentation
* Editing the Blueprint itself

The class hierarchy and code is all carefully built to be as efficient and streamlined as possible. As a result the structure is complex and highly interdependent, and editing it without a full understanding of its inner workings can break or bog down the game. If you're not on the Tech team, and haven't received express permission from the Tech Lead, you shouldn't be editing the code in any way. Something you need? Just ask. We're here to help.

# Finished and Documented Blueprints:

**Note:** The Blueprints listed below are the *only* Blueprints finished and approved for use in CoT. All others are depricated or unfinished, and should not be added into levels moving forward.

>[DialoguePrintBox_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/DialoguePrintBox_BP)  
[EndLevelTrigger_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/EndLevelTrigger_BP)  
[HealthTrap_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/HealthTrap_BP)  
[Killbox_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/Killbox_BP)  
[Ladder_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/Ladder_BP)  
[ObjectMoveSwitch_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/ObjectMoveSwitch_BP)  
[ObjectToMove_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/ObjectToMove_BP)  
[PatrolGuard_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/PatrolGuard_BP)  
[Shrine_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/Shrine_BP)  
[StaticGuard_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/StaticGuard_BP)