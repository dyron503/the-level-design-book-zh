# Lighting

How to light a game level with functional lighting strategies

Lighting design is about placing lights in the game world to create visual depth, evoke mood, and provide information to help players play. Poorly lit spaces often feel stale, flat, unfinished, or confusing.

Since lighting is so important for readability, we recommend a lighting pass during / soon after establishing core gameplay in [blockout](../blockout/) or [scripting](../scripting/) phase.

The industry usually categorizes lighting as an aspect of [environment art](../env-art/), but here we will focus less on graphics and more on the design and function of lighting. What do lights say and do?

In the study above by Harley Wilson, lights tell us a lot about the game world and help us play:
  * [Worldbuilding](../../preproduction/worldbuilding.md). Recessed down-lights along a wall suggest a fancy modern gallery.
  * [Massing](../../blockout/massing/). Cooler grays wash a gallery wall, warmer lamps highlight counters, dim down-lights mark a shadowy corner. Lights divide this area into three sub-areas.
  * [Circulation](../../layout/flow/circulation.md). The far wall is dark, maybe it leads to a backdoor or a closet. It's probably not a primary exit, which would be lit more prominently.

## What is video game lighting?

In real-life, light is visible energy that interacts with surfaces. It is an elegant system; with the core physics of energy and photons, you can derive all other complex light effects.

In contrast, video game lighting is NOT elegant. It's a fake-as-hell fucking mess, secretly made of many different subsystems in a game engine:
  * Light sources: base layer of direct illumination, based on light angle and position
  * Shadows: objects occlude (block) light and project shadow maps onto other objects
  * Materials: the color, texture, opacity, and reflectivity of 3D surfaces
  * Postprocess: screenspace effects like color correction, bloom, and HDR eye adaptation
  * Reflections: true reflectivity requires re-rendering the scene; most games use approximations
  * Baking: developers pre-render lightmaps and reflection data

Imagine making a rainbow with a prism. In real-life, you shine a ray of light through a prism and a rainbow "automatically" emerges because that's how photons and physics work.

But in a video game, a prism effect would be a mess of hacks:
  * Refracting glass material + screen space reflection for prism shape
  * Ray FX, white beam and rainbow painted separately in Photoshop
  * Glow sprites where beams intersect prism
  * Caustic projections / translucent AO for nearby surfaces

This is not an elegant universe of photons interacting with surfaces. In the list above, notice that we're not even using any light sources! It's all "fake"!

It's enough to make a real-life physicist vomit. "But light without shadows or reflectivity doesn't make any sense," cry the physicists. Haha, silly physicists! This is video game land!

Graphics programmers are secretly bothered as much as physicists. Tech like raytracing is about trying to make game lighting more elegant. Maybe in 10 years it will be.

## A brief history of light

The sun and the moon (reflecting light from the sun) are the most common natural light sources.

There are also artificial light sources like controlled fires, gas lamps, incandescent light bulbs... and in the 21st century, there's energy-efficient fluorescent lights and LED lighting.

However, this is not just a story of technology and progress. The light bulb did not make the sun obsolete, and the LED does not make fire obsolete. We still like sunny days and romantic candle-lit dinners.

Fire has not disappeared from the world. Instead, the meaning and use of fire has changed. Lighting design is about understanding how light conveys these ideas, moods, and emotions.

## What is lighting design?

Real-life lighting design is the art / science of placing light sources to account for context and functionality, whether for an office or a moody restaurant.

Real-life professional lighting designers assess building plans and coordinate with architects. They shop in catalogs published by light fixture manufacturers, with detailed technical specifications and lab-tested light falloff charts / standardized IES profiles that they can test in 3D simulations. They must also balance local laws and building codes about minimum light levels, budget, maintenance plans, energy use, and sustainability.

Some game engines are increasingly adopting this technical / scientific lighting approach. However, we must be vigilant: real-life lighting design has fundamentally different goals vs. video game lighting design.

