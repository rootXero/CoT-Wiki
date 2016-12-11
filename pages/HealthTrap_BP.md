# Usage

When a character comes into contact with the mesh associated with this trap, a health modifier will be applied to them. This is primarily a stand-in until specific traps have been developed, and can be used to either add or subtract from the player's health as desired.

# Variables

| Name      | Details                                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HealthMod | The number of points to be added to the player's health. To subtract health, this number should be negative. At present hero characters have ten points of health a piece and will die with that number hits zero. |

# In the Future

This is a temporary stopgap for traps, and as such has very limited functionality. The Trap_BP parent class has been structured to include a much wider range of effects, and will be slowly implemented through various child classes as time allows, including speed modifiers, character injuries, and others. Traps will also have a range of scrap that can be obtained from dismantling them and, for things like slowdowns, effect times.