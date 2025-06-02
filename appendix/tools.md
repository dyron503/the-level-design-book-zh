# Tools

Links to various level editors, moddable games, engines, and art tools

This page contains several lists of links to useful tools, both ancient and modern:
  * [Moddable games (recommended)](#moddable-games-recommended). Short list of moddable games for "serious" level design, with active level design community tied closely to the game industry.
  * [Moddable games (all)](#moddable-games-all). A much longer list of known games with modding tools. For various reasons, we don't recommend using these tools.
      * But in the end, the best tool is whatever is most interesting to you.
  * We also list general [3D game engines](#3d-game-engines), [2D level editors](#2d-level-editors), [3D art tools](#3d-art-tools), [2D art tools](#2d-art-tools), and [planning tools](#planning-tools) common in the game industry.

## Moddable games (recommended)

When you mod a game, you get to re-use graphics, sounds, code, and most importantly, core game design and tuning. We strongly recommend learning level design by modding.

This is a list of recommended games with well-supported toolsets and active communities. Download the tools, build levels, ask for help, and share your work.

We generally recommend Quake and Doom since these games have large active communities, free stable multiplatform tools, and proven design.

Game | Editor | Combat | Scripting | Community
-- | -- | -- | -- | --
Quake 1 | [TrenchBroom](../appendix/tools/trenchbroom.md) ([guide](../appendix/tools/trenchbroom.md#how-to-use-trenchbroom), [video](https://www.youtube.com/watch?v=gONePWocbqA&list=PLgDKRPte5Y0AZ_K_PZbWbgBAEt5xf74aE)); see [Quake resources](./resources/quake.md) | static, [entities](../appendix/resources/quake.md#horde-mode-2021-re-release), dynamic (Horde) | visual ([entities](../appendix/resources/quake.md#arcane-dimensions)) + code ([QC](../appendix/resources/quake.md#coding)) | [QM Discord](https://discord.gg/58XqmZM), [Slipseer](https://www.slipseer.com/index.php), [Quaddicted](https://www.quaddicted.com/)
Doom | [GZDoomBuilder](http://devbuilds.drdteam.org/doombuilder2-gzdb/) / [SLADE3](http://slade.mancubus.net/) ([guide](https://eev.ee/blog/2015/12/19/you-should-make-a-doom-level-part-1/)) | static | visual ([entities](https://zdoom.org/wiki/Actor_property_flags)) + code ([ACS](https://zdoom.org/wiki/ACS)) | [Doomworld](https://www.doomworld.com/)
Half-Life 2 | [Hammer++](https://ficool2.github.io/HammerPlusPlus-Website/) ([SDK 2013 SP](https://developer.valvesoftware.com/wiki/Source_SDK_2013), [Mapbase](https://github.com/mapbase-source/source-sdk-2013/wiki)) | static / scripted | visual ([I/O](https://developer.valvesoftware.com/wiki/Inputs_and_Outputs)) | [RTSL](https://www.runthinkshootlive.com/), [MapLabs](https://discord.gg/p2c6Mfa), [TWHL](https://twhl.info/)
Counter-Strike 2 | Hammer 2 ([wiki](https://developer.valvesoftware.com/wiki/Counter-Strike_2_Workshop_Tools), [video](https://www.youtube.com/watch?v=UZxsTvPeD1M)) | multiplayer | code (VScript2?), visual (Pulse?) | [Mapcore](https://www.mapcore.org/), [Steam](https://steamcommunity.com/workshop/browse/?appid=730)
Portal 2 | [Puzzle Maker](https://developer.valvesoftware.com/wiki/Portal_2_Puzzle_Maker) (in-game) | -- | visual ([entities](https://developer.valvesoftware.com/wiki/Inputs_and_Outputs)) | [Steam](https://steamcommunity.com/app/620/workshop)
Team Fortress 2 | [Hammer++](https://ficool2.github.io/HammerPlusPlus-Website/) ([guide](https://tf2maps.net/posts/299571/)) | multiplayer | visual ([I/O](https://developer.valvesoftware.com/wiki/Inputs_and_Outputs)) | [tf2maps](https://tf2maps.net/)

Combat setup
  * Static: pre-placed enemies, arcade style, "fire and forget"
  * Scripted: pre-placed enemies with some control over AI behavior
  * Dynamic: high level "director" manages enemies automatically
  * Multiplayer: combat centers around other players

## Moddable games (all)

These moddable games are NOT part of our recommended list, for one or more reasons:
  * player or modder community has died off
  * OR the tools are too old, unsupported, broken, or painful
  * OR the tools are seen as "illegitimate" by the industry (even though the industry is wrong)

But your enthusiasm matters most. The best tool is whatever you will actually use to finish projects.

Game | Editor | Combat | Scripting | Community
-- | -- | -- | -- | --
CoD: MW (2007) | CoD Radiant | static | visual | ???
Call of Duty: Black Ops 3 | [Radiant (BO3 Mod Tools)](https://www.reddit.com/r/CODZombies/comments/58nbvq/black_ops_3_mod_tools_super_guide/) | static / dynamic (zombies) | code ([GSC](https://www.reddit.com/r/CODZombies/comments/58nbvq/black_ops_3_mod_tools_super_guide/)) | ???
Crysis 2 | [Mod SDK v1.0](https://download.cnet.com/Crysis-2-Mod-SDK-v1-0/3000-7441_4-75452927.html) | static | ??? | ???
[The Dark Mod](https://www.thedarkmod.com/) | [DarkRadiant](https://www.darkradiant.net/) ([wiki](http://wiki.thedarkmod.com/)) | static (stealth) | visual + code ([DoomScript](https://wiki.thedarkmod.com/index.php?title=Scripting_basics)) | [TDM Forums](https://forums.thedarkmod.com/index.php?/forum/54-tdm-editors-guild/)
Divinity: Original Sin 2 | Divinity Engine 2 ([guides](https://docs.larian.game/Larian_guides)) | scripted (RPG) | code ([Osiris](https://docs.larian.game/Scripting), [guide](https://docs.larian.game/Osiris_Overview)) | [Larian Forums](https://forums.larian.com/ubbthreads.php?ubb=postlist&Board=73&page=1)
Doom 3 | [DarkRadiant](https://www.darkradiant.net/) ([wiki](http://wiki.thedarkmod.com/)) | static | visual + code ([DoomScript](https://wiki.thedarkmod.com/index.php?title=Scripting_basics)) | [idtech4 Discord](https://discord.gg/d52AHfFH)
DOOM (2016) | [SnapMap](https://snapwiki.doom.com/) (in-game) | static / dynamic ([Conductor](https://snapwiki.doom.com/index.php?title=AI_Conductors)) | visual ([Logic](https://snapwiki.doom.com/index.php?title=Logic)) | [SnapHub](https://snapwiki.doom.com/index.php?title=SnapHub)
DOOM Eternal | [idStudio](https://idstudio.idsoftware.com/) ([guide](https://idstudio.idsoftware.com/category/getting-started)) | static / dynamic ([Encounter Manager](https://idstudio.idsoftware.com/gameplay/gameplay-framework/encounter-manager/create-an-encounter)) | visual ([Logic Designer](https://idstudio.idsoftware.com/gameplay/gameplay-framework/logic-designer/index)) | [official Discord](https://discord.gg/DOOM)
Fallout 4 | [Creation Kit](https://www.creationkit.com/) | static | code (Papyrus) | [NexusMods](https://www.nexusmods.com/fallout4/)
Far Cry 5 | in-game | static | visual | in-game
F.E.A.R | [FEAR SDK 1.08](https://gamebanana.com/tools/397) ([guide](https://web.archive.org/web/20170520123009/http://forums.steampowered.com/forums/showthread.php?t=1284271#post15155531)) | scripted | ??? | [Discord](https://discord.gg/9xYZyu4)
Fortnite | [Creative Mode](https://www.epicgames.com/fortnite/en-US/creative) (in-game) | multiplayer | visual ([Devices](https://fortnite.gamepedia.com/Devices)) | [Reddit](https://www.reddit.com/r/FortniteCreative/)
Gears of War | UnrealEd 3 | scripted | visual | ???
Half-Life 1 | [Valve Hammer Editor](https://twhl.info/wiki/page/Tools_and_Resources) ([guide](https://twhl.info/wiki/page/Tutorial:_In_the_Beginning_Part_1)) | static | visual ([entities](https://twhl.info/wiki/page/category:Entity_Guides+Half-Life_Entity_Guide)) | [TWHL](https://twhl.info/)
Halo Infinite | [Forge](https://www.halowaypoint.com/news/halo-infinite-forge-fundamentals#scripting) (in-game) | multiplayer | visual (nodes) | in-game
Left 4 Dead 2 | Hammer ([guide](https://developer.valvesoftware.com/wiki/Authoring_Tools/SDK_(Left_4_Dead_2))) | dynamic / multiplayer | visual ([I/O](https://developer.valvesoftware.com/wiki/Inputs_and_Outputs)) + code ([VScript](https://developer.valvesoftware.com/wiki/L4D2_Vscripts)) | [Steam](https://steamcommunity.com/app/550/workshop/)
Metro Exodus | [Exodus SDK](https://exodus-sdk.atlassian.net/wiki/spaces/ESDK/overview) | static | visual ([VS](https://exodus-sdk.atlassian.net/wiki/spaces/ESDK/pages/1714591047/VS+Editor)) | [mod.io](https://mod.io/g/exodussdk)
Minecraft | Creative Mode ([guide](https://www.reddit.com/r/Minecraft/comments/qmndk/the_gigantic_guide_for_building/)) / [Forge](https://mcforge.readthedocs.io/en/1.15.x/gettingstarted/) (in-game) | static / dynamic | visual ([Commands](https://minecraft.fandom.com/wiki/Commands)) | [Planet Minecraft](https://www.planetminecraft.com/), [CurseForge](https://www.curseforge.com/minecraft/worlds)
Prodeus | [in-game](https://www.prodeusgame.com/) ([guide](https://steamcommunity.com/app/964800/discussions/0/2846795319618738927/)) | static | visual ([entities](https://wiki.prodeus.com/index.php?title=Category:Entities)) | [official Discord](https://discord.gg/GY3gCQU)
Quadrilateral Cowboy | [in-game](https://blendogames.com/qc/) ([guide](https://steamcommunity.com/sharedfiles/filedetails/?id=701335671)) | static | ??? | [Steam forum](https://steamcommunity.com/app/240440/discussions/1)
Quake 2 | [TrenchBroom](../appendix/tools/trenchbroom.md) ([video](https://www.youtube.com/watch?v=P2bFcL32lUE)) | static | visual (entities) | [Map-Center](https://discord.gg/BhmHT2kyp2)
Quake 3 Arena | [NetRadiant-c](https://github.com/Garux/netradiant-custom) / [GtkRadiant](https://icculus.org/gtkradiant/) | multiplayer | visual (entities) | [LvL World](https://lvlworld.com/)
Quake 4 | [Q4Radiant](https://www.iddevnet.com/quake4/LevelEditor.html) | static | visual + code ([.script](https://www.iddevnet.com/quake4/ScriptFile.html)) | ???
Roblox | [Studio](https://www.roblox.com/create) ([guide](https://developer.roblox.com/en-us/learn-roblox/studio-basics)) | all | code (Lua) | [official Discord](http://discord.gg/roblox), [RobloxHelpers](https://scriptinghelpers.org/)
Shadowrun | [Shadowrun Editor](https://shadowrun-series.fandom.com/wiki/Getting_Started) ([guide](https://shadowrun-series.fandom.com/wiki/Getting_Started)) | scripted (RPG) | visual ([Gumbo](https://shadowrun-series.fandom.com/wiki/Gumbo_Script_101)) | [Steam](https://steamcommunity.com/app/346940/workshop/)
Skyrim | [Creation Kit](https://www.creationkit.com/) | static | visual ([Triggers](https://www.creationkit.com/index.php?title=Category:Triggers)) + code (Papyrus) | [NexusMods](https://www.nexusmods.com/skyrim)
Thief 1 / Thief Gold / Thief 2 | [DromEd](https://www.ttlg.com/forums/showthread.php?t=141708) ([guides](https://www.ttlg.com/forums/showthread.php?t=131800), [wiki](https://dromed.whoopdedo.org/)) | static (stealth) | visual ([Stim](https://www.ttlg.com/forums/showthread.php?t=131800#stimulus), [OSM](https://www.ttlg.com/forums/showthread.php?t=131800#scripts)) | [TTLG](https://www.ttlg.com/forums/forumdisplay.php?f=85)
Thief 3 | [T3ed](https://www.ttlg.com/forums/showthread.php?t=94005) ([guide](http://www.shadowdarkkeep.com/files/komagtutt3.htm)) | static (stealth) | visual (Actors, Triggerscript) | [TTLG](https://www.ttlg.com/forums/forumdisplay.php?f=138)
Unreal Tournament (1999) ("UT99") | UnrealED 2.1 / [227h](https://www.oldunreal.com/oldunrealpatches.html) ([guide](https://www.oldunreal.com/wiki/index.php?title=Tutorials)) | multiplayer | visual (Actors) + code ([UScript](https://www.oldunreal.com/wiki/index.php?title=Chimeric)) | [Oldunreal](https://www.oldunreal.com/), [ut99.org](https://ut99.org/)
Unreal Tournament 4 | Unreal Engine 4 ([guide](https://www.epicgames.com/unrealtournament/tutorials)) | multiplayer | visual ([Blueprint](https://docs.unrealengine.com/en-US/Engine/Blueprints/)) | [Discord](http://discord.gg/unrealtournament) (dead)

## 3D game engines

Modern all-purpose game engines almost never have good level design tools by default, so you should expect to download and install additional plugins to aid construction.

Engine | 3D tools | Scripting | Community
-- | -- | -- | --
[Unity](https://unity.com/) | [ProBuilder](https://www.procore3d.com/probuilder/), [RealtimeCSG](https://realtimecsg.com/), [SabreCSG](https://assetstore.unity.com/packages/tools/modeling/sabrecsg-level-design-tools-47418) | C#, [Visual](https://docs.unity3d.com/Packages/com.unity.visualscripting@1.9/manual/index.html), [Playmaker](https://hutonggames.com/) | [Official Unity Discord](https://discord.com/invite/unity)
[Unreal](https://www.unrealengine.com/) | [CubeGrid](https://docs.unrealengine.com/5.3/en-US/cubegrid-tool-in-unreal-engine/), [Modeling Mode](https://docs.unrealengine.com/5.0/en-US/modeling-mode/), [Mesh Tool](https://www.unrealengine.com/marketplace/en-US/product/mesh-tool) | C++, [Blueprint](https://docs.unrealengine.com/en-US/Engine/Blueprints/index.html) | [Unreal Slackers Discord](https://unrealslackers.org/)
[Godot](https://godotengine.org/) | [CSG](https://docs.godotengine.org/en/stable/tutorials/3d/csg_tools.html) | [GDScript](https://docs.godotengine.org/en/3.1/getting_started/scripting/gdscript/gdscript_basics.html), [C#](https://docs.godotengine.org/en/stable/tutorials/scripting/c_sharp/index.html) | [Godot Community](https://godotengine.org/community)

It is possible to import [TrenchBroom](../appendix/tools/trenchbroom.md) files into Godot, Unity, or Unreal. See [TrenchBroom > Compatibility](../appendix/tools/trenchbroom.md#compatibility-engine-pipeline) for recommended plugins and importers.

## 2D level editors

If your engine already has a built-in 2D level editor, then use that. But if you're using a homemade engine or web-based framework, you'll need a standalone 2D level editor.

Unlike the fragmented 3D editor ecosystem, all standalone 2D level editors are open-source, stable, and engine-agnostic with easily parsed JSON file formats. Here we generally recommend Tiled, with its many features and widespread engine support.

2D level editor | Notes
-- | --
[Sprite Shapes](https://docs.unity3d.com/Manual/class-SpriteShapeRenderer.html), [Tilemaps](https://docs.unity3d.com/Manual/class-Tilemap.html), [Tilemap Extras](https://docs.unity3d.com/Packages/com.unity.2d.tilemap.extras@latest/) | built-in Unity
[Paper2D tilemaps](https://docs.unrealengine.com/4.27/en-US/AnimatingObjects/Paper2D/TileMaps/) | built-in Unreal, are "experimental"
[TileMaps](https://docs.godotengine.org/en/stable/tutorials/2d/using_tilemaps.html) | built-in Godot; supports autotiles
[Tiled](https://www.mapeditor.org/) | most common standalone editor, [supports many engines](https://doc.mapeditor.org/en/stable/reference/support-for-tmx-maps/) (Unity, Unreal, Godot, and more)
[LDtk](https://ldtk.io/) | more recent tool, streamlined, lots of features
[Ogmo](https://ogmo-editor-3.github.io/) | not actively developed, but still simple + solid

## 3D art tools

In most cases, we don't recommend using 3D modeling tools to build levels. That said, all these tools basically do the same thing, and you should use whatever tools you like using.

We generally recommend Blender, free open source software that now rivals commercial tools. Older artists often prefer Maya or 3DS Max because they already learned it + industry pipelines are tightly coupled. But let's be clear -- Blender is basically the future, and Autodesk's days are numbered.

Tool | Notes
-- | --
[Blender](https://www.blender.org/) | free and open source; steadily getting more popular in industry with rich feature set
[Maya](https://www.autodesk.com/products/maya/overview) | common in games and film, expensive but [free for students](https://www.autodesk.com/education/free-software/featured)
[3DS Max](https://www.autodesk.com/products/3ds-max/overview) | common in games and architecture, expensive but [free for students](https://www.autodesk.com/education/free-software/featured)
[Cinema 4D](https://www.maxon.net/) | not often used in games but perfectly usable, [free for students](https://www.maxon.net/en-us/training/educational-solutions/educational-solutions/students/)
[SketchUp](https://www.sketchup.com/) | used by architects but no [topo](http://wiki.polycount.com/wiki/Topology) / [UV](http://wiki.polycount.com/wiki/Texture_Coordinates) tools, don't use it beyond [blockout](../process/blockout/) phase

## 2D art tools

Good 2D art tools are vital for drawing level layouts and diagrams, and essential for making your own graphics and textures. Some of these tools even run online in your browser for free.

Tool | Notes
-- | --
[Photoshop](https://www.adobe.com/products/photoshop) | expensive photo-editor / painter, has [student discount](https://www.adobe.com/creativecloud/buy/students.html)
[Illustrator](https://www.adobe.com/products/illustrator) | expensive, good for vector maps, has a [student discount](https://www.adobe.com/creativecloud/buy/students.html)
[Substance](https://substance3d.com/) | expensive, popular powerful texture generator tool, [free for students](https://www.substance3d.com/education/)
[Affinity](https://affinity.serif.com/en-us/photo/) | cheap Photoshop / Illustrator alternative
[Photopea](https://www.photopea.com/) | free ad-supported Photoshop clone, in-browser (!)
[Krita](https://krita.org/) | free open source Photoshop alternative
[Paint.NET](https://www.getpaint.net/) | free open source Photoshop alternative
[GIMP](https://www.gimp.org/) | free old school Photoshop alt with bad name
[Aesprite](https://www.aseprite.org/) | cheap popular pixel art painting tool
[Inkscape](https://inkscape.org/) | free open source Illustrator alternative
[Boxy SVG](https://boxy-svg.com/) | free online Illustrator alternative, runs in browser
[PureRef](https://www.pureref.com/) | free (PWYW) moodboard tool / reference image manager
[Allusion](https://allusion-app.github.io/) | free open source moodboard manager with PureRef-like drag and drop

## Planning tools

Good note-taking and writing tools can help you write design documentation, plan a project, track work tasks, and collaborate with others.

Tool | Description
-- | --
a notebook (real-life, paper) | many designers keep personal notebooks; think of it as a portable always-on browser tab
[Miro](https://miro.com/) | popular freemium service for collaborative whiteboarding / "mindmap" / planning
[Notion](https://www.notion.so/) | popular freemium service for notes, lists, wikis, documentation
[Trello](https://trello.com/) | popular freemium service for "kanban" style project planning in games
[Scrivener](https://www.literatureandlatte.com/scrivener/overview) | cheap ($50) writing tool popular among authors, rich outlining features
[TiddlyWiki](https://tiddlywiki.com/) | free open-source lightweight personal wiki that lives in a single .HTML file on your device
Google Docs | sometimes it's best to keep it simple

## To review...
  * for fundamentals, we recommend modding Quake or Doom
  * for [making 2D levels](#2d-level-editors), we recommend Tiled
  * for [general 3D art](#3d-art-tools), we recommend Blender
  * for [general 2D art](#2d-art-tools), the world still uses Photoshop
  * for [planning](#planning-tools), we recommend keeping an IRL paper notebook for personal sketches, notes, etc.
  * but anyway, you should use whatever you feel good about, because making and finishing stuff is more important than social consensus
      * the ultimate level design tool is "giving a shit"
