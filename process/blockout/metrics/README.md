# Metrics

The proportions and distances of the level, how big the level feels

## What are metrics?

In level design, metrics are the sense of scale, distance, and measurements across the entire level / game.

All level designers use at least two types of core metrics:
  * Player metrics (or physics metrics) are factual numbers measured in-engine like player size, movement speed, maximum jump height, etc.
      * describes game physics, derived from the game engine
      * example: "player size" is a specific fact that can be measured and verified
  * Building metrics are suggested floor / wall dimensions and guidelines that you codify for yourself based on your desired [experience goal](../../preproduction/#experience-goal)
      * prescribes game feel, decided by designer(s)
      * example: "regular hallway size" is a guideline; what does "regular" mean for each project?

Depending on the project, you might need combat metrics or puzzle metrics too.

But beware of over-reliance on metrics. Numbers and measurements may give the illusion of infallible design laws -- the illusion that following these numbers will give you the perfect level. You must reject this illusion! You cannot measure your way to a good game experience. Metrics are a helpful design tool to help you make decisions, but metrics are not magic.

Note that "metric" is also a generic word for "measurement", it's not just a level design word. Across the game industry, we also have mobile game metrics ("KPI"), audience metrics, marketing metrics, monetization metrics... anything that can be measured.

## Scale

Metrics help you establish scale, the general sense of how big the game world feels.

In level design we usually follow real world architecture built at a [human scale](https://en.wikipedia.org/wiki/Human_scale). That means making sure rooms don't feel too small or too big for people. Proper scaling is very important when working in a realistic style, because it makes the level feel more plausible -- it will feel more like a real place built by humans and inhabited by humans.

But imagine a game about being a cat, it would need some rooms that feel too big (because cats are smaller than humans.) Or imagine a car game -- it would need houses that feel too small (because cars are bigger than humans).

For games we "build at the player's scale", which may or may not be a human scale.

### Video game scale is weird

The human scale is helpful, but video game spaces are not human. Video games often rely on an exaggerated sense of scale that does not correspond to any consistent real world measure.

In The Elder Scrolls: Skyrim, the world area is about 14 square miles, the tallest mountain is 766.5 meters above sea level, and the player runs (not sprints) at 11.7 mph without tiring. That means the entire "province" of Skyrim is half the size of Manhattan, the tallest mountain is shorter than the Burj Khalifa in Dubai, and every peasant is a high performance marathon runner. By any real world measure, it is very small and weird. And yet, Skyrim somehow still feels like a large vast natural landscape with a huge alpine mountain, populated by typical people of average fitness.

So when building video game spaces, remember that it should merely "feel" realistic as part of the mood, atmosphere, or aesthetic.

But if you approach level design too much like real world architecture, then ironically, your levels will feel too big, complicated, and implausible.

Don't follow real world scale.

### Scale advice
  * "Big" levels feel big, but are actually much smaller than in the real world.
  * Players regularly move at very fast speeds... that feel normal in the game world.
  * The game world feels internally consistent, even if the specific numbers seem silly to think about.

Unfortunately it's not scientific. You'll only know "it feels right" when you're walking around inside your level and playtesting.

That's why we recommend considering metrics at the [blockout](../) phase. You can't really test metrics with a paper layout, but if you wait too late (like after an art pass) then it will be very time-consuming to make big changes. You might even have to redesign the entire level.

## Basic metrics

In theory, you can build your game or level at whatever scale you want. In practice, physics implementations assume a default scale, and asset stores supply environment art at a common humanoid scale. Following convention is... convenient.

For your convenience we provide common metrics for popular game engines below, but we encourage you to check out our full list of [Tools](../../../appendix/tools.md).

### Common player sizes
Game / Engine | Default units | Bounding box (width, height) | Eye height
-- | -- | -- | --
Unity | Meters | 1.0 x 1.8 m (or 1.0 x 2.0 m) | 1.5 m - 1.7 m
Unreal | Centimeters | 60 x 176 cm (half-height: 88) | 152 cm (88+64)
Quake / Half-Life / Source Engine | Inches?* | 32 x 72 in | 64 in
(US, real-life) | Inches | 20 x 69 in (average adult) | 66 in
  * Bounding box / collision sizes are usually much bigger than the actual character model. This bigger thicker size is for more stable movement. It's not a hitbox.
  * Note that in-game eye height is usually below where actual eyes would be. Many FPS games put your eyes in your neck or chest. For more detail, see [Metrics of perception - Camera height](#camera-height).
  * * Quake, Half-Life, Source Engine / "Quake lineage" games use "inches" lightly (eg. [in Team Fortress 2, everyone is 7 feet tall](https://developer.valvesoftware.com/wiki/TF2/Team_Fortress_2_Mapper's_Reference)) and don't really make sense.

### Common modern architecture dimensions
Game / Engine | Interior walls (depth, height) | Minimum hall width | Doors (width, height) | Steps (height, depth)
-- | -- | -- | -- | --
Unity | 0.1 x 3.0 m | 2.0 m | 1.25 x 2.5 m | 0.1 x 0.15m
Unreal | 20 x 300 cm | 150 cm | 110 x 220 cm | 15 x 25 cm
Quake / Half-Life / Source Engine | 16 x 128 in | 64 in | 56 x 112 in | 8 x 12 in
(US, real-life) | 6 x 96 in | 48 in | 36 x 80 in | 7 x 11 in ("7-11")
  * The minimum hallway width should be at least double the player width. Even then, it will feel a bit narrow and uncomfortable.
  * Modern doors should be narrower than hallways to allow space for a door frame.
  * Modern flights of stairs have landings / platforms every 12-16 steps. Long or tall stairs will feel industrial, monumental, or otherwise non-domestic.
  * Modern stairs should follow a 30-35 degree slope. arctan(7/11) = 32 degrees
  * In Source 1 and older engines, level grids followed power-of-two numbers. Unity users often prefer 1.0's and 10's. Unreal users are split based on their age. Use whatever number roundings that you and your collaborators prefer.
  * When building in a realistic modern style, do some [research](../../preproduction/research.md) beforehand: gather plans, blueprints, schematics, or even read through local building codes.

### Deviating from conventional metrics

Deviate meaningfully from typical metrics, proportions, and spaces.

Steep stairs will feel more harrowing and awkward than shallow stairs, and if that's the [experience goals](../../preproduction/#experience-goals) you want, then go for it. Often the best part of a level is the uncommon and unexpected. But to make something feel unusual, you must contrast it with enough usual common elements first.

#### What if the level is stylized / isn't realistic?

Even with stylized non-realistic art styles, metrics still need to feel internally consistent to the game world / design norms. For example, the steps in Quake 1 maps are often 16 inches tall, but the rest of the game world is appropriately big and chunky to match that proportion.

#### What if the level isn't modern?

Do [research](../../preproduction/research.md) on the type of architecture you're using. For example, traditional Japanese architecture uses the [ken (間)](https://art-design-glossary.musabi.ac.jp/ken/) proportional system. Italian Renaissance architects used the golden ratio (1 : 1.618) in the vein of Ancient Greek and Roman architecture, etc.

## How to use metrics

Some ways to bring metrics into your level design process:
  * Build a metrics zoo test map
	  * Prototype core player metrics
	  * Use world-aligned grid textures
	  * Test modular kit
  * Metrics debug tools, editor previews
  * Codify shared building metrics

For more information on planning, see [Pre-production](../../preproduction/) and [Research](../../preproduction/research.md).

### Build a metrics zoo test map
Build a "metrics zoo" / "metrics playground" developer-only test map that exhibits the different gameplay objects, modules, and prefabs across all your levels.
  1. [Blockout](../). Make a simple level with various rooms, hallways, and floor heights.
  2. Playtest for usability. Walk around with gravity, jump on objects, be a general nuisance.
  3. Playtest for feel. Pay special attention to the sizes of walls, doors, and floors. Does the height of the stair steps feel right? Do doors feel too narrow or too short?
  4. [Iterate](../playtesting/#iteration). After each metrics revision, playtest and walk through again. Repeat.

Some example core player physics metrics
  * Basic movement
	  * Walk speed, run speed
	  * Maximum step height, maximum angle slope incline
	  * Minimum hallway width, minimum ceiling height
  * Jump, fall, drop, height
	  * Maximum jump height, maximum jump distance, running jump distance
	  * Gravity strength, fall speed
	  * Fall damage height threshold for 1% damage vs 100% damage lethal fall

#### Use world-aligned grid textures

When blocking out, use some kind of world texture with a little surface detail.
  * Do not use flat solid colors, these lose visual scale and depth cues while prototyping.
  * Do not use detailed textures, these are visually busy, can distort scale, and are distracting.

We recommend using placeholder grid / checkerboard textures, anything with repeating lines at regular intervals that will help you eyeball distances and proportions as you build your blockout. Check our [Resources](../../../appendix/resources/) for links to various prototyping texture packs.

While building, make sure the texture scale stays constant and independent of the 3D object scale.

To ensure a constant scale in your game engine:
  * Quake / Half-Life / Source: make sure your level editor's "texture lock" is disabled, and set all brush faces to use world axis alignment. For [TrenchBroom](../../../appendix/tools/trenchbroom.md), see ["TrenchBroom Manual: Working With Textures"](https://trenchbroom.github.io/manual/latest/#working_with_textures).
  * Any modern game engine: configure the shader or material to use a triplanar projection with a tilting grid texture. This has the added benefit of automating UV unwraps across all objects, so you can focus more on geometry rather than texture alignment.
	  * Unity: visual shader editor has a built-in [Triplanar Node](https://docs.unity3d.com/Packages/com.unity.shadergraph@17.0/manual/Triplanar-Node.html), or to go deep on coding your own shader see [Ben Golus' post "Normal Mapping for a Triplanar Shader"](https://bgolus.medium.com/normal-mapping-for-a-triplanar-shader-10bf39dca05a)
	  * Unreal: material editor has a built-in [WorldAlignedTexture Node](https://docs.unrealengine.com/4.27/en-US/RenderingAndGraphics/Materials/Functions/Reference/Texturing/#worldalignedtexture), or to go deep into coding your own shader see [Ryan DowlingSoka's post "Triplanar, Dithered Triplanar, and Biplanar Mapping in Unreal"](https://ryandowlingsoka.com/unreal/triplanar-dither-biplanar/)

#### Test modular kit metrics

With a modular kit, you build a level with pre-made tiles and components that snap together.

What's the best size for a doorway? You don't have to worry anymore; that metric is baked into the doorway module. In modular construction, you measure once, and basically copy-and-paste that measurement across the entire level.

However, it is common to iterate on a modular kit on the fly -- adjusting tile sizes and measurements, refining and art passing modules later, etc. If you make big changes to the modular kit's design assumptions, such as tile grid size or granularity, then you will likely have to rebuild everything because the new kit won't work for levels that used the old kit.

The best way to test the metrics and scale of a modular kit is to use it! Blockout with it, try to build hallways that loop back on themselves, then playtest and walk around in it.

For about modular construction, see [Modular kit design](./modular.md).

### Metrics debug tools and guides

For action games with a heavy focus on player movement and platforming, it can be difficult to predict whether a wall is too high to jump, or a gap too wide, etc. An in-editor metrics measurement tool / visualization / trajectory preview can help resolve these ambiguities.

For Psychonauts 2, developers implemented a "jump preview" editor visualization so that level designers could easily predict a player's jump arc:
> "The jump metrics tool is designed to be placed into the level when the game is not running to visualize Raz’s jump arc. This can be used to help place objects along an action path so they’ll be reachable by the intended jump type. The tool runs the jump simulation code at edit time, while the game is not running. Any changes to the jump tuning would be reflected by the preview arc."
> -- Devin Kelly-Sneed, ["Behind the Code: Designing Raz's Jump"](https://www.doublefine.com/news/devin-article-raz-jump)

### Codify shared building metrics

Beyond player metrics like maximum movement speed or jump height, you can also set recommended building metrics for yourself as a guideline -- and these shared guidelines across a design team can help make construction and collaboration easier. Some examples:
  * [Combat metrics](#combat-metrics): What is "close range" or "long range"? How big is a "big fight"? How tall is [cover](../../combat/cover.md), how high should a window be?
  * [Pacing metrics](../../preproduction/pacing.md): How long should each map or chapter be altogether? How far should the exit be, how much backtracking should be allowed?
  * [Storytelling metrics](../../env-art/storytelling.md): How long is this NPC dialogue, and how far can the player travel while they are talking? How many narrative assets such as audio logs, readables, codex collectibles, etc. should be placed in a given part of the level?
  * [Optimization metrics](../../env-art/optimization.md): If we are streaming in chunks of level data, how big should each chunk be? How long does the level transition hallway or sequence need to be, to mask the level streaming time? How many different meshes, materials, or shaders, can we load for each level?

Some example combat metrics for Team Fortress 2, based on [observation and analysis from the TF2maps community](https://tf2maps.net/threads/guide-scale-and-your-map.12605/):
  * Close range weapons: 256 units or less
  * Medium range weapons: 1024 or less (and projectiles become easier to dodge, etc)
  * Rocket spam and snipers: 2048
  * Maximum drop height without fall damage: 256

These metrics are reflected in the arena design of Team Fortress 2 maps like Badwater Basin below. Most drops are 256 units high, with maybe a few drops at 320 to apply a small penalty for any falling players. However there aren't many 512 unit drops because that would limit player options too harshly, and also render close range weapons much less effective.

## Metrics of perception

What affects the player's perception of size and speed? Basically anything on the screen.

### Camera height
If you are prototyping a game, finalize the camera height / eye offset as soon as possible, because it will affect how big the entire game world and all its characters feel. The camera height is one of the key variables that affect the player's sense of a virtual body, because "slow" and "fast" are relative to body size.
> "Some animals are lightning fast. Others are pitifully slow. But slow and fast are relative terms. Four miles per hour doesn't feel very fast to a human: it's approximately one body-length per second. But to a small insect it's approximately 100 body-lengths per second. A human traveling that fast would be going 20,000 miles per hour! This is why some animals' brains process visual stimuli much faster than ours, and why they have better reflexes (think about how hard it is to swat a fly). What does it feel like to comprehend the world at such speeds?"
> -- Alex Reisner, creator of [SpeedOfAnimals.com](https://www.speedofanimals.com/)

For suggested eye heights, see the [Basic metrics](#basic-metrics) section above.

### Local reference points, composition, texturing, fog
TODO: more local context, objects along the line of movement

### Camera field of view (FOV)
Your sense of perceived speed depends on how much you are seeing and the rate of visual change within your vision. A high [field of view](https://en.wikipedia.org/wiki/Field_of_view_in_video_games) (FOV) will zoom-out to produce fisheye distortion that increases apparent speeds at the edge of the screen (periphery).

Note that there are three ways to measure field of view -- horizontal, vertical, and diagonal -- but for games we generally refer to the horizontal FOV so that it scales well with widescreen setups.

Some players prefer high FOVs because they can see more of the world around them and gain better situational awareness, and there have also been studies that suggest a high FOV helps some players mitigate motion sickness while playing first person games.

The default Quake (1996) field of view was 90 degrees, and competitive players often set their camera to 120 degrees so that they could see more of their surroundings. This made more sense when CRT monitors and TVs had a 4:3 aspect ratio, but feels different on a modern 16:9 widescreen display.

Today, most commercial 3D action games tend to offer accessibility settings with an FOV range slider for users to adjust the camera to their personal comfort, usually between 60 and 90 degrees, but default to a narrower FOV. A high FOV distorts the image in an unrealistic / unflattering way. Meanwhile, a lower FOV zooms-in and "flattens" the view depth, giving a greater sense of closeness and intimacy with the game world. If your game is about looking up-close at characters' faces, you would err on a narrower FOV so that the faces don't look strange or distant.

Portrait photographers often try different lens focal lengths to get the most flattering distortion and closeness with their subject. 20 mm (84° FOV) narrows the face with extreme proximity, 70-100 mm (29-20° FOV) is more naturalistic, and a long 200 mm (10° FOV) telephoto lens widens and flattens the face with a longer distance from the subject.

On top of the base FOV setting, many third person action games shift to a higher FOV when the player sprints or accelerates. This FOV change gives a greater sensation of speed, even if the actual speed increase is negligible. In contrast, some virtual reality games purposely occlude and mask peripheral vision to decrease this sense of acceleration and mitigate [VR sickness](https://en.wikipedia.org/wiki/Virtual_reality_sickness).

### Sound design, HUD / UI, and NPC AI as speed metrics
The brain processes all senses together. Vision isn't just a matter of seeing, it is also a matter of sound, memory, knowledge, etc.

To demonstrate, there is [a well-known experiment in game feel](https://youtu.be/Fy0aCDmgnxg?t=464) involving two identical circles sliding past each other to swap places. Without any sound, the circles will appear to be just exchanging positions, but if you play a collision sound when the circles intersect, then the circles will appear to collide and bounce off each other instead.

For a more direct example of how other stimuli affect our sense of speed, consider the ZX Spectrum port of Super Hang-On (1987). In this single player motorcycle racing game, the "turbo" button temporarily increases the player's max speed limit to 324 km/h, beyond the normal limit of 280 km/h. However, the game does not render faster nor does the player actually move faster; instead, the engine sound gets louder, numbers get bigger, and opponent NPCs slow down. These contextual cues combine to give a faster feel without actually adjusting the camera nor the player.

## The church of metrics: "rational game design"

A game industry practice known as rational game design (RGD) / rational level design (RLD) focuses on measuring metrics to plot parameterized game mechanics against game difficulty in a coordinate space, with the goal of mapping out a game's possibility space in a quantified way.

Basically, give everything in the game a number, and then add up all the numbers to help guide your design decisions. If you don't like how the numbers add up, change them. This general workflow looks like:
  1. Design game mechanics, and identify various parameters and modifiers.
  2. Plan levels across the entire game with different combinations of mechanics and modifiers.
  3. Quantify parameters for each mechanic (e.g. 0% difficulty jump is a 3 m wide gap between platforms, while a 100% difficulty jump is 10 m wide, etc.)
  4. Iterate on each level's metrics to conform to desired difficulty scores and target values.

### Criticism of rational game design

Supporters claim this design method represents a more "rational" and "scientific" approach to plotting and pacing the player experience. Unfortunately there are very few public resources on how to practice RGD, which is convenient because that means we can't actually evaluate its methodology or claims -- its evangelists can always claim that we haven't read the proper holy scriptures, and so we don't truly understand how to practice it. What little documentation here is cobbled together from the few articles and resources available online, with much of the material guarded as a trade secret by Ubisoft.

We caution against any uncritical belief in any single design method, especially something that touts supposed objectivity / ahistorical understandings of "form follows function." And we remain skeptical of any method that claims to capture conceptual depth with a number. The more technical the design formula, the more formulaic the design will be -- a common critique leveled at many Ubisoft games.

But if RGD / RLD serves as a useful design tool that yields good results for the type of game you're making, then there's no harm in using it with moderation. Collecting data, measuring spaces and distances, and playtesting are all certainly good design practices. Just don't drink too much of this rationality Kool-Aid.

## To review...

Metrics are useful measurements to help blockout levels at a consistent scale. If a level feels weird or awkward to play, it may need better attention to metrics.

To recreate a real world place, don't copy the exact measurements -- video game scale is often weird and inconsistent. Instead, scale depends more on your intuition of "what feels right."

To use metrics, blockout a metrics test map / zoo / playground with simple gridded textures, and then walk around in it. If you're using a modular kit, then build a test level and walk around in it, to make sure the modules are at the right scale and dimensions you need.

The most important level design metrics to consider are usually player physics metrics like movement speed, stair step height, and jump distance. You'll also probably want common building metrics like typical doorway width, window height, wall height, etc.

Metrics reflect human perception, which is affected by anything on screen or even game audio.

Many metrics are just "good numbers" and guidelines you give yourself, they're not a scientific infallible way to perfect level design. Metrics are useful, but metrics are not magic.

## Now what?
  * Use metrics to build a [blockout](../).

## Further reading on metrics
  * Examples of detailed metrics breakdowns:
	  * [Doom metrics](./doom.md)
	  * [Quake metrics](./quake.md)
  * ["Scale and your map"](https://tf2maps.net/threads/guide-scale-and-your-map.12605/) guide by Grazr. Even if you're not making a Team Fortress 2 map, it is useful to see how they derive their suggested metrics here.
  * [Source Engine / Half-Life 2 metrics (Valve Developer wiki)](https://developer.valvesoftware.com/wiki/Dimensions)
