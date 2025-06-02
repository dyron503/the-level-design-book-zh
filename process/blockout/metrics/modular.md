# Modular kit design

How to measure and design modular kits, 3D tilesets for building levels

When doing a [blockout](../) or [art pass](../../../process/env-art/), you might use a modular kit -- a 3D tileset of modules, meshes designed to snap together. This comes from the real-life building practice of [prefabricated modular construction](https://en.wikipedia.org/wiki/Modular_building).

If you're new to 3D modeling or level design, then don't attempt to design your own kit yet. Many considerations go into designing a robust kit. Your first kit will probably be very hard to use, especially if you haven't learned from using other peoples' kits already. Instead, see our list of [Resources](../../../appendix/resources/) to download a free pre-made modular kit suitable for prototyping.

But if you have experience in level design and 3D tools, then you are ready. On this page we will detail the many considerations and best practices for designing your own modular kit.

Most of the info on this page comes from Joel Burgess' excellent GDC talks on designing modular kits for big open world games: ([GDC 2013: Skyrim's Modular Approach to Level Design](http://blog.joelburgess.com/2013/04/skyrims-modular-level-design-gdc-2013.html) ([slides](http://www.slideshare.net/JoelBurgess/gdc2013-kit-buildingfinal))) and ([GDC 2016: The Modular Level Design of Fallout 4](https://www.youtube.com/watch?v=QBAM27YbKZg) ([slides](https://www.slideshare.net/JoelBurgess/gdc-2016-modular-level-design-of-fallout-4), [video](https://www.youtube.com/watch?v=QBAM27YbKZg))).

## 1. Pre-production

do you have a lot of level designer time, and need to reuse limited art assets many times?

planning kit percentages, decide what is most important first

how granular / chunky should the kit be? depends on what level designers need / want, more customization OR faster prototyping time?

## 2. Blockout the kit

DO NOT MAKE VARIANTS YET, just build basic pieces first

### Prototype metrics

decide on your units... build to a human scale

### Common module types
  * floor, ceiling, wall, doorway (single), doorway (double), window, corner
  * platforms (landscape)
  * glue
  * flanges and arches (caves)
  * shells (caves)

### Define a footprint

stay in footprint / bounding box

### Asset naming

pay attention to naming, level designers and kit artists need to agree on a pattern

Epic's recommended naming scheme?

## 3. Metrics: stress test the kit

do NOT just stop at an ideal case

collision is one of the biggest issues, make sure you can't get stuck?

### Loopback Test

### Stack Test

can you build multi-level environments? floors should NOT be paper thin, they have thickness and mass just like walls

### Gap Test

do you have enough glue for interior kits with off-angle construction? essential for tunnel or cave kits

## 4. Art pass the kit, make variants

texture variations go a long way, and are "cheap" -- you don't have to test and validate the module geometry again

consider building a tool for easily swapping in module types, which will make art pass and remesh much faster

## Sources

As mentioned at the top of this page, much of the info here comes from two excellent GDC talks by Joel Burgess, which are a must-read for anyone doing modular construction:
  * ["GDC 2013: Skyrim's Modular Approach to Level Design"](http://blog.joelburgess.com/2013/04/skyrims-modular-level-design-gdc-2013.html) ([slides](http://www.slideshare.net/JoelBurgess/gdc2013-kit-buildingfinal)) is the "101" introductory talk to modular kit design considerations, and how they approached building out levels for Fallout 3 and Skyrim, while avoiding the worst of Oblivion's sins.
  * ["GDC 2016: The Modular Level Design of Fallout 4"](https://www.youtube.com/watch?v=QBAM27YbKZg) ([slides](https://www.slideshare.net/JoelBurgess/gdc-2016-modular-level-design-of-fallout-4), [video](https://www.youtube.com/watch?v=QBAM27YbKZg)) is the "201" intermediate talk that elaborates on what they did for Skyrim's modular kits, and expanded when building Fallout 4.

## Further reading
  * ["Modular Level and Component Design" by Lee Perry](https://docs.unrealengine.com/udk/Three/ModularLevelDesign.html) for Game Developer magazine, Nov 2002. A solid article by the lead level designer on Gears of War (2006), one of the first game dev writings to detail modular construction practices -- which only began emerging in the early 2000s when brush-based CSG construction began falling out of fashion. Included here mainly for historical interest; compare against [History of the level designer](../../../culture/history-level-designer.md).
