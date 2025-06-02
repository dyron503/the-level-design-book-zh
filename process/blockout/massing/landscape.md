# Landscape

How to plan and sculpt 3D terrain for level design; painting, planting

## What is landscape design?

Honestly there's not much existing theory or documented knowledge about level design and landscapes. Environment artists tend to work at a small scale with limited portfolio piece scenes, while level designers focus on buildings. When you look for tutorials or guides on this topic, almost everything will focus on engine-specific sculpting tools and geological simulation tools -- and nothing about the actual act of designing the terrain. Our existing design theory has basically neglected the landscape, which feels foolish when so much modern shooter, open world, and multiplayer design happens in landscapes.

Unfortunately, real world landscape architecture provides only limited insight for level designers. The landscape architect must account for surrounding ecology, climate, hydrology, soil chemistry, archeological mitigation, land rights, building codes... these are interesting factors to consider for worldbuilding, but definitely out of scope when you're just trying to blockout some basic level geometry.

So in this section, we want to focus on design and function. We define landscape design in video game levels as the purposeful shaping of topography to aid desired player flow and experience goals.

## Anatomy of a mountain

Landscapes are made of rock, dirt, and sand, gradually worn down by wind or water (erosion).

When the tectonic plates along the Earth's crust interact, they often push rock upward ([tectonic uplift](https://en.wikipedia.org/wiki/Tectonic_uplift)) and form a variety of mountains. When warm air rises and pushes clouds toward the top of a mountain, the higher altitude and lower air pressure causes the clouds to rain. That rain water flows back down the mountain, forming rivers and valleys. That rain stays on the windward side of the mountain range, while the other downwind side ([leeward](https://en.wikipedia.org/wiki/Windward_and_leeward)) loses moisture to the hotter air and thus stays relatively dry and arid ([rain shadow](https://en.wikipedia.org/wiki/Rain_shadow)).

