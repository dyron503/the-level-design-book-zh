# Prospect-refuge

psychological / architecture theory about how people seek vantage and safety

Prospect-refuge theory is a widespread belief in architecture that humans have an "inborn desire" to seek out prospect (vantage points / lookouts) and refuge (enclosures safe from threats / view).

This book argues that prospect-refuge, as traditionally understood, has limited application to level design. Risk / safety / information in video games often differs greatly from real world architectural assumptions. (And frankly, we're also skeptical whether it's useful for real world architecture.)

At the end of this page, we suggest an alternative application of prospect-refuge theory, using already existing terms and concepts in level design.

(TODO: prospect refuge illustration with big red Xs)

## History

In his 1975 book The Experience of Landscape, geographer Jay Appleton combined psychologist Daniel Berlyne's "arousal theory" with early evolutionary psychology to form his prospect-refuge theory. It's worth tracing how this happened.

In the 1950s and 1960s, Berlyne experimented with lab rats and curiosity. He argued that when a lab rat (or a human) sees a new space, they feel "aroused" as they process the unfamiliar environment.

Note that Berlyne does not mean sexual arousal, but instead something more like engagement -- a general state of increased energy expenditure and mental responsiveness. That is, a more complex and novel environment stimulates more arousal / engagement.

However, too much complexity and novelty is negative. In his 1960 book Conflict, Arousal and Curiosity, Berlyne cautions that too much of this environmental arousal can lead to anxiety and uncertainty. When graphed below, it is a "U-shaped" effect:

The basic premise of evolutionary psychology is that humans are just like any other animal with survival instinct. Appleton reasoned that Berlyne's environmental arousal also aided human evolutionary fitness. Increased mental responsiveness would've been useful for a caveman / early human to parse threats and find safe places from predators.

Outside of psychology, no really cared about this until 1988, when architectural historian Grant Hildebrand popularized Appleton's prospect-refuge. Hildebrand wanted to strengthen modernist architecture's claims to universal design and function, and so psychology was an effective way to argue why architect Frank Lloyd Wright's buildings supposedly had intrinsic psychological appeal -- culminating in his 1999 book Origins of Architectural Pleasure. (Maybe these men were indeed alluding to sexual arousal.)

## Criticism

There are several ways to critique prospect-refuge theory, including its science and philosophy:
  * Berlyne's behaviorism and psychology of aesthetics
	* does studying lab rats' aesthetics actually teach us anything about human aesthetics?
	* can art and aesthetics be studied in this way at all?
	* The field of psychology is currently in a [replication crisis](https://en.wikipedia.org/wiki/Replication_crisis), where famous experiments and theories cannot be validated or reproduced
	* can we replicate the U-shape curve? (maybe not)
  * Appleton's addition of evolutionary psychology
	* [widespread criticism of evolutionary psychology](https://en.wikipedia.org/wiki/Criticism_of_evolutionary_psychology)
	* even if evo psych is real, is it relevant to video games?
  * can we replicate prospect-refuge effect? ([2021 study:](https://onlinelibrary.wiley.com/doi/abs/10.1002/mar.21449) prospect is real, but refuge is not)
	* ([2016 meta-analysis of 34 other studies](https://medium.com/@social_archi/prospect-refuge-theory-ca5d80379e51))

At first glance, prospect-refuge theory seems very applicable to games. It is about survival and safety, like many 3D action games. But for the many reasons listed above, we think it is better not to rely on it.

## How to use prospect-refuge in level design: maybe don't.

We argue that these same ideas are more useful if we utilize already existing terms and concepts in level design instead. These industry-specific terms have less philosophical baggage and offer more technical specificity, especially for combat games.
  * Instead of prospect, use sightline / vista.
  * Instead of refuge, use cover / enclosure / base / safe house.

### Instead of prospect...

A sightline is a line of empty space where one area can be seen from another area.

A vista is a vantage point with access to many distant sightlines. It is most useful in single player level design to convey progression beats, preview landmarks, and offer layout information -- especially for an arena layout before an encounter begins.

(TODO: link to specialized sightline and vista pages)

### Instead of refuge...

The problem with the word "refuge" is that it implies safety. But the video games, the player's sense of safety is complicated, and extends far beyond the level design.

For many action games, threat assessment is a core mechanic / skill that players must develop over time, dependent on the overall combat design.

Survival and death systems also vary greatly between games: some may reward players for death, or even penalize survival.

#### Safety as game state

A dozen hours into the action RPG Elden Ring (2022), the player enters a "debate parlor" in a magical castle. When most players reach this point, it will feel very dangerous.
  * In Elden Ring, the most difficult boss enemies tend to inhabit highly decorated landmark areas. So the unique art assets here differentiate the room from past rooms, it stands out as a special area of high importance.
  * The player has reached this point after fighting through 3-5 encounters, and is probably wondering where the next save point is. Past boss arenas featured convenient save points before the fight; this one does not, and pushes players to risk their progress.

(screenshot: debate parlor entry)

Suddenly, a giant glowing wizard wolf begins growling at the player.
  * The wolf has a name and a large health bar, indicating it is a dangerous boss enemy.
  * The medium-sized room makes the large wolf feel even larger. It will be difficult to dodge the wolf's attacks.
  * Furniture and clutter further limit the player's mobility and options. (Until the boss destroys the furniture, opening up more floor space, making the fight a bit easier.)
  * Epic dramatic music begins playing.

(screenshot: battle begins proper)

Note all the factors that make the situation feel dangerous: the UI, consistent use of environment art, the past encounters and progression system, even the music.

After defeating the boss, only a quiet "grace" campfire-like save point remains. This landmark boss arena now functions as a safe house, territory won by the player after a difficult battle. The chaotic half-demolished parliament chamber now takes on the mood of a peaceful ruin.

This is the same room, but it undergoes three different state changes before, during, and after the encounter.
  * sense of safety depends less on layout / blockout / architecture, and instead more on the wider game systems / encounter design patterns
  * game worlds change ownership and function much more frequently than in the real world
  * something won't "look safe" if past levels featured traps or ambushes

Thus, "refuge" is a situation / game state, not a formal quality of architecture. No shape or layout is intrinsically safe.

#### Enclosure

So what word should we use instead of refuge?

We propose enclosure: the degree that an area is surrounded by cover.

Cover is any object that blocks a sightline and/or combat.

TODO: base / safe house

there is
