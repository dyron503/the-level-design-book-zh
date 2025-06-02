# Gates

In level design, a gate is anything that blocks player [flow](../../flow/) , usually along a [critical path](../criticalpath.md).

Gating is an abstract concept, it is not necessarily a literal gate or door. It could be a magic barrier, an NPC blocking a doorway until you complete their quest, or an avalanche of rocks that falls behind the player. Anything that blocks player movement is functioning as a gate.

Gating is also a verb: "we have to gate the player inside the arena until they complete the boss fight..."

## Gate types

### Strictness
  * Hard gate: players must always complete the encounter with no shortcuts (e.g. wait until a timer elapses, defeat all enemies, loot a key from a defeated boss)
  * Soft gate: can potentially exit early, but must usually complete the encounter (e.g. exit mechanism requires staying in a vulnerable position, so most players clear the arena first)
  * Hidden exit: the player must explore the arena to find the exit (e.g. an exit hidden in a corner that most players won't notice until after clearing the arena)

### Direction
  * Forward gate: player's forward progress is blocked.
  * Backward gate / one-way entrance: player cannot backtrack.

## Lock and key gates

A lock and key gate is a hard gate that prevents the player from passing through until they find the "key" somewhere else in the level. This key is abstract -- it can be a literal key item that the player picks up, or it could be a button.

Some best practices with implementing lock and key gating:
  * Show the lock before the key. When the player finally finds a key, they might remember the locked door they encountered earlier. If you do it the other way around, it will feel less like the player solved a problem, and more like they accidentally stumbled on the lock with the key already.
  * Remind the player about the lock when they get the key. Maybe the key is on a balcony overlooking the lock, or the button is aligned with a window facing the lock. Nonrealistic projects could script a brief cutscene that shows the unlock.
  * If the lock requires multiple keys, the lock's visual design should hint at the key count. For example, a locked door that requires three keys should have three keyholes.

## Shortcuts

A shortcut is a hard gate that the player can unlock from the other side, allowing easier backtracking and/or better flow between areas. Exploration games often feature one way doors, climbable ladders that drop down, or elevators that turn on.
