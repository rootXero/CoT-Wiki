# Usage

Drop into the location of the asset you’d like to move. In the Details panel, select **“ObjectToMove (Inherited)”** from the hierarchy list, then change the Static Mesh to the asset you want to use. If necessary, change the transform scale of the object in the same panel.

This requires [ObjectMoveSwitch_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/ObjectMoveSwitch_BP) to also be set up in order to work.

# Variables


| Name               | Details                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ObjectFinalOffset  | The number of units that the object will move along each axis to its final destination from its initial location, set in the details panel of the editor per instance. If IsEleveator is set to True, this value is ignored.                                                                           |
| IsElevator        | Check if this object is an elevator that should only move up and down, reversing on each switch press.                                                        |
| ElevatorOffset    | The Z-offset of the elevator from its initial position. If the elevator starts at the top of its movement range and goes down, this value should be negative. |

# In the Future

I'm currently working on implementing the ability to set multiple switches for the same object, all of which must be pressed to activate the object's movement (for use with multi-switch doors, etc.)