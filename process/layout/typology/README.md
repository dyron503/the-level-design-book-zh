# Typology

Abstract layout patterns for level design, with concrete examples

## What's a typology?

A typology is a layout design pattern, a class system that helps us think about layouts. It abstracts the layout -- it simplifies and generalizes the structure.

Why say "typology" instead of "type"? It's not just academics being pretentious. Adding the "-ology" part reminds us that it is a big field of study, a system of ideas connected to other ideas. "Types" is too general.

Typologies are useful for:
  * classifying different types of level design
  * [reasoning about map and design](../../../studies/overview.md)
  * open world / battle royale type projects, since a variety of typologies will usually lead to a variety of game content
  * shared design language, aids collaboration and teamwork

In the real world architecture diagram above, Maja Baldea thinks about different ways to organize apartment buildings. She abstracts (simplifies, generalizes) these buildings as windowless blocks because she's not interested in little details, she's thinking about the overall shape, [massing](../../blockout/massing/), and [composition](../../blockout/massing/composition.md), to classify different types of residential buildings.

## Elements

Beyond walls, floors, and ceilings, there's also some common gameplay elements frequently found in most levels:
  * [Cover](../../combat/cover.md). Half cover vs. full cover, hard cover vs. soft cover.
  * [Gates](./gates.md). Hard gate vs. soft gate, lock and key, forward gating vs. backward gating.

## Room typologies

Room typologies are generalized patterns for a single area / "chunk" of the level.

We use "room" as a generic term for "space." A room could be a garden, cave, etc. This dates back to 90s game engines, where outdoor spaces were rooms with sky ceilings.

### Corridor

Straight-on linear progression through the space, like a hallway, river, or canyon. Anything with a one-way trajectory through a predictable sequence of spaces could be considered a corridor.
  * High degree of authorship, control, and certainty. You know where the player must go and how much time the player will likely take.
  * To speed it up, add downward slopes, one-way drops, and bright lighting
  * To slow it down, add side areas, alcoves, and spotty lighting

#### Corridor example: house in P.T

The first person horror game P.T. (2014) made players walk down the same hallways over and over, with a looping mechanic that teleports the player back to the start once they open the door at the end. It is a powerful use of the corridor, and would've suffered with a more open layout.

Note the strong control of sightlines, forcing the player to stare through a window at the corner, or to detour into the bathroom to notice the mirror and sink. Horror tropes and ominous alcoves discourage players from moving too quickly, while linearity and familiarity culminate in a sense of foreboding, dread, and doom. All we can do is go deeper, and there is no escape.

### Switchback / Hairpin

A dead-end corridor with a visible exit when you backtrack.
  * Similar to corridor, offers a lot of control and authorship
  * Obscuring the exit encourages the player to explore the dead-end first
  * Brief confusion, mild sense of exploration and navigation

#### Switchback example: cave in Dear Esther

### Ring Around The Rosie / Combat Bowl
Small open area with [cover](../../combat/cover.md) in the middle, usually full cover like a pillar or column, resulting in a spinning / rotating flow. Especially common in fast-paced combat games, where players can "dance" / circle-strafe around the central cover while blocking enemy attacks.
  * Add a one-way drop to force a specific flow, and/or introduce some verticality

### Arena / Point of Interest (POI)
An arena is an open area with several lanes of [circulation](../../layout/flow/circulation.md) and some [cover](../../combat/cover.md) in the middle.
  * open world and battle royale designers use points of interest (POIs), big arenas anchored by a large landmark with multiple entrances and exits
  * in single player, arenas usually need [gating](./gates.md); gate players from leaving the arena early, but also gate the entrance to prevent players from pulling all the enemies into a chokepoint

#### Example: Dead Simple in Doom 2

(TODO: draw Dead Simple floorplan and critical path)

## Level typologies

Level typologies are generalized layout patterns for multiple rooms / entire levels.

### Hub-and-spoke

A larger multi-area pattern with a central area (hub) and several smaller areas / passages extending off of it (spokes). To explore different spokes, the player must return to the hub.
  * Gives unifying identity to different spokes, conveys logic to the structure
  * Needs lots of work to update the hub with each visit, or else it'll feel like backtracking
  * Can be a useful pacing tool, returning to a hub can feel like a relaxing reward
  * Gated hubs block off most spokes at the start, the player gradually unlocks shortcuts
  * [encounter](../../combat/encounter.md)

#### Example: Medical Pavilion in BioShock 1

BioShock 1 features multiple hub-and-spokes. In the beginning Medical Pavilion chapter 1

### Loopback

(TODO: diagram)

A linear progression that loops back on itself, most common in open world dungeons.
  * Similar to Corridor: lots of control and certainty with less player indecision
  * Helps an area feel structurally non-linear and plausible, even if progression is initially linear
  * Subtle loopbacks feel like closing the loop of a natural inevitable circuit
  * Overly convenient loopbacks can feel like contrived shortcuts that plead for the player's gratitude, and thus feel artificial or implausible

#### Example: (some dungeon) in Skyrim

(example: skyrim layout and screenshot)

The open world fantasy RPG Skyrim features many dungeons where the player must return to the overworld after completing the dungeon. However, backtracking often feels monotonous or rote after an area has been cleared out... (TODO: finish)

### Branching chokepoints / string of pearls

### Pass-through

### Time cave

## Multiplayer typologies

Multiplayer layouts tend to be more nonlinear, circuitous, and bidirectional, emphasizing high replay value with reusable areas. Many team-based games feature bases / spawn rooms where players can safely join the game, as well as capture points for the teams to attack and defend.

### Base / spawn room

### No man's land

### Sniper nest / sniper alley

### Figure 8
most common in classic CTF maps, Blood Gulch, etc

### Connector / Pivot
In multiplayer team games with bases and routes toward capture points

Example: CS:GO

### Three lane
Example: League of Legends, DOTA, Call of Duty: Modern Warfare... also common in CS:GO (1 lane for each bomb site, and middle connector lane)

## Against typology?

Once you classify something, you're potentially trapping yourself within the limits of those classifications. Sometimes it may be more helpful to ignore typologies and refuse categorization.

## To review...

A typology is a way to classify different categories of level layouts. These words and labels help us talk and think about layout.

Room typologies are patterns for designing single areas, like corridors, switchbacks, ring-around-the-rosies / combat bowls, and arenas / POIs.

Level typologies are patterns arranging multiple rooms in sequence, like loopback, pass-through, branch and bottleneck, hub-and-spoke, and time cave.

## Further reading / sources
  * ["A Pattern Language"](https://en.wikipedia.org/wiki/A_Pattern_Language) (1977) by architect Christopher Alexander et al. is the classic typology manual of modern architecture and urban planning today, pioneering the New Urbanism movement.
  * ["On the ‘Three Typologies’"](https://medium.com/@tlukejones/on-the-three-typologies-ed0b5747fd9c) (2017) by architect Luke Jones is a wonderful essay about how architects still aren't quite sure how to classify architecture.
