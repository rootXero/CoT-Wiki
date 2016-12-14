# Usage

Currently a box to stand in for a switch, this can be placed in-level to move another object around.

This is the activation piece of a two-Blueprint set, and requires This requires the [ObjectToMove_BP](https://app.deveo.com/collegeforcreativestudies/projects/city_of_thebes/wiki/ObjectToMove_BP) to also be set up in order to work.

# Variables

| Name               | Details                                                                                                                                                                        |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ObjectToMove       | Select the object (as named in your World Outliner) to be moved. Must be an instance of ObjectToMove_BP.                                                                       |
| IsSingleActivation | If checked, this switch can only be activated once. Required for proper multi-switch use (to prevent player from pressing same switch multiple times instead of all switches). |
| IsActivator        | If checked, this functions as a functionality unlock corresponding to *TakesActivation* in ObjectToMove_BP. Both must be checked to use this feature.                          |