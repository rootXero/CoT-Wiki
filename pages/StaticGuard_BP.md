# Usage

Static guards do not chase a player, just stand in place. They are primarily intended for Level Zero, and will speak one line on approach and another when collided with. They can also affect the player's health on collision.

# Variables

| Name                | Details                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| GuardApproachString | The string printed when the guard sees a HeroChar.                                                                                   |
| GuardBumpString     | What the guard says when bumped into by a HeroChar.                                                                                  |
| BumpHealthMod       | The number of points added to the character's health when they bump into a guard. To subtract health, this value should be negative. |