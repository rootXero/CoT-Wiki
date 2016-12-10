# Summary

ObjectToMove_BP is a flexible Blueprint that has a wide variety of uses. As the name implies, this Blueprint allows an object to be transformed in-game, currently upon a switch press (see *In the Future* section of this article for extended plans).

Examples of things that this Blueprint can be used for are raising platforms, opening doors, and elevators.

# Usage

Drop into the location of the asset you’d like to move. In the Details panel, select **“ObjectToMove (Inherited)”** from the hierarchy list, then change the Static Mesh to the asset you want to use. If necessary, change the transform scale of the object in the same panel.

This also requires an [ObjectMoveSwitch_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/ObjectMoveSwitch_BP) to be set up in order to work.

# Variables


| Name               | Details                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ObjectFinalOffset  | The number of units that the object will move along each axis to its final destination from its initial location, set in the details panel of the editor per instance. If IsElevator is set to True, this value is ignored.                                                                           |
| IsElevator        | Check if this object is an elevator that should only move up and down, reversing on each switch press.                                                        |
| ElevatorOffset    | The Z-offset of the elevator from its initial position. If the elevator starts at the top of its movement range and goes down, this value should be negative. |

# In the Future

I'm currently working on implementing the ability to set multiple switches for the same object, all of which must be pressed to activate the object's movement (for use with multi-switch doors, etc.)

I also plan to add the ability to have the object move on direct interaction, switched on and off in the editor with a boolean value. This can be used for elevators or other objects we wish to move without needing to press a dedicated switch.

Additionally, if requested it would be fairly simple to add in the ability to rotate or scale the object as well upon interaction. If this is something that would be useful, let the Tech team know.