REAL-LIFE LIGHTING | GAME LIGHTING
-- | --
Runs on electricity | Also runs on electricity
Must obey laws of physics | Pick and choose laws; godless
Follow local regulations | No regulations, only gamer norms
Infinite light sources, infinite rendering | Optimize for fewest light sources
Long-term, you live in it | Short-term, you visit it
Glare is literally painful to look at | Glare makes your game worth $60
Comfort, safety, usability, reliability | Drama, detail, clarity, plausibility

## Light sources

Since game lighting is so complicated, we will mostly focus on the fundamentals of lighting design for level designers: placing light sources.
  * Core light source types
  * Static vs. dynamic light sources
  * Fixture vs. light source

### Core light source types

Almost every game engine uses these four core light source types:
  * Ambient light is the default minimum amount of light in the world. Not really realistic.
  * Directional light casts constant light from a direction, like sunlight downwards from the sky.
  * Point lights (omnidirectional / "omni" light) are like light bulbs, throws light in all directions.
  * Spotlights cast a cone of light in a certain direction from a certain position.

(TODO: light source diagram)

Together, these light sources form a complete domain of basic lighting tools:

Global, affects everything | Local, affects nearby things
-- | --
Shines in all directions | Ambient light | Point light
Shines in one direction | Directional light | Spotlight

Other light shapes are just variations on these core types.
  * Area lights are wide flat rectangular spotlights
  * Tube lights are long point lights
  * Emissive materials / "texture lighting" use self-illuminated pixels like point lights

### Static vs dynamic

A static light does not change at all, while a dynamic light can change in color, intensity, direction, or position.

Static lighting is almost always better for framerate because the engine can "bake" lighting data like lightmaps and reflections -- but rebaking constantly gets annoying, and lighting data can consume a lot of memory.

In contrast, dynamic light means the level can change and react, enabling switchable moving lights and day-night cycles -- but if there's too many light sources, then it might overload the player's machine and the framerate will suffer.

### Fixture vs light source

A light fixture is a visible plausible source of light, like a light bulb or a fireplace. But a window with sunlight is also like a fixture. Within a game level, this is usually like an architectural feature or a decorative lamp prop.

This is not the same as an in-engine light source, which is actually an invisible source of light with no apparent cause. It often looks kind of weird, and simply doesn't happen in real-life.

A motivated light is a light source with a plausible fixture.

Note that a single fixture may actually motivate multiple invisible in-engine light sources. In the image pictured below by Harley Wilson, there are only two visible light fixtures: an orange fireplace and a blue-gray window. But what looks like two lights is actually 11+ light sources!

## Lighting theory

Here are two ways of approaching lighting design:
  * Three point lighting: common theory for 2D media like film and photography
  * D6 lighting: more abstract but more 3D, for architects and interior designers

### Three point lighting

Three point lighting is a lighting theory with three types of lights:
  * Key light: the primary light source
  * Fill light: softer secondary light source to brighten up shadows
  * Rim light: an accent to highlight objects and edges

While these core concepts are useful, it has limitations for level design. This technique comes from photography and film, so it assumes linear fixed 2D screen compositions -- not an interactive 3D space that a viewer navigates freely.

For more about this 2D lighting theory, see [Three point lighting](./three-point.md).

### D6 lighting

D6 lighting is a lighting theory focused on coverage and space, inspired by a six sided die. Each side represents a lighting strategy, for a total of six strategies:
  1. Focal point ⚀
  2. Focal frame ⚁
  3. Path ⚂
  4. Area ⚃
  5. Area with focal point ⚄
  6. Area with path ⚅

This theory has more applications for architecture and level design, however it's obscure and less known than three point theory.

For more about this 3D lighting theory, see [D6 lighting](./d6-lighting.md).

## How to light a level

Lighting can be very time-consuming, so don't attempt to do final lighting all at once. Instead, build flexibility into your workflow, and work iteratively.

We recommend lighting in four passes:
  * Global lights
  * Wayfinding / critical path lights
  * Gameplay / combat encounter lights
  * Detail and mood lighting

### 1. Global lights

Begin with an initial pass at any global key lights and fill lights: skylight, ambient light, and any skybox / atmospherics.

