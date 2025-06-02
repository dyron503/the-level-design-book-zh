# Composition

the overall visual arrangement and organization of shapes in a level; landmarks, vistas, approaches; also, why "leading lines" aren't real

## What is composition?

Composition is the overall visual organization of the level. There are two types of composition:
  * Spatial composition: the overall big picture 3D arrangement of core [masses](./). We cannot guarantee a specific view, and instead account for a wide variety of viewing angles and positions.
      * This is "composition" as practiced in 3D arts like architecture, interior design, and sculpture.
  * Shot composition: how the level looks in the player's 2D camera frame / screen, from a specific angle at a specific position.
      * This is "composition" as practiced in 2D arts like drawing, painting, photography, and film.

A lot of level design tutorials and resources out there claim that specific shot composition is really important. For many reasons, we disagree and we have a different definition of composition. Instead, we argue that spatial composition is much more important than shot composition.

(TODO: image)

## Spatial composition

Spatial organization involves building-up a spatial hierarchy, where some parts of the level should feel more important than the other parts. At the top of the hierarchy are key landmarks, focal points, and central areas that contrast meaningfully with their surroundings and anchor the rest of the composition. Some ways of building spatial contrast:
  * Height. Big tall towers in crowded spaces, or small short objects in open spaces.
  * Density / spread. A wider open space surrounded by smaller narrower structures.
  * Orientation. An angled object that breaks from the surrounding grid.
  * Shape. Lots of rectangular things nearby? Try putting a round thing there.

In the image above, notice how the central legislative chamber of the [Palace of Assembly, Chandigarh](https://en.wikipedia.org/wiki/Palace_of_Assembly,_Chandigarh) by Le Corbusier (bottom-left) uses several types of contrast in its floor plan. It's big, it's a circle in a box, and it's rotated at a skewed angle / axis that breaks from the rest of the grid. So it feels very important and vital to the function of this building! If this were a level, the main setpiece or final boss fight would probably take place in this round room.

The chamber is off-center and almost touches the eastern wall. But it doesn't feel off-center, does it? That's because focal points create new centers within the spatial organization. Imagine a zone of influence emanating from important area; it sort of "pulls" the rest of the composition around it. (See diagrams in bottom-right for how focal points influence how we perceive the "center" of a space.)

And remember, hierarchy depends on local contrast and context. A tall thing only seems special if it is surrounded by short things. A small thing will feel more special if surrounded by bigger things.

### Landmark

A landmark or point of interest (POI) is a unique and memorable shape, mass, or location in a level.

TODO: examples

TODO / IMPORTANT: landmarks have to feel relevant and useful !! otherwise they don't function as landmarks!

Actual landmarks (what the player notices during play) vs. fake set dressing landmarks (e.g. random skybox elements in The Last Of Us don't orient players, aren't actually useful)

### Saliency

### Sightlines

A sightline is a trajectory of empty open space that offers a possible view of another space.

Sightlines are tools that players use when it seems relevant to the current game state and goals. If the player has no reason to look along a sightline, then there is a high probability that they won't use the sightline at all. A sightline is an opportunity / situational tool that the player might ignore, it cannot guarantee behavior.

Even if the player looks in a certain direction, there is no guarantee they will remember or process what they saw. (Imagine reading a boring book or watching a boring movie; your eyes may see the words / images but that doesn't mean you actually read or process it.)

In the diagram above, level designer Sal Garozzo highlights common strategic sightlines on a 2015 version of the competitive multiplayer shooter map de_cache in Counter-Strike: Global Offensive, from [GDC 2015: Community Level Design for Competitive CS:GO (via YouTube)](https://www.youtube.com/watch?v=ocqmuBq4Ts4). Each sightline offers a different degree of coverage and information for attacking / defending the bombsite A area.

However, would all these sightlines be readily obvious to a first-time player, at first glance?

No. In fact, recognizing and memorizing these sightlines is part of learning the game / learning the map. Competitive players must actively study these sightlines; it is NOT a natural subconscious obvious way of looking around. The existence of a sightline does not mean the player will use it, nor even know it's there.

For more on sightlines in a multiplayer context, see [Balance](../../combat/balance.md).

### Vista

So how do we convince the player that, on first glance, the sightline is important?

A vista is an exceptionally deep scene composition that offers an overview of the next area, giving the player an opportunity to formulate a strategy. In modern encounter design, it is very common to introduce an arena with a vista beforehand, especially if the arena layout is complicated.

(TODO: talk more about vistas with examples that also emphasize the flow / layout into the vista)

### Approach

An approach is a path with a vista.

(TODO: show approach examples)

(TODO: example... Fallingwater?)

### Prospect-refuge

[Prospect-refuge theory](../prospect-refuge.md) is a widespread belief / design pattern in real world architecture which argues that humans navigate spaces by seeking prospect (vantage points) vs. refuge (safe areas), evoking their innate survival instincts.

We think prospect-refuge is bad theory (and bad science / bad art) with limited applications to level design. Instead we recommend using existing concepts and terminology with less philosophical baggage, like sightline vs. cover.

For more on why we think it's bad theory, see [Prospect-refuge](../prospect-refuge.md).

(TODO: include prospect refuge image)

## Shot composition (fallacy)

Shot composition is the 2D arrangement of level geometry relative to the player's camera perspective.

And ok, some of this matters, sometimes. Sightlines, approach, color and lighting, perspective -- all these aspects can matter, sometimes.

But some level designers misinterpret shot composition as level design. They argue that if you arrange everything in your level to make nicely framed views, then players will magically wordlessly know what to do and where to go.

Composition is not mind control. This is such a common misconception in level design theory that we're going to devote a whole section to debunking it. For this reason, we call this the shot composition fallacy: a belief that seems true and useful, but is actually deeply wrong, leading to a worse understanding.

### Screenshots aren't levels

First of all, a screenshot is not a level. This may seem obvious, but many level designers seem to have forgotten.

Instead, a screenshot is an image of the game at a specific position, angle, and time. Taking a screenshot is an act of photography.

Do photos capture an objective truth about a place or time? No. A photographer is an artist who chooses a place and time to create an image. Even a dev overview screenshot of a blockout emphasizes and downplays certain elements. A photo is an artistic interpretation that captures only one aspect of an actual person, place, or thing.

No photo can replace the experience of visiting a place or meeting a person, and no screenshot can replace a playtest.

More importantly, there is no guarantee the player will imagine the same framing or composition. The player never plays your screenshot.

For more on the decades-long debate about photography and meaning, see [On Photography](https://en.wikipedia.org/wiki/On_Photography) by Susan Sontag (about photos and US politics) or [Camera Lucida](https://en.wikipedia.org/wiki/Camera_Lucida_(book)) by Roland Barthes (about photos and death).

### Leading lines (are bullshit)

There's currently a trend in level design to analyze screenshots by drawing "leading lines" that seem to point / guide the player's eyes toward a landmark in the distance.

However we argue that leading lines aren't actually effective, and furthermore, leading lines don't even make sense within their own logic.

Leading lines routinely fail if you actually bother to playtest. You'll find that there is a 99% chance the player will look somewhere else, and a 1% chance they will look in the intended direction for 0.5 seconds. A screenshot is not a level, no one ever plays a screenshot.

Framing a view within a space is called photography, and it is a skill that humans practice and develop. It is not a natural subconscious process.

Leading lines misunderstand human [gaze tracking](https://en.wikipedia.org/wiki/Eye_tracking), perception, and information processing. Retina scans and tech show how leading lines and other traditional tenets of 2D visual composition don't "lead the eye" in the ways we think they do. Even if they did, there's no guarantee the player actually processed the visual information.

Shot composition makes more sense for photography, film, and other static flat 2D media where the author has strong control over the camera, and the audience can pay special attention to the entire image. However, it makes very little sense for interactive environments where the player can move the camera to the wrong place at the wrong time. A video game level is a place, not a painting, photo, or film.

Literally every hallway you build will seem to converge in the distance. This phenomenon is called foreshortening, creating an illusion of depth in an otherwise flat 2D image. Games with isometric or parallel projection make leading lines impossible. The [art history of perspective drawing](https://en.wikipedia.org/wiki/Perspective_(graphical)) is interesting, but it's not level design.

Ironically, leading lines mislead level designers into believing that shot composition, environment art, and set dressing are central level design problems instead of [metrics](../metrics/), [encounter design](../../combat/encounter.md), or [playtesting](../playtesting/). Even if leading lines worked (which they don't), you would do it near the end of the level design process. Focus on the fundamental foundation of the level first.

Leading lines are a [self-fulfilling prophecy](https://en.wikipedia.org/wiki/Self-fulfilling_prophecy) when you move the game camera into a specific place to frame a specific view. Of course the screenshot will follow rules of composition! That's because you composed it like that! And then you drew lines on it! This is photography, not level design. Consult the ["Golden Ratio" meme](https://knowyourmeme.com/memes/the-golden-ratio) about the absurdity of self-fulfilling composition patterns.

This isn't how people navigate spaces. People use pattern recognition, prior knowledge, and cultural associations to build mental maps in their mind. [Wayfinding](../wayfinding.md) is a complex active process of moving and using an environment, not just looking at one spot of a level from one angle.

### Sightlines vs. leading lines

It may seem like sightlines and leading lines are the same. They both relate to tracing what the player sees from their camera perspective.

However, sightlines and leading lines emphasize very different things:
  * Sightline: a trajectory of empty open space that offers a possible view of another space
      * A tool that players use when it seems relevant to the current game state and goals
      * Again, we want to emphasize:
          * Sightlines are made of empty open space
          * Sightlines are situational tools that do not guarantee behavior
  * Leading line: fake imagined phenomenon where walls and linear set dressing seems to converge in the distance to subliminally direct the player where to go
      * No one navigates spaces like this
      * No one plays video games like this
      * Don't make levels for no one

For much better ways of influencing / "guiding" the player, see [Wayfinding](../wayfinding.md).

## To review...
  * Spatial composition is the overall organization of 3D masses in the level.
      * Hierarchy is when some things seem more important than others, usually because they contrast in terms of size, shape, spread, or angle.
          * Landmark
          * Saliency
      * Sightlines are lines of empty space that the player can use to see into another area.
          * Vista
          * Approach
  * Shot composition is some kinda-bullshit theory that the player's view determines their behavior, rather than the player's actual understanding of the space.
      * Screenshots aren't levels; levels are spaces that players use
      * Leading lines are brain poison, don't use them
      * Don't confuse leading lines with sightlines, which are actually real

## Now what?
  * Apply this theory to the [blockout](../).
  * For more on "guiding the player" with architecture, see [Massing](./) and [Wayfinding](../wayfinding.md).

## Further reading

Our stance against leading lines / shot composition in level design is currently not the norm in the game industry. While we think it's 99% brain poison, other credible designers disagree:
  * ["Environment Design as Spatial Cinematography: Theory and Practice"](https://www.youtube.com/watch?v=L27Qb20AYmc) by Miriam Bellard, Rockstar North (GDC 2019) goes over Rockstar's approach to filmic environmental composition in Grand Theft Auto 5 levels. Bellard suggests a walkthrough method with rule-of-thirds overlay, and emphasizes affordance / salience model of embodied spaces. She also "myth-busts" leading lines and weenies while simultaneously arguing they are still useful. Overall, this is probably the most "balanced" industry talk on shot composition, but maybe just don't drink too much of the evo psych / [shape psychology kool-aid](../../../process/env-art/psychology.md).
  * ["The Importance of Nothing: Using Negative Space in Level Design"](https://www.youtube.com/watch?v=GZ99gAb4T0o) by Jim Brown, Epic Games (GDC 2014)
