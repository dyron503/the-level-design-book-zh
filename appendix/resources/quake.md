# Quake resources

Models, textures, sounds, tutorials, and other links for Quake mapping and modding

## Get the Quake Level Design Starter Kit

Download the [Quake Level Design Starter Kit](https://github.com/jonathanlinat/quake-leveldesign-starterkit) (Windows and Linux only) by Jonathan Linat, which contains a lot of recommended tools and assets for single player Quake 1 mapping, all collected in one convenient bundle. This is the easiest way to get started.

## Communities

If you're interested in Quake mapping and modding, we strongly recommend joining a Quake community. It's the best way to learn! Experienced people can give you tech help, advice, and feedback on your work. Some have even been modding Quake for 20+ years.
  * [Quake Mapping Discord](https://discord.gg/58XqmZM) is the biggest public social hub, beginner-friendly with frequent single player design jams and social opportunities
      * For Quake 2, try [Map-Center discord](https://discord.com/invite/BhmHT2kyp2) instead.
      * For multiplayer Quake, try [QuakeWorld.nu](https://www.quakeworld.nu/) and [Quake.World discord](http://discord.quake.world/) instead.
  * [Slipseer](https://www.slipseer.com/) is a new single player mapper-modder hub with downloads, assets, and free file hosting services.
  * [Quaddicted](https://www.quaddicted.com/) is the main single player Quake map archive, currently in the middle of an extensive rebuild (as of 2024).
  * [Func_msgboard](https://www.celephais.net/board/) is the longest running Quake level design web forum, but maybe not as newbie-friendly as QM Discord or Slipseer
  * [The QuakeCast](https://quakecast.podbean.com/) is a long-running podcast series where David "dumptruck_ds" Spell interviews various Quake community members and discusses new releases

## Mapping

### How to make Quake maps
  * get TrenchBroom level editor (included in Level Design Starter Kit linked above)
      * [more info and advice for TB](../tools/trenchbroom.md)
      * [official download page](https://github.com/TrenchBroom/TrenchBroom/releases)
  * most people start with [David "dumptruck_ds" Spell's video tutorials](https://www.youtube.com/watch?v=gONePWocbqA&list=PLgDKRPte5Y0AZ_K_PZbWbgBAEt5xf74aE) ([full playlist](https://www.youtube.com/playlist?list=PLgDKRPte5Y0AZ_K_PZbWbgBAEt5xf74aE))
  * or start with [Andrew Yoder's text tutorial](https://andrewyoderdesign.blog/2019/06/08/making-your-first-map-in-quake-part-1/) (covers basic setup + making your first room)
  * after you know the basics, check out the [Quake Builder video tutorials](https://www.youtube.com/user/mikedm92/videos) by MarkieMusic
  * for useful map measurements and combat stats + design advice, see [Quake metrics](../process/blockout/metrics/quake.md)
  * for more about releasing maps and mods, see [How to package a Quake map/mod](./how-to-package.md).

### Recommended reading
After you know the basics of map construction and feel somewhat comfortable in the editor, learn about more complex design and building patterns:
  * ["How to Make Rooms Look Good"](https://archive.is/VP86K) (2001) on Quake architecture by Xenon
  * ["Curve tutorial"](https://www.quaketerminus.com/hosted/happymaps/curv_tut.htm) (200x) on building "CZG curves" by Christian Grawert
      * ["Mapping for Quake: Advanced Curves" part 1 video](https://www.youtube.com/watch?v=RjzYKGm_DQk) + [part 2](https://www.youtube.com/watch?v=sS0Fr1L2P2w) by David Spell
      * ["Trenchbroom and Quake: Curved Tunnel"](https://www.youtube.com/watch?v=E27I6JCn9jw) by MarkieMusic
  * ["The Door Problem of Combat Design"](https://andrewyoderdesign.blog/2019/08/04/the-door-problem-of-combat-design/) (2019) by Andrew Yoder is a solid introduction to tuning Quake [encounters](../process/combat/encounter.md)
      * ["Balancing Skill Levels for Quake"](https://www.slipseer.com/index.php?threads/balancing-skill-levels-for-quake.554/)
      * [Chris Holden's #quake #leveldesign tweets](https://twitter.com/search?q=@ChrisHoldenDev #quake #leveldesign&src=typed_query&f=top)
  * ["Quake Renaissance"](https://www.rockpapershotgun.com/topics/quake-renaissance) (2021) series about Quake culture by Robert Yang
      * (id Software industry history) [part 1](https://www.rockpapershotgun.com/quake-renaissance-where-is-quake-and-how-did-it-get-here)
      * (25 years of Quake mod history primer) [part 2](https://www.rockpapershotgun.com/quake-renaissance-a-short-history-of-25-years-of-quake-modding)
      * (guide to Quake player culture norms + well-known mods to play) [part 3](https://www.rockpapershotgun.com/quake-renaissance-how-to-start-playing-quake)
  * ["Bal's Quake Mapping Tips & Tricks"](https://www.slipseer.com/index.php?threads/bals-quake-mapping-tips-tricks.100/) (2022) by Benoit "Bal" Stordeur is a crucial must-read for intermediate / advanced Trenchbroom construction techniques.
  * for more on Quake's influence on level design, see [History of the level designer](../../culture/history-level-designer.md)

### Compiling Quake maps
To play Quake maps, you must compile (bake, package) the editable .MAP into a playable optimized .BSP file. You will need both tools and a graphical user interface (GUI).
  * Compile tools: [EricW Tools](https://github.com/ericwa/ericw-tools) (already included in Quake Level Design Starter Kit)
      * qbsp.exe builds 3D mesh + detects "leaks" ([video tutorial: how to fix leaks](https://www.youtube.com/watch?v=kFd-D46OCrg))
      * vis.exe calculates [PVS occlusion culling](https://en.wikipedia.org/wiki/Potentially_visible_set) to optimize map performance
      * light.exe bakes lightmaps and shadows, makes [lighting](../process/lighting/) happen
          * STRONGLY RECOMMEND viewing [light.exe examples](https://ericwa.github.io/ericw-tools/) + [light.exe docs](https://ericwa.github.io/ericw-tools/doc/light.html)
  * Compiler GUI: choose either [TrenchBroom's built-in compile window](https://trenchbroom.github.io/manual/latest/#compiling_maps) or [Necro's Compiling GUI](https://shoresofnis.wordpress.com/utilities/ne_q1spcompilinggui/) (both already in the kit too)

### Example map source files
  * many mods package .MAP source files with the public release, just look in the mod folder
  * [trenchbroom_quake_map_source.zip](https://toolness-media.s3.amazonaws.com/quake/trenchbroom_quake_map_source.zip) ([4.5 mb download](https://1666186240-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces/-LtVT8pJjInrrHVCovzy/uploads/PKHfAru222Fn59yFy5mA/trenchbroom_quake_map_source.zip?alt=media&token=5cedcccc-91c9-4010-82ae-d757fa9c8d6e)) is a collection of the original Quake 1 .MAP source files ([as released by John Romero in 2006](https://rome.ro/news/2016/2/14/quake-map-sources-released)) but converted to modern file format (TrenchBroom compatible) + fixed texture references (with repackaged Quake101.wad), thanks to Atul "toolness" Varma
  * for more about parsing and working with [.MAP files in code, see .MAP file format](./formats/map.md)

### Engines / source ports
To play Quake (and playtest your own maps or mods) you need a source port -- a Quake engine that "ports" the original 1996 engine code and add many new features / compatibility.
We only list free open source ports in active ongoing development. ([see full list of source ports via QuakeWiki.org](https://quakewiki.org/wiki/List_of_engines_and_ports))

Source port | Description
-- | --
[Ironwail](https://github.com/andrei-drexler/ironwail) | current community-standard engine for single player; bundled in Quake Level Design Starter Kit
[Quakespasm-Spiked](https://triptohell.info/moodles/qss/) | previous community-standard engine for single player
[FTE](https://fte.triptohell.info/) | many features + wide compatibility beyond Quake 1 file formats, good for making standalone games
[nQuake](https://www.nquake.com/) | common multiplayer Quake ("QuakeWorld") bundle but lacks many single player / graphics features

## Assets / textures
In Quake modding culture, it is generally considered normal and acceptable to rip models, sounds, and textures from other maps and mods, as long as you credit the original authors.

However, if you rip textures and assets from a .BSP, you'll usually have an incomplete fraction of the full kit. It'll likely be difficult to use. In these cases (e.g. the Makkon set) you're better off finding the full official public texture releases.

### Texture WADs
Quake texture collections are stored in .WAD files. To use textures in a level, download a .WAD and then add the WAD path to the .MAP file using the level editor. (Note: this is not the same as a Doom WAD. Quake WADs are only for map textures.)
  * [Prototype WAD](http://khreathor.xyz/site/prototype/) by Khreathor is useful for blockout and prototyping.
  * [Quake101 WAD](https://www.quaddicted.com/files/wads/quakewad.zip) contains all the Quake textures in one collection, or you can just download [the textures used for each map](http://www.quaketastic.com/files/texture_wads/id1_wads_per_map_v3.zip) if you want to stay strictly within a traditional theme.
  * [Knave](https://www.quaddicted.com/webarchive/kell.quaddicted.com/q1textures.html) is a medieval library themed texture set by Kell
  * [Makkon](https://www.slipseer.com/index.php?resources/makkon-textures.28/) is the current most-popular texture set used in community Quake maps today

Texture WAD archives
  * [Quaddicted WAD archive](https://www.quaddicted.com/files/wads/) contains many .WADs but it's somewhat unorganized.
  * [Quaketastic](https://www.quaketastic.com/?dir=files/texture_wads) has a similar pile of unorganized WAD files
  * [Slipseer](https://www.slipseer.com/index.php?resources/categories/texture-wads.6/) has a small but growing archive of better organized WAD files

### WAD Tools
  * The most common WAD creating / editing tools are [TexMex](https://quakewiki.org/wiki/TexMex) and [Wally](https://github.com/Ty-Matthews-VisualStudio/Wally), which can browse WADs and convert textures for you easily.
  * If you are going to modify WADs frequently, you can automate the WAD building process via batch processing via command line interface (CLI) with [qpakman](https://github.com/bunder/qpakman).
  * Use TexMex or [BSP2WAD](https://www.quaketerminus.com/tools.shtml) to extract textures from a compiled .BSP map file
  * Palletizing textures to fit Quake's fixed 256 color palette is tricky, because some of the colors are reserved as "fullbright" colors. You may also need EricW's tool ["defullbright"](https://github.com/ericwa/defullbright) to remove these fullbright pixels.

### Skyboxes
Quake has two different sky systems. The original 1996 sky system is a two panel texture parallaxed over itself. Newer Quake engines support a more standard cubemap-style skybox made of 6 static .TGA textures, each corresponding to one side of the skybox.
  * [https://www.quaddicted.com/webarchive/kell.quaddicted.com/skyboxes.html](https://www.quaddicted.com/webarchive/kell.quaddicted.com/skyboxes.html)
  * [https://lvlworld.com/review/Quake%203%20Arena%20skybox%20collection](https://lvlworld.com/review/Quake%203%20Arena%20skybox%20collection)
  * [http://www.simonoc.com/pages/artwork.htm](http://www.simonoc.com/pages/artwork.htm)
  * [https://www.slipseer.com/index.php?resources/makkon-skyboxes.139/](https://www.slipseer.com/index.php?resources/makkon-skyboxes.139/)

## Mods / dev kits

Mods add new functionality and features for mappers to use in their levels. Listed below are common Quake mods and toolkits used by single player Quake mappers.

When you release your map(s) or mod, bundle the core mod files with your maps to make a self-contained .ZIP with no external dependencies. For example: if you make a mod with Copper then you should include the Copper mod files in the ZIP. Big mods include slimmed-down "dev kits" you can use, which have just the core mod files.

### Arcane Dimensions
[Arcane Dimensions](https://www.moddb.com/mods/arcane-dimensions) is a popular recent mod / toolkit that adds many new monsters and features.
  1. install the latest version of Arcane Dimensions ([v1.81](https://www.quaddicted.com/reviews/ad_v1_80p1final.html) as of January 2022)
  2. add the /ad/ mod folder and ad_1_8.fgd in your map editor
  3. read the included ad_v1_80_documentation.txt for info and advice
  4. open the [example test maps](https://www.quaddicted.com/filebase/ad_v1_80testmaps.zip) in an editor to learn how to use the new systems
  5. if you want to make your own mod based on AD, get the slimmed-down dev kit instead
     * the [Arcane Dimensions QuakeC source code is available on GitHub](https://github.com/SimsOCallaghan/ArcaneDimensions)

### Alkaline
[Alkaline](https://alkalinequake.wordpress.com/) is a recent "base" themed mod / toolkit that adds sci-fi themed monsters and weapons.
  1. install [latest version of Alkaline](https://alkalinequake.wordpress.com/) (minimal dev kit available)
  2. add the /alkaline/ mod folder and alkaline.fgd in your map editor
  3. read the included docs.html Alkaline mapping manual

### Copper
[Copper](http://lunaran.com/copper/) is a minimalist "refinement" mod that rebalances vanilla Quake gameplay and adds quality-of-life features for mappers. It is good for a "vanilla+" feel without vanilla bugs.
  1. install [latest version of Copper](http://lunaran.com/copper/download/)
  2. add the /copper/ mod folder and copper.fgd in your map editor
  3. read the [official Copper - Mapping notes](http://lunaran.com/copper/mapping/) for info and advice

### Progs_dump
[Progs_dump](https://www.quaketastic.com/files/single_player/mods/progs_dump_devkit_v200.zip) is a recent dev kit mod that adds new mapper features, but doesn't add any new monsters or weapons, it's still basically the same old vanilla Quake gameplay.
However, because it exposes so much functionality, it's possible for mappers to add some new game features without coding in QuakeC.
  * [progs_dump_manual_200.pdf](https://www.quaketastic.com/files/single_player/mods/progs_dump_manual_200.pdf)
  * [official progs_dump video tutorial series](https://www.youtube.com/playlist?list=PLgDKRPte5Y0AxvsTeUMfLTo6zcyuPD8QU)
  * [progs_dump QuakeC source code is available on GitHub](https://github.com/dumptruckDS/progs_dump_qc)

### Horde mode (2021 re-release)
To map for the new "Horde" mode added in the Quake 2021 re-release:
  1. download the special Horde mode .FGD file and load it into your map editor
  2. in the editor, add a single horde_manager entity, this is the brain of horde mode
  3. in the editor, add info_monster_start entities for where you want monsters to show up. You can also toggle a info_monster_start, which lets you do progression stuff.

See the example Horde mode .MAP source file for usage:

## Modeling
To make custom monsters, weapons, items, or props, you must export a 3D model.
For a list of 3D art tools, see [Tools](../tools.md#3d-art-tools).

The original Quake models are stored in .MDL files in a sub-folder called /progs/ . The MDL format reflects the memory limits of 1996 PCs:
  * Max triangles: 2048; max vertices: 1024
  * Textures: 8-bit palettized; max UVs: 1024
  * Max vertex animation frames: 256 at 10 FPS
For more info on MDL file format and parsing, see [Quake MDL file format spec](./formats/mdl.md).

The 2021 re-release, as well as more recent fan engines, have added [MD5 (Doom 3 format)](https://modwiki.dhewm3.org/MD5_(file_format)) much more modern file support with much higher memory limits and skeletal animation support.
  * Model data stored in .md5mesh file
  * Animations stored in .md5anim file; can load multiple .md5anim files for one model
  * Textures are .tga, bind with .mtr material definition file
  * works in 2021 re-release engine ("KexQuake"), Quakespasm-Spiked, and FTE

### Quake MDL
  * Get the [Quake MDL importer / exporter for Blender v2.8+](https://bitbucket.org/khreathor/mdl-for-blender/wiki/Home) by Taniwha, Khreathor, and Jazzmickle.
      * [installation](https://bitbucket.org/khreathor/mdl-for-blender/wiki/Installation)
      * [scene setup](https://bitbucket.org/khreathor/mdl-for-blender/wiki/Scene%20Setup)
      * [material setup](https://bitbucket.org/khreathor/mdl-for-blender/wiki/Materials)
      * [animation notes](https://bitbucket.org/khreathor/mdl-for-blender/wiki/Animations)
      * ["MDL for Blender 2.8 - Common Problems, Quirks, and Solutions" (11:03)](https://www.youtube.com/watch?v=nZC-G9Tz6OM) by Fairweather
  * Fairweather has made some great beginner video tutorials on using Blender to model for Quake, no prior Blender or 3D experience required:
      * [Modeling for Quake - Part 1 - Interface and Basic Navigation (8m 44s)](https://www.youtube.com/watch?v=oSH03YZq2EA)
      * [Modeling for Quake - Part 2 - Poly Modeling Basics (15m 10s)](https://www.youtube.com/watch?v=aMj-pKcCVAI)
      * [Modeling for Quake - Part 3 - Creating the Mesh (12m 27s)](https://www.youtube.com/watch?v=AigfWLsog60)
      * [Modeling for Quake - Part 4 - UV Mapping (20m 04s)](https://www.youtube.com/watch?v=VAVUiRm3h1I)
      * [Modeling for Quake - Part 5 - Texturing and Exporting (11m 56s)](https://www.youtube.com/watch?v=_t_SY6JnTnA)

### Quake MD5
  * Get the [MD5 Importer/Exporter for Blender 2.80+](https://github.com/KozGit/Blender-2.8-MD5-import-export-addon) by KozGit.
  * read the documentation thoroughly, it's a little complicated
  * community is still figuring out best practices / pipeline... ask questions and shares notes in QM Discord #modeling-and-texturing

## Coding
Quake game code is written in a special programming language called QuakeC. It has many historical quirks and it can be tricky to learn, but once you figure it out, it's fun.

QuakeC tutorials and documentation
  * [http://www.cataboligne.org/extra/qcmanual.html](http://www.cataboligne.org/extra/qcmanual.html)
  * [http://pages.cs.wisc.edu/~jeremyp/quake/quakec/quakec.pdf](http://pages.cs.wisc.edu/~jeremyp/quake/quakec/quakec.pdf)
  * [http://www.insideqc.com/qctut/](http://www.insideqc.com/qctut/)
  * [https://quakewiki.org/wiki/QuakeC_basics](https://quakewiki.org/wiki/QuakeC_basics)
  * [https://quakewiki.org/wiki/QuakeC_tutorials](https://quakewiki.org/wiki/QuakeC_tutorials)

Example QuakeC projects
  * "clean and fixed" original Quake v1.06 source code with bug fixes: [https://github.com/Jason2Brownlee/CleanFixedQuakeC](https://github.com/Jason2Brownlee/CleanFixedQuakeC)
      * useful as a base for a vanilla style mod
  * progs_dump mapping toolkit source code: [https://github.com/dumptruckDS/progs_dump_qc/](https://github.com/dumptruckDS/progs_dump_qc/)
  * official 2021 re-release source code: [https://github.com/id-Software/quake-rerelease-qc](https://github.com/id-Software/quake-rerelease-qc)

QuakeC tools
  * There's a [VS Code QuakeC extension](https://github.com/joshuaskelly/vscode-quakec) by Joshua Skelton.
  * FTEQCC is probably the most modern compiler available, with plenty of compilation options and enhancements. You can choose between GUI version and a command line version:
      * [FTEQCC GUI (Win64)](https://sourceforge.net/projects/fteqw/files/FTEQCC/fteqccgui64.exe/download)
      * [FTEQCC (Win64)](https://sourceforge.net/projects/fteqw/files/FTEQCC/win64-fteqcc.exe/download)
      * [More download options](https://sourceforge.net/projects/fteqw/files/FTEQCC/)
      * [FTEQCC site with all downloads and documentation](http://fte.triptohell.info/moodles/fteqcc/)