If you are using any emissive materials as key lights, e.g. a glowing river of lava, then configure this light source as well.

If your desired look involves baked indirect light, run an initial low quality light bake immediately. Some fancy global illumination solutions (e.g. UE5 Lumen) may be able to light the entire game world with just one sunlight-like directional light.

### 2. Wayfinding / critical path lights

Next, ensure any important entrances / exits along the [critical path](../../layout/criticalpath.md) are well-lit from the desired approach. You will likely need to use local light sources, e.g. place a light fixture next to a doorway.

Build a hierarchy. Big important exits should have more important looking lighting, while secondary spaces should have dimmer less focused lights.

### 3. Gameplay lights

Lighting to foreshadow encounters (enemy approach, battle line, possible strategies and flanks)

Lighting to highlight puzzle elements and suggest areas to explore

### 4. Detail and mood lighting

Fine tune and tweak everything, but don't spend too long, it probably looks good enough, and if you tweak it too much you might destroy the effect from a previous pass.

(TODO: images and examples?)

## Common lighting design problems

### Shadows are too dark after a light bake?
Your albedo textures might be too dark. If the textures are too dark, then any resulting light bounces will be faint, no matter how bright your lights are. Unless you have specific stylistic or technical reasons to do otherwise, your main diffuse textures should usually be in the 50-100% brightness range. See ["Texturing Values for Environments"](https://environmentart.wordpress.com/2016/06/13/texturing-values-for-environments-part-1/) by Rogelio Olguin, and the old Epic Games UDK docs ["Epic Games Texturing Guidelines"](https://docs.unrealengine.com/udk/Three/TexturingGuidelines.html).

## Lighting examples

TODO: showcase different contexts (industrial vs residential) and moods (scary, comfy)

### Lighting example: Ratchet and Clank - Rift Apart

## To review...

Lighting gives visual depth to a scene, allowing players to gauge distances and distinguish shapes. Because it serves a very important gameplay function, you should do a lighting pass early in the level design process, before a proper art pass.

Video game lighting tech is a crude illusion that approximates real-life light. Many game lighting effects do not actually use any lighting systems.

There are 4 core light source types: ambient, directional, point, and spotlight. These lights can be static or dynamic, and motivated by a visible light fixture or unmotivated without any visible source.

The most common lighting theory is three point lighting, which defines key lights, fill lights, and rim lights based on the light's orientation to the camera and subject.

To light a level, work gradually over several lighting passes. Do global lights first, then light for wayfinding, and then for gameplay, and finally any last details or moods.

## Now what?
  * Move on to [Environment Art](../env-art/).
  * Lighting is traditionally the most performance-heavy visual aspect of a level. After a lighting pass, you'll want to do an [optimization](../env-art/optimization.md) pass.

## Further reading on lighting

### Game lighting
  * ["Functional Lighting"](http://magnarj.net/article_funclight.html) by Magnar Jenssen is about lighting levels to aid readability for typical shooter gameplay.
  * ["Gamma and Linear Space"](https://www.kinematicsoup.com/news/2016/6/15/gamma-and-linear-space-what-they-are-how-they-differ) by Kinematic Soup covers an important but often neglected aspect of game graphics: color space and gamma curves.
  * [GDC 2022: Recalibrating Our Limits: Lighting on 'Ratchet and Clank: Rift Apart' by Anna Roan and Brian Mullen (via YouTube)](https://www.youtube.com/watch?v=geErfczxwjc) is a great overview of how many AAA lighting artists work today, with lots of process and iteration examples.

### General CG lighting
  * [Blender Conference 2022: The Secrets of Photorealism by Andrew Price (via YouTube)](https://www.youtube.com/watch?v=Z8AAX-ENWvQ) is a video intro to lighting 3D scenes for photorealistic look. Color temperature, falloff, materials, and optics / post process.

### Real world lighting design
  * The Architecture of Natural Light, by Henry Plummer. Monacelli Press: 2009.
  * [IESNA Lighting Handbook](https://openlibrary.org/books/OL58383M/The_IESNA_lighting_handbook), 9th edition (2000). edited by Mark S. Rea.
