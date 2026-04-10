# PlanckSource
An open source toolset for making source style first person games in Godot

## Design Philosophy
### Everything's an Entity
The basic element of PlanckSource is an entity. Entities can be of multiple types: "Character", "Item", or "Actor" for example.
Entities can be created and edited with a built-in editor or even edited munally with a script for more customization.

### Characters
A charcter entity can be either a player or an NPC.
Charatcers have built in properties that determine their behavior.
TEAM : A character can either be assigned to a team, in which case they assiste their allies and attack characters on other teams (Useful for making friendly or hostile NPCs), or a character can have no assigned team in which case they are hostile to every other entity.
INVENTORY : Every character has a inventory that can be as large as you decide. There is no built-in inventory manager, only the ability for the character to switch which item in the inventory they are holding. This makes it usable in a large assortments of games from survival crafter to story-based horror.
Other Properties include model, health, no-clip, invincible, etc.

### Items
An item is anything that can be obtained by the player.
A few examples are-built in but you can make custom items through scripts.
Built in examples include melee weapon, ranged weapon.
All items must have a model or a texture.
Items have a property called countToInvSpace that will tell an inventory weather or not it should count to the inventory space and canBeHeld. Both are true by default but you may want to change them to false to add items that are used to track upgrades or powerups. This could even be used to store a whole players save progress in the inventory itself.


### Actors
Actors are typically used in environment/level design.
Actors can be a sender, receiver, or both and must have an ID with the send/recie.
They are typically used for buttons, doors, etc.