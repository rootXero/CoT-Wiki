# Summary

Pickup_BP is the base Blueprint for treasure and scrap objects in-world.

# Usage

Drop into your desired location. In the Details panel, select **"Asset (Inherited)"** from the hierarchy list, then change the Static Mesh to the asset you want to use.

# Variables

| Name        | Details                                                                                                                                                                                                                                                                                                                    | Revision No. |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
|             | **SET BEFORE PLAY**                                                                                                                                                                                                                                                                                                        |              |
| Loot Value  | The number of loot/treasure points to be added to the character's counter when this object is picked up.                                                                                                                                                                                                                   |              |
| Scrap Value | The number of scrap points to be added to the character's counter when this object is picked up.                                                                                                                                                                                                                           |              |
| Is Cursed   | Check if this is a cursed treasure asset, meaning that picking it up will subtract from the character's maximum health. Cursed assets do not grant scrap and will never update the player's scrap, even if the set value is non-zero. Cursed assets may ONLY be placed with the approval of the Tech Lead or Art Director. | 94           |
| Curse Cost  | The number of health points to be deducted from the character's maximum health if this is a cursed asset. Should generally be one.                                                                                                                                                                                         | 94           |