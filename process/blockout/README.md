---
description: 设计体量和关卡体验参数、打磨寻路体验并通过试玩，打造出基本的 3D 关卡。
---

# 搭建关卡白盒

## 关卡白盒

### 为什么要搭白盒？

白盒（也叫白模或者灰盒）是 3D 关卡草图。使用简明形状搭出，不具细节或经过打磨的美术资产。

搭白盒是为了制作关卡原型，进行测试并调节其基本形状。

关注下图中关卡白盒和最终交付版本的区别。形状一开始是灰色的体块——然后经过数月[跑测](playtesting/)和[场景美术工作](../environment_art/)，白盒变成一堆桶……或者干脆被完全删除。

![《使命召唤：现代战争》（2019）中“码头”场景的草图与最终美术稿对比，Brian Baker](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-M-8CjOctRDm_ccN4vu9%2F-M-8Dt4KaPpenMXMsARp%2Fblocktober_CodMW2019_Docks_BrianBaker.jpg?alt=media\&token=194299e3-8f7f-438b-8295-6b1a5a149975)

白盒**有助于验证。**

在白盒中删除或重建粗糙的几何体花的「钱」很少，但废弃完工的美术成品不但「昂贵」，还很浪费。

还不确定关卡结构的时候，最好花小钱改善它，直到关卡足够完善，可以投入昂贵的后期资源。

与设计文档和草图不同，**你可以游玩白盒，**&#x5728;关卡中流动，评估关卡平衡、遭遇战设计和关卡体验参&#x6570;**。**&#x767D;盒阶段只是开始，从这里你才能发现设计思路能否运作。

> 「如果考虑到《霓虹白客》发售时包含超过 100 个关卡，开发团队制作的废弃关卡数量是这个数字的两倍，而仅 _Smackdown_ 这一关卡就经历了 50 多次修改，那么整个游戏中涉及的调整和重设计就多达数千处。」
>
> _— 来自_ [_《霓虹白客》是如何制作的_](https://www.gameinformer.com/feature/2022/11/25/how-a-neon-white-level-is-made) _。由 Blake Hester 写作, 收录在 Game Informer #350 期_

<figure><img src="https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LtVT8pJjInrrHVCovzy%2Fuploads%2FYgg5qtTDgMUTwNahZRZ2%2FLDB_NeonWhite_Blockout_GameInformer.jpg?alt=media&#x26;token=1eef8217-5311-437c-b58d-17e7b9fa868f" alt=""><figcaption><p>《霓虹白客》（2022 年）「Smackdown」的早期白盒。由 Ben Esposito, Russell Honor, 和 Carter Piccollo 制作 <a href="https://www.gameinformer.com/feature/2022/11/25/how-a-neon-white-level-is-made">(通过 Game Informer 查看)</a></p></figcaption></figure>

### 关键概念

搭白盒时，考虑下面的关键概念：

* 关卡体量由形状塑造，传达体积和重量。
  * _结构是厚重，还是轻薄？这里是怎样的地点？_
  * 地标需要着重考虑。
  * 如今，关卡设计文化对构图有些重视过头了。
* 关卡体验参数
* [**Massing**](https://book.leveldesignbook.com/process/blockout/massing) is the general sense of volume and weight conveyed by the shapes.
  * _Is this structure thick / heavy, or thin / light? What kind of place is this?_
  * [Landscapes](https://book.leveldesignbook.com/process/blockout/massing/landscape) need special consideration.
  * [Composition](https://book.leveldesignbook.com/process/blockout/massing/composition) is currently over-emphasized in level design culture today.
* [**Metrics**](https://book.leveldesignbook.com/process/blockout/metrics) are the general scale, dimensions, and proportions of the level.
  * _Is this area too big or small? Can the player fit in this room?_
  * examples of useful measurements: [Doom metrics](https://book.leveldesignbook.com/process/blockout/metrics/doom), [Quake metrics](https://book.leveldesignbook.com/process/blockout/metrics/quake)
* [**Wayfinding**](https://book.leveldesignbook.com/process/blockout/wayfinding) is the player's navigation process for learning the map structure.
  * _How to help the player find the_ [_critical path_](https://book.leveldesignbook.com/layout/flow#critical-path) _/ level exit? Does the player feel too lost?_
* [**Playtesting**](https://book.leveldesignbook.com/process/blockout/playtesting) is when you run an experiment to see if the level meets its design goals.
  * _Can most players complete the level? Do the_ [_encounters_](https://book.leveldesignbook.com/process/combat/encounter) _work? Is it_ [_balanced_](https://book.leveldesignbook.com/process/combat/balance)_?_
  *   Playtesting is really important. This is the whole point of making a blockout.

      \## Construction methods

There are five common 3D level construction methods in games:

* **Primitives:** arrange simple basic shapes like cubes and boxes.
* **Brushes / modeling:** construct 3D shapes in the level editor.
* **Modular kit:** connect pre-made pieces together, like Lego.
* **Sculpting:** "paint" organic 3D shapes, useful for landscapes.
* **Splines:** create math curves that procedurally generate geometry

#### Primitives

**Primitives** are simple 3D shapes, like the default gray cubes and boxes built into a game editor.

Move / rotate / scale the shapes. Arrange them together, stack them on top of each other, make more complex groups of shapes.

This is a surprisingly powerful blockout method. You can always use this method in any 3D engine or tool, but you'll hit limitations with blocking out anything beyond simple boxy buildings.

<details>

<summary>Advice for blocking out with primitives...</summary>

Pay attention to [**metrics**](https://book.leveldesignbook.com/process/blockout/metrics)**,** establishing scale is tricky.

To make a **ramp**: make a long wide thin cube, then rotate to slope downward. To make **stairs**: avoid suffering and just make a ramp instead

To make a **doorway:** leave a gap between two walls, no door frame. To make a **window:** make doorway-like gap, then fill in with a short waist-height wall

</details>

![dimensional massing diagram by Francis Ching, from "Architecture: Form, Space, and Order"](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-M0ee4eVuNuFAVpXzg-K%2F-M0efIvq7LPUjG7M4Osu%2FFormSpaceAndOrder_Dimensions_FrancisChing.png?alt=media\&token=cd5d2b5b-adcc-4f4d-86de-05a11d1dfb65)

#### Brushes / modeling

**Brushes** are simple low polygon 3D shapes modeled in the level editor.

This was the main level construction method across the industry from 1990s-2000s.

We strongly recommend this method because it offers the most control and handmade feel, but unfortunately most modern game engines often have poor brush modeling tools. It can be tricky to figure out a workflow here.

<details>

<summary>Advice for blocking out with brushes / low poly...</summary>

Use a **3D modeling tool** that emphasizes low poly geometry.

* Unity: [ProBuilder](https://unity.com/features/probuilder) is OK, but [SabreCSG](https://assetstore.unity.com/packages/tools/modeling/sabrecsg-level-design-tools-47418) / [RealtimeCSG](https://realtimecsg.com/) are more focused
* Unreal: use [CubeGrid](https://docs.unrealengine.com/5.3/en-US/cubegrid-tool-in-unreal-engine/) + [Modeling Tools](https://docs.unrealengine.com/5.3/en-US/modeling-tools-in-unreal-engine/) (or [Mesh Tool](https://www.unrealengine.com/marketplace/en-US/product/mesh-tool))
* if the engine can use .MAP or .BSP files, use [TrenchBroom](https://book.leveldesignbook.com/appendix/tools/trenchbroom)

Use a **big coarse grid size** based on [metrics](https://book.leveldesignbook.com/process/blockout/metrics), specifically _player width._

* [Doom](https://book.leveldesignbook.com/process/blockout/metrics/doom) or [Quake](https://book.leveldesignbook.com/process/blockout/metrics/quake): 32u wide player = set grid to 32 or 64
* Unity: 1m wide player = set grid to 1 or 2
* Unreal: 60uu wide player = set grid to 50 / 100, or 64 / 128

</details>

![simple 3D modeling with "brushes" in TrenchBroom; GIF demonstration by Benoit "Bal" Stordeur](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MGiaafOL1SFz9zF9aNV%2F-MGieDp2Fm8LbDvJ1WXD%2FTrenchbroom_Bal_CreateVerts.gif?alt=media\&token=d4b48e7b-24d3-4031-a6e5-0e5d2169c7bf)

#### Modular kit

Snap together pre-made pieces of architecture from a kit of **modular parts**.

However, if the kit is badly designed or poorly configured, it'll be hard to use. If you're a beginner, you probably shouldn't try to make your own kit -- just download one instead.

_For more on planning, measuring, and constructing modular kits, see_ [_Modular kit design_](https://book.leveldesignbook.com/process/blockout/metrics/modular)_._

_For links to download free modular prototyping kits, see_ [_Resources._](https://book.leveldesignbook.com/appendix/resources)

<details>

<summary>Advice for blocking out with modular kit...</summary>

**Configure the Grid and turn on Grid Snapping** (how-to: [Unity](https://docs.unity3d.com/Manual/GridSnapping.html), [Unreal](https://docs.unrealengine.com/4.27/en-US/BuildingWorlds/LevelEditor/Viewports/ViewportToolbar/))

* use a large coarse grid based on module size
* e.g. if wall modules are 5m wide, then set grid to 5

**Use vertex snapping** to align modules precisely (how-to: [Unity](https://docs.unity3d.com/Manual/PositioningGameObjects.html), [Unreal](https://docs.unrealengine.com/4.26/en-US/Basics/Actors/Transform/))

Just **download a pre-made kit.**

</details>

!["graybox" blockout modular kit used for prototyping levels in Skyrim, image by Joel Burgess](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MbP02oa-qIyy5tjCgbG%2F-MbP6Rdo6HOddzlUrPo1%2FLDB_ModularGraybox_Transparent_JoelBurgess_Skyrim.png?alt=media\&token=4a1cd17d-c36a-4edd-bb5f-2c457385153c)

#### Sculpting

Most modern engines have a **sculpting tool** that lets you paint and deform a flat plane.

We use this only for making big smooth shapes like terrain and landscapes; it's bad for hard surfaces like buildings.

But if landscapes are central to a project, there's no way to avoid sculpting.

_For more on sculpting and designing terrain, see_ [_Landscape_](https://book.leveldesignbook.com/process/blockout/massing/landscape)_._

<details>

<summary>Advice for blocking out with a sculpt...</summary>

**Sculpting is often a distraction for beginners.** Making a mountain with a single click is so fun and empowering that you'll forget to do any level design. Be careful! Don't let sculpting tools seduce you!

**Use a large brush size** and focus on big core shapes first.

**Define ground planes** with the [Set Height (Unity)](https://docs.unity3d.com/Manual/terrain-SetHeight.html) or [Flatten Target (Unreal)](https://docs.unrealengine.com/en-US/Engine/Landscape/Editing/SculptMode/Flatten/index.html) brush

**Sculpt slopes as stepped terraces** to define the gradient, then smooth it.

**Avoid erosion / auto-generator tools,** you need control over the design.

</details>

![sculpting landscapes for the "Nagrand" region in World of Warcraft: Legion](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MQA2sisUAlB9q25CfTE%2F-MQAfRAYCcp_SPK5Z06u%2FLDB_WorldOfWarcraft_Nagrand_Editor.jpg?alt=media\&token=12c3c6f6-42e0-4d72-97ce-b2ac6b9f7966)

#### Splines

**Splines** are invisible curves that generate geometry along the path.

These curves are also _non-destructive_; you can adjust a spline at any point and regenerate its geometry.

A spline is ideal for blocking out curvy linear forms like roads or rivers, where it can also automatically deform the surrounding landscape.

It's also possible to generate non-linear areas and buildings with splines too, but this type of workflow isn't common and usually requires custom tooling.

<details>

<summary>Advice for blocking out with splines...</summary>

Like sculpting, **splines are often a distraction for beginners.** Playing with splines is so fun that you'll forget to do any level design. Don't let splines seduce you!

**Spline tooling varies.** They became common only in the mid 2010s. Unreal has excellent built-in support for [Blueprint Splines](https://dev.epicgames.com/community/learning/tutorials/39/populating-meshes-along-a-spline-with-blueprints). Unity users are less lucky and have to try various plugins like [SplineMesh](https://github.com/methusalah/SplineMesh) or [code your own splines](https://catlikecoding.com/unity/tutorials/curves-and-splines/).

**Splines aren't magic.** If you want to make anything more complicated than roads, rivers, or bridges, it will usually require custom tooling and a lot of art support.

</details>

![animated GIF of a procedurally generated bridge defined with a spline in Unreal Engine 4; by Peter Severud (via Artstation)](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-LtVT8pJjInrrHVCovzy%2Fuploads%2FhGdbv9as1rObARSizSQ1%2FLDB_UE4_Spline_PeterSeverud-bridge.gif?alt=media\&token=3533ad65-dab7-41be-afc5-435f357ec831)

{% hint style="warning" %}
**Why not use a 3D art tool like Blender, Maya, Max, or SketchUp to blockout?**

People debate thi&#x73;**.** Here's our take: 3D art tools don't let you tune gameplay, collision, encounters, or items. Playtests become slower and less frequent.

_Example: on an unnamed AAA game, moving a rock requires a multi-step hour-long process: (1) load debug build, (2) find which file has the object, (3) open Maya, (4) edit file, (5) recompile game, (6) load debug build again to confirm change._
{% endhint %}

### How to blockout

Here's a general process. If you're a beginner, or you're at the start of a new project, try to do everything. You will gradually personalize your own process and style.

1. **Sketch layout**
2. **Add ground plane, scale figures, walls**
3. **Playtest**
4. **Diverge, iterate, and playtest again**
5. **Repeat step 4 until done**

#### **1. S**ketch [layout](https://book.leveldesignbook.com/process/layout)

It can be difficult to blockout without any plan, especially for beginners. Even a simple scribble can help a lot.

Look at the layout sketches below. The left sketch emphasizes the scale of each space, the middle sketch focuses on the relationships between the areas, while the right sketch is a more detailed floor plan drawing. Any of these sketches can work, any of them can help you plan a blockout.

Just draw something!

![example: three similar but different layout drawing styles that can maybe help you plan the blockout... any of these are fine to get you started, JUST DRAW SOMETHING](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MJe5grxs_9aB9cQTHIv%2F-MJe8gVOx8EpDXFe1j7R%2FLDB_Blockout_LayoutSketch.png?alt=media\&token=88d63751-302f-4b0e-b967-629600c0a5e7)

#### 2. Add ground plane, scale figures, and walls

**Create a ground plane** (or a big flat cube) near the center of the 3D space (0, 0, 0).

Use a light-colored gridded prototyping texture so that you can visually estimate sizes and scales. This floor object will help "ground" the rest of the level geometry, providing a horizon line and context for everything else to rest upon.

**Add a player-humanoid scale figure** to help establish scale.

If you don't have any humanoid assets, create a roughly human-shaped block to serve as a placeholder. The scale figure helps establish consistency and clearance for the player.

_For more on common hallway / wall sizes and humanoid dimensions, see_ [_Metrics_](https://book.leveldesignbook.com/process/blockout/metrics)_._

_For links to free prototyping and blockout textures, see_ [_Resources_](https://book.leveldesignbook.com/appendix/resources#prototyping-blockout-textures)_._

![example: a gray ground plane with a yellow scale figure standing on it](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MJe5grxs_9aB9cQTHIv%2F-MJeAjdNKCAHbaWFL8CD%2FLDB_Blockout_GroundPlaneWithScaleFigure.png?alt=media\&token=0a204b23-9fea-46ec-bb1b-0c0a6ee75711)

**Build a wall segment** that's approximately **150-200% as tall as the scale figure**.

If you're working in a modern game engine, sizes don't have to be exact -- the sense of proportion is most important to establish here.

If you are blocking out with a [modular kit](https://book.leveldesignbook.com/process/blockout/metrics/modular), just place a standard wall module next to the figure.

**Texture the wall with a different color** from the ground plane. Color and brightness provide important context for understanding what the space is made of, and how these various floor and wall planes relate to each other. If you are afraid of colors affecting your blockout too much, then at least use textures with different shades of gray.

![example: added a white wall segment that's twice the height of the scale figure](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MJe5grxs_9aB9cQTHIv%2F-MJeDELv7F2AvTzb119H%2FLDB_Blockout_WallSegment.png?alt=media\&token=d3ea7bdf-6afb-4cb0-9d4e-ece580a2af0e)

**Copy & paste wall segments** to build up more space until you have at least one room or hallway. Some tools feature special "duplicate" or "clone" commands: in Hammer, hold Shift and drag the brush; in UE4, hold Ctrl+Shift and drag the wall object.

Intersections are OK. Messy is OK.

To make a doorway or window, just leave a gap between wall segments, and fill it in later. Entryways and hallways should be at least twice as wide as the scale figure.

![example: copy-and-pasted / duplicated more wall segments, based on the first wall](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MJe5grxs_9aB9cQTHIv%2F-MJeEYD8eFYH12CCC6WN%2FLDB_Blockout_DuplicateWalls.png?alt=media\&token=93a136db-26fd-4a08-a143-e6d11fa1759b)

#### 3. Playtest

**Do a simple self-playtest:** **walk around the space, within the game engine, with full player gravity, collision, and speed.**

The purpose of the blockout is to experiment. To verify the results of the experiment, you must test the prototype. _Do NOT just fly around in the editor view,_ that won't help you imagine the player experience.

* [**Massing**](https://book.leveldesignbook.com/process/blockout/massing)**.** Do the level's shapes make sense? Is it confusing to look at?
* [**Metrics**](https://book.leveldesignbook.com/process/blockout/metrics)**.** Does the player fit through every door and passage? Do the stairs / ramps work? Can the player jump where they're supposed to jump?
* [**Flow**](https://book.leveldesignbook.com/process/layout/flow)**.** Does movement feel slow or fast, smooth or complex? What type of movement is ideal for your intended design goals?

![example GIF: walking around the half-built space in the game engine, playtesting as soon as possible](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MJe5grxs_9aB9cQTHIv%2F-MJeJ3Z58qdf26qnGLQe%2FLDB_Blockout_WalkAround.gif?alt=media\&token=7e046fea-8dfe-458a-9afd-13e5d76435ab)

#### 4. Diverge and iterate

**Diverge from original plans and respond to the playtest.**

99% of the time, your blockout will not survive a playtest. Rooms will feel awkward, doorways too narrow, the layout too confusing. But this is exactly why we blockout!

Want to rebuild huge sections of your blockout? _Go for it._ Want to delete an entire room? _Do it._ Need to split a courtyard into two smaller areas? _You have permission._

![example: following a layout sketch, more areas blocked out with more scale figures](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MJeMC4-hkmZuYJmjtP_%2F-MJeORHBJk5wedNsrlFw%2FLDB_Blockout_Continue.png?alt=media\&token=74bd0d75-3415-4e0e-82fc-8ab2ddae649c)

Keep an open mind about what your playtests and walkarounds are telling you.

**Continue adding new scale figures, walls, and floors.**

**Then playtest again.**

![example GIF: the original blockout felt too cramped, so what if we widened the space and deleted the walls?](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MJeMC4-hkmZuYJmjtP_%2F-MJeV-8_20G-hHvLwdem%2FLDB_Blockout_Iterate.gif?alt=media\&token=11cad130-4fd5-444c-ab92-2764debc514a)

#### 5. Continue iterating

Keep an open mind and continue this cycle of modification + playtesting. Continue developing the blockout. Build, then walk around in it, then modify, then playtest again... and repeat. This design process is called **iteration**, because we are making new _iterations_ that build off of the strengths of the previous version.

As you gradually build more and more of the level, it may surprise you how much it changes over time. Let the map surprise you.

![](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MJeMC4-hkmZuYJmjtP_%2F-MJeZWyTKE3_-naKWebY%2FLDB_Blockout_IterateAgain.png?alt=media\&token=95f125da-c5cb-437d-8c6f-87e52a936800)

### Common blockout problems

* **(most common) My blockout feels too small / too big.**
  * Use more scale figures during construction.
  * Playtest more often and catch scaling problems sooner.
  * Too big? Delete unnecessary rooms and compress what's left.
  * Too small? Expand outermost walls, then expand the center to fill up the new space.
  * Or delete everything and rebuild. It's just a blockout.
* **I have anxiety and stare at the empty level editor screen without making anything.**
  * Sketch a layout drawing, and then try to follow that plan.
  * Just blockout one simple room. You can always delete it later. The point is to get rid of the blank page. In drawing, this is "activating the canvas"; in writing, this is a ["shitty first draft."](https://wrd.as.uky.edu/sites/default/files/1-Shitty%20First%20Drafts.pdf)
  * Do something else and return to the blockout later.

### Example blockouts

#### "Castle" for Dirty Bomb (Splash Damage)

![layout, blockout, and final version of Castle for Dirty Bomb, by Splash Damage ("Blocktober: Dirty Bomb")](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MLDeIzewXRUNnJ5PFQB%2F-MLDhORGMq9yBPegLNFd%2FLayoutBlockoutProduction_Castle_DirtyBomb_AnthonyMassey.jpg?alt=media\&token=3c2cd3e0-af4a-43b1-8665-3233a5818ce1)

Splash Damage level designer Anthony "MassE" Massey designed the map Castle for the competitive multiplayer team shooter Dirty Bomb. Massey took inspiration from twisting medieval streets and typology of the real-life Tower of London, and conceptualized the initial layout drawing (above, left). But note how the resulting blockout (above, center) differs from the layout with fewer curves, more 90 degree angles, and chunkier areas. The layout was just an initial guide. Because this is a multiplayer shooter map, the design team playtested the blockout with a focus on movement and combat [metrics](https://book.leveldesignbook.com/process/blockout/metrics):

> “The scale of maps is always the hardest aspect to get right. It’s important to plot your main paths and measure these distances; we’re looking for anything between 8 and 12 seconds from spawning to an objective. \[...] Anything longer than that and players get frustrated when they respawn and have to run back. On the other hand, if the time is shorter it risks the map feeling too small for 8v8 matches, and can lead to chaotic gameplay. \[...] This stage is crucial to map development, but our team operated by a simple rule of thumb; if it feels long, it’s too long."
>
> "Considering \[player classes] is the next step. We had to look at combat ranges to allows our entire arsenal to function, \[...] while also ensuring variety in combat spaces to allow \[different abilities] to be viable (like \[an airstrike ability]). In real terms, this means considering the ratio between outdoor and indoor areas, ensuring \[characters with outdoor-focused abilities] were viable."
>
> \-- from ["Blocktober: Dirty Bomb" Splash Damage blog post](https://www.splashdamage.com/news/blocktober-dirty-bomb/)

#### "World's Edge" for Apex Legends (Respawn)

![final detailed blockout (left) and final art pass (right) for "World's Edge" map in Apex Legends; blockout by Rodney Reece](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MO8sJkf5R21JCooOety%2F-MO8uy0cr2ThBu1jW33E%2FWorldsEdge-BlockoutToFinal_ApexLegends_RodneyReece.jpg?alt=media\&token=13d43a80-2f72-4a6d-9629-9183e24f0ac5)

Respawn level designer Rodney Reece built the blockout for "World's Edge", a large competitive multiplayer map for first person battle royale game Apex Legends. Notice how the map changed drastically from blockout (left) to art pass (right) in not only theme but also layout and composition.

> "Originally the idea was the map was snowy. But art wanted to bring green into the map, and in one of the meetings, Robert Taube suggested what if the Epicenter (then called Frozen Explosion) caused the snow.
>
> A key to being a good designer is being flexible to new ideas. For instance, the Art team came up with The Dome. In my blockmesh, it was a volcano. They pitched it and I adjusted to incorporate the idea. I had to create a new layout for it, but it made it better.
>
> But other times, certain \[points of interest] are fun from the beginning. In those situations, I am more stubborn about what can change. Sorting Factory is a good example of that. It's important to identify what's precious and what's flexible in terms of layout. Because it takes a team!"
>
> \-- [remarks by Rodney Reece (@RodneyReece7)](https://twitter.com/RodneyReece7/status/1336783331711623168)

### Against blockouts?

For some projects, the traditional blockout might be less helpful. The experience may depend less on spatial design and more on the [art pass](https://book.leveldesignbook.com/process/env-art). Blockouts can't validate a concept dependent on art or other assets.

#### Vertical slice for "Firewatch" (Campo Santo)

For the first person narrative exploration game Firewatch (2016), developer Campo Santo wanted to focus on mechanics like walking and talking; the main appeal of the game concept was looking at art passed scenery and listening to voice acted dialogue. Following typical best practices, they first built a blockout to test the viability of these mechanics. However, the blockout did not help them answer any questions about the player experience because the game pacing was fundamentally a narrative design and environment art issue, not so much a level design issue. The traditional blockout process wasn't working.

According to environment artist Jane Ng's account, it wasn't clear whether Firewatch would "work" as an experience until they _skipped the blockout process_ and instead completed a vertical slice prototype with an art passed environment and near-final dialogue.

!["Greyboxing did not answer any of the important questions" and other slides from "Making the World of Firewatch" by Jane Ng at GDC 2016](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MJsODeoivwyff8ntbp4%2F-MJsPLWJYvQjvOzsrzqG%2FBlockout_Firewatch_JaneNg_GDC2016.jpg?alt=media\&token=4e93e95d-0dbd-44d4-8444-25fec5e68761)

#### Location scouting for "Untitled Goose Game" (House House)

For the top-down third person stealth puzzle game Untitled Goose Game, developer House House sought to create an authentic-feeling British village in 3D. Level designer Jake Strasser had never been in the UK, so blocked out the initial level with occasional use of photo reference. However, this blockout-first approach required Strasser to fill-in gaps from his imagination -- and because he didn't have a British imagination, these gaps often felt implausible or inauthentic in subtle ways, counter to their intent. The traditional blockout process wasn't working.

So instead, Strasser tried a [research](https://book.leveldesignbook.com/process/preproduction/research)-first "location scouting" approach. He went on an exhaustive virtual tour of various UK villages, taking lots of photos from Google Street View. After recreating several village streets in-game, Strasser finally pin-pointed what type of structure suited the game's needs, and settled on an unusual side street layout based on [Pump Street in the village of Orford](https://goo.gl/maps/WAkqYmNRARyAEimi9). Here, blockout was less about building a space, and more about discovering a space.

!["It started feeling more like a unique place with its own quirks and history"... from "Google Maps, Not Grayboxes: Digital Location Scouting for Untitled Goose Game" for GDC 2021 by Jake Strasser](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-LtVT8pJjInrrHVCovzy%2F-MfLamIDFl70FqTdwVLz%2F-MfLqnwVxJhTOa4jEdZf%2FLDB_UntitledGooseGame_ResearchReferenceOrford_GDC2021_Jake.jpg?alt=media\&token=2ac751ed-560a-49c9-9fff-114a6a967f11)

### To review

A **blockout** is a simple but playable "rough draft" level with minimal detail. We keep it simple and blocky so that we can easily change it.

You can build a blockout with **primitives**, **brushes**, **modular kit**, **sculpting**, or **splines**. The best technique will depend on your engine and project, or you can combine multiple techniques.

How to blockout:

1. **Sketch a** [**layout**](https://book.leveldesignbook.com/process/layout), even a simple one
2. Add a **ground plane,** **scale figures,** and **walls**.
3. **Playtest** immediately; does it feel OK to walk around? You need to know now.
4. **Diverge** from your original plan, **iterate and playtest again**
5. **Repeat step 4.**

**The most common problem is scale**, especially for beginners. Playtesting the blockout in-game is the best way to know if it feels too big or too small.

Blockouts might be less helpful for some projects like single player art-dependent narrative levels.

### Now what?

* Review **key concepts** for blockouts like massing, metrics, wayfinding, and playtesting.
* Once you're built and tested a blockout, do a [**scripting** ](https://book.leveldesignbook.com/process/scripting)pass or a [**lighting**](https://book.leveldesignbook.com/process/lighting) pass.

#### More about blockouts

* [GDC 2018: "Invisible Intuition: Blockmesh and Lighting Tips to Guide the Player and Set the Mood"](https://www.youtube.com/watch?v=09r1B9cVEQY) by David Shaver and Robert Yang is probably the most up-to-date industry-standard blockout talk, showing blockout examples from Shaver's work on Naughty Dog games alongside distilled examples prototyped in Unity. However, it's actually more concerned with [composition](https://book.leveldesignbook.com/process/blockout/massing/composition) and [wayfinding](https://book.leveldesignbook.com/process/blockout/wayfinding) than construction.
* ["Quake Mapping Tips: Building Layouts" (5 min) video by Michael Markie](https://www.youtube.com/watch?v=G4tWWiuaF7g) starts with a very simple one room blockout in Quake 1, then gradually elaborates on it and makes it more compelling to play. Note the frequent playtesting and design iteration. A great example of an improvised blockout process with little pre-planning.