To design a plausible naturalistic landscape, consider how various type(s) of rock, erosion, and climate will shape the terrain. Then consider how the local inhabitants responded to that terrain.
  * Water flows downward and curves around obstacles. That means rivers curve a lot, which also means mountains and valleys curve a lot.
	* ... so roads and paths should curve around as well, since humans must follow terrain. Straight flat highways and roads are relatively modern, and imply a powerful industrial society that can devote (or waste?) resources to grading roads.
  * On taller mountain ranges, there is often a prominent [tree line](https://en.wikipedia.org/wiki/Tree_line) that marks where trees can no longer grow because it is too dry, cold, or windy. Above the tree line, the mountain rock is clearly exposed with occasional bushes / plants, or heavy snowpack in the winter.
  * Vegetation holds dirt in place. Trees with deep roots are especially good at resisting erosion and blocking wind. Forests act as [windbreaks](https://en.wikipedia.org/wiki/Windbreak), which means there can be different biomes on the windward / leeward side of a forest.
  * Elevation changes affect wind and water patterns. If your level features mountains, should the biome be the same on both the windward / leeward

## Landscape sculpting workflow

People have been sculpting for thousands of years, so there's a lot of theory about how to sculpt, and it's a topic that deserves its own book. Here we're going to focus on the basics of sculpting as they relate to sculpting terrain in a game engine:
  1. [Terrain layout](#id-1-terrain-layout): draw a simple diagram of the landscape with labels. What are the different biomes and microclimates? Which areas are most important?
  2. [Terrain blockout](#id-2-terrain-blockout): sculpt rough shapes for the landscape, with attention to flow and scale. How big is each valley, hill, mountain, or canyon? Is it high or low, long or short, sharp or smooth?
  3. [Terrain metrics](#id-3-terrain-metrics): measure travel times, heights, and traversable ramps / slopes. Is it clear where the player can go? Do locations feel too close or too far?
  4. [Art passing](#id-4-art-passing): sculpt and paint smaller details, apply set dressing. Does this space have a clear mood? Does it feel lived-in or plausible? "Finished"... or empty?

After each stage, we of course strongly recommend [playtesting](../playtesting.md). When playtesting, check for:
  * Areas that feel too big, routes that feel too long or too annoying
  * Blocked areas that shoudn't be blocked, unclimbable slopes that look climbable
  * Game breakers where the player can get stuck or fall into a crevice

### 1. Terrain layout
First, draw a [layout](../../layout/) to plan the landscape. Shade regions according to their theme and local climate. Label and highlight prominent areas. Your landscape layout drawing should be able to answer these questions:
  * What are the biggest areas, which areas need to be next to each other?
  * What is the theme of each area, and how does it relate to adjacent areas?
  * What types of art assets will each area need?

In the example layout drawings below from World of Warcraft, note how the dev team began with a simple [bubble diagram](../../layout/#3-bubble-diagrams) to begin solving the spatial relationships. As they spent months / year iterating on the level, the final landmass retained similar organization but resulted in very different sizes and shapes. The "Highmaul" area in the top-left roughly tripled in size, the flood plains halved, and the beach expanded into a harbor. Plan to deviate from your plan.

### 2. Terrain blockout
Where does the player start and what is the [critical path](../../layout/flow/#critical-path), if any? What's the primary and secondary [circulation](../../layout/flow/#circulation) through each zone, and between zones?

Does the [massing](./) feel small and cozy, or narrow and claustrophobic? What is the spatial identity of each area in the overall [composition](./composition.md)?

Site planning
  * Figure out [metrics](../metrics.md) early, especially for landscapes. In most terrain tools, it is difficult to shrink / expand / move different parts of the terrain after the initial sculpt. Moving a mountain is trickier than moving a wall.
  * Define the palette of big recurring shapes and objects common in this area (e.g. a house; a tree) and include their placeholders in the blockout.

For big development teams like Blizzard that need to coordinate production across multiple departments, this blockout phase is also a good time to do [research](../../preproduction/research.md) and planning with environment artists:
> Take for example the new Nagrand. Not only do we have the environment that you know of as the Nagrand from Outland, but new areas, like a wetlands, and a higher elevation arid region. The visual clash of these disparate environmental themes could be quite jarring if not handled with care. There is a constant conversation between the level designer and the environment artist about shape language, color, diversity, scale, mood, model usage, and ultimately the visual tone of the zone as a whole that keeps the zone development moving in the right direction."
> -- Ely Cannon, senior level designer on World of Warcraft, from ["Artcraft - Level Design part 3"](https://www.mmo-champion.com/content/4457-Artcraft-Level-Design-Part-3)

### 3. Terrain metrics
Now is a good time to think about balance... shallow slopes vs deep slopes, thin ledges vs thick ledges

Include generous space for landings at the top and bottom of ramps / stairs, or else players might overshoot and jump off a ledge

Is this walkable area readable, are the boundaries clear? Can the player survive a fall from __ height, can they walk up this __ degree slope?

Travel time, where is the nearest fast travel point

### 4. Art passing
Refine shapes and overall [composition](./composition.md) and add some details (grass, plants, rocks). Is the silhouette, geology, and erosion pattern plausible or consistent? Work on lighting, mood, and color palette. Does each sub-region feel distinct and readable?

You should still be making big changes to the terrain btw, and each time you do, repeat step 2 and 3

## Procedurally generated biomes

Handpainting grass and flowers is time-consuming, and if you ever redo your art then you'll just have to paint everything all over again.

The most common method is to define biomes, thematic palettes of foliage and textures that automatically decorate a landscape. Then the terrain system can automatically decorate itself by procedurally generating the details.

Big AAA open world games invest a lot of in tools, scripting, and environment art to automate their landscape art passing workflows like this. It usually isn't practical to do this unless you're making a big project with a team.

## Topology

### Sculpting
Sculpt a solid [blockout](../blockout.md) first. Resist the urge to sculpt details.
Use "set height" brush to layout floor planes and terraces
Your general sculpting workflow will be: (1) add or subtract mass, (2) smooth, (3) repeat forever
To define a slope, sculpt terraced "steps" and then smooth over. For narrow ledge ramps along the side of a mountain or canyon, a dedicated ramp tool is probably easier.
Don't oversmooth, don't leave everything a blobby melted mess... sharpen and crease, define shapes

For each region, start with 3-4 basic materials and shades.
Paint with consistency. Don't reuse a cliff material as a ground material.
Do the big basic flat sculpt first, then switch to increasingly smaller brushes to smooth over slopes and add minor height variations to the floor plane.
Avoid using erosion brushes for blockout... these can't do level design for you!! These are for detailing your level later in the design process

### Topological patterns
Plateaus are raised landforms with flat tops. Terraces are flat surfaces cut from a slope.
Craters are big deep holes in the landscape. Bowls are shallow holes in the landscape, and hollows are smaller bowls. Think of them as negative plateaus which can also be terraced. Descending into these surface depressions can offer a sense of safety, or perhaps a sense of being trapped.
In real-life, terraced bowls make for fantastic naturalistic amphitheaters that focus sound and provide a big comfortable gathering place. Conversely, a small hollow can offer a sense of closeness and intimacy. In games, bowls are most often deployed as artillery craters in battlefields to offer low shallow cover -- which, we suppose, is its own form of closeness and intimacy.
Combining a plateau with a crater produces a unique volcano-like effect that could also double as a sort of shelter or hideout (above, top-left)

## Paths
### Path design
Axial paths are straight, angular, and efficient, associated with human power and control.
Meandering paths are curved, round, and inefficient, associated with nature and leisure. pg 91
Paths respond to constraints:
  * Users. Who made this path, and who is using this path today?
  * Topography. Paths usually follow the curve of the landscape or shoreline. Cutting into the landscape or tunneling is a lot of work.
  * Vegetation. Paths usually go around large trees or dense vegetation. Clearing land is a lot of work.

Sharply painted paths with hard materials imply maintenance. Disused / occasional paths with soft materials blur and dissolve.

TODO: Breath of the Wild "triangle composition"
TODO: find BotW screenshots that matches both diagrams

### Path types
  * Ledge paths are open on one side, closed on other. Common for hiking trails on mountains and canyons. Useful for suggesting scenic views, or offering a pleasant contrast between open view vs. closed enclosure.
  * Cuttings are enclosed on both sides, usually "cut" through a landform or with retaining walls. It can feel safe and relaxing on a sunny day, or damp and mysterious on a cold dark night.
  * Ridge paths are open on both sides and raised up. Common for big open wetland areas, offers a big sweeping exhilarating view if there's enough height.
  * Switchbacks or zig zag paths go back and forth with periodic stopping places to control your pace. Not naturally occurring, but often used on steep hiking trails to make ascent (or descent) safer.

## Gardening
A landscape is more than the landmass and terrain, it's also about the overall climate, ecology, and vegetation. Landscape architects work heavily with gardening and plantings.
Every video game landscape is a garden, intentionally shaped to facilitate an aesthetic or mood. Video games expect us to suspend disbelief and pretend that diegetically, within the fiction of the game world, that these are untouched wild places. This is a fun lie we reserve for players, but as designers, we should never be taken in by our own lies.
Do research on your desired climate
An ecotone is a boundary where two different ecologies meet. It can be sharp or blurred.

### Trees
Trees are basically walls that you can walk through; they enclose spaces through repetition and verticality.
thin enclosure (french garden) vs thick enclosure (a glade in the middle of a forest)
Tree planting: natural or artificial? Artificial: quincunx, formalized forest (pg, 65)
Vary plantings by height
Complex planting: understand humidity, wind, rain shadows, etc

## Example landscapes

### "Pinar del Mar" Island in Alba, by ustwo games
[Alba: A Wildlife Adventure](https://www.albawildlife.com/) is a 3D open world exploration game about environmentalism and bird watching, set on a Spanish island called Pinar del Mar.
In her post ["The Environment art of Alba: a Wildlife Adventure"](https://medium.com/@ustwogames/the-environment-art-of-alba-a-wildlife-adventure-6bddd8b56955), environment artist Jessie van Aelst wrote a breakdown of her environmental design and development process.
  * [Pre-production](../../preproduction/): early on, the team defined four pillars for the entire game -- care for nature, sense of Spain, human impact on natural world, and freedom of childhood.
  * [Research](../../preproduction/research.md): they went on virtual tours through Spain via Google Maps, and even went bird watching in real-life. They collected a lot of photo reference and assembled moodboards.
  * [Blockout](../../blockout/): they made an early version of the island with simple geometric shapes and flat colors, allowing them to quickly iterate and test game systems / characters -- once they had a better idea of the game, they later redesigned and rebuilt the island entirely.

For building up the landscape, ustwo developed a custom non-destructive terrain tool workflow in Unity.

For sculpting the main landscape topology, they used a custom Unity editor tool to place splines that procedurally painted onto the internal terrain heightmap at editor-time. This spline-based approach allows for a non-linear non-destructive workflow with smooth flowing shapes that they could fine-tune at will. A designer could also copy-and-paste large landmasses. And because each stroke is a separate game object, that also means multiple people could merge their landscape changes together relatively easily. (note from editor: I'm actually really impressed by this.)

Terrain splines have three brush modes: ridge (for hills and terraces), valley (for rivers and ponds), and level (for flattening / smoothing). The spline's stroke falloff is a user-adjustable AnimationCurve. It also has a built-in terracing curve, as well as a customizable noise modifier.
Each spline pushes / pulls the terrain in a certain way, and the accumulation of all these splines results in a complex landscape.

For texturing, the landscape uses a basic four channel splat (RGBA). Each color (red, green, blue, alpha) corresponds to a texture type -- dirt, clay, grass, and sand. The triplanar terrain shader also applies extra masks for splat transitions, and sets different textures based on world position / world normal.
> "For each splat, we had a ruleset. Sand would only appear on certain low heights of the terrain. Dirt would come in as the next layer in the height as well as appear on really flat and even surfaces. Then it would transition into Grass, almost all areas of the game are grass unless the incline was so drastic it would then turn into cliff splat material." "After this pass was done we added some more detail maps to each splat. This means the gradient transitions between splats would now have a bit more detail. These maps really helped with stretching the bandwidth of our limited amount of terrain splats."
> -- env artist Jessie Van Aelst, from ["The Environment art of Alba: a Wildlife Adventure"](https://medium.com/@ustwogames/the-environment-art-of-alba-a-wildlife-adventure-6bddd8b56955)

They also implemented extra "terrain stamps" overrides, editor-only game objects that could project a specific splat color onto the underlying terrain. This allowed them to add additional details and paint roads / paths, mask out foliage, etc. In the GIF below, note that the last frame consists of hand-placed details, on top of the procedurally generated base.

The team divided the island into several distinct biomes, each with their own plant and animal populations. Artists configured different biome elements for procedurally generated detail scattering / set dressing.
> We defined each biome with biome elements. Ex: a pine tree forest biome would include pine trees, pine cones and bush biome elements. The biome elements all have variant slots as well as variables indicating how likely each asset would spawn and what the scale ranges would be.
>
> These biomes would then be placed onto the terrain in a similar fashion to the terrain manipulation. The marker would project cubes onto the terrain to indicate the area where it would generate a biome. The colour of these cubes would represent:
>
> Yellow — area where biome generation happens. Green — an asset will be generated here. Red — an asset could spawn here but won’t because of restrictions
>
> These colours were very useful for us to understand what to expect before generating the terrain. A requirement we came up with was to be able to move around the biome markers and keep the compositions inside intact. For example, a clump of trees that was spawned in just the right composition would spawn in the same composition even if we moved this biome to the other side of the island.
>
> Biomes would generally overlap, so how do we make them work together? In order to overlap or put a biome inside another biome we worked out a system of prioritisation. The marker’s vertical position would therefore decide what would be overwritten.
> -- env artist Jessie Van Aelst, from ["The Environment art of Alba: a Wildlife Adventure"](https://medium.com/@ustwogames/the-environment-art-of-alba-a-wildlife-adventure-6bddd8b56955)

## Now what?
  * Landscapes usually won't feel natural until after extensive [art passing](../../env-art/).
  * Narrative-focused landscape projects benefit greatly from [worldbuilding](../../preproduction/worldbuilding.md).
  * Unity extra terrain tools: [https://docs.unity3d.com/Packages/com.unity.terrain-tools@2.0/manual/index.html](https://docs.unity3d.com/Packages/com.unity.terrain-tools@2.0/manual/index.html)
  * Unity Path Paint tool: [https://github.com/Roland09/PathPaintTool](https://github.com/Roland09/PathPaintTool)

## Further reading
### Terrain sculpting workflow
  * [World of Warcraft: Level Design Panel](https://www.youtube.com/watch?v=eYDd3T_s1zo) (Blizzcon 2016) features 30 minutes of level designers Matt Sanders and Ely Cannon sculpting, painting, planting, and set dressing small mountainous island zones in Blizzard's internal map editor for World of Warcraft.

### General landscape architecture books
  * [Form and Fabric in Landscape Architecture](https://issuu.com/tdgarden/docs/form_and_fabric_in_landscape_archit) by Catherine Dee
  * The Fundamentals of Landscape Architecture by Tim Waterman
  * Theory in Landscape Architecture: A Reader edited by Simon Swaffield
  * The Planting Design Handbook by Nick Robinson
