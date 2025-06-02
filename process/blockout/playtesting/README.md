# Playtesting

How to run a playtest, and then collect / analyze data

A playtest is when someone plays your level, and you watch whether your level works or not.

Playtesting is a foundational skill and process in game design. You should do it.

## Why playtest?

Playtests are when you witness whether your level is "fun" or boring, clear or confusing, pleasant or annoying. If players hate your level, you should deal with that problem as soon as possible. "Playtest early and often."

Level design takes a long time, and it is natural to lose motivation during a project. Playtesting with someone else can boost your energy when you see someone else enjoying your terrible broken half-broken map, despite your misgivings.

The commercial game industry takes playtesting so seriously that they perform many phases of testing like user research, QA, test markets, usability, certification, etc. The biggest game companies even run their own dedicated playtesting labs.

## Playtest formats

Each playtest has a different purpose, depending on the audience.
  * Self-playtest: you test your own level.
	  * You should playtest your level yourself every day, as part of the design process
	  * Good for catching obvious problems (does the level load? is the doorway wide enough?)
  * Critique: someone else (usually a fellow game dev) playtests your level and gives you knowledgeable feedback afterward. You can even have a conversation to brainstorm how to solve the problems.
	  * Ideally, do this after every phase: after layout, blockout, scripting, and art pass, etc.
	  * This is where a lot of learning and collaboration happens, very common in workplace
	  * Good for getting help on ["wicked problems"](https://en.wikipedia.org/wiki/Wicked_problem) -- problems that are so complex that you can't even describe the problem, much less solve it
  * Public playtest: someone else (ideally a "normal person" / member of the public, and not a developer) playtests the level.
	  * Watching their behavior is more important than their feedback
	  * Very important for catching hidden problems ("unknown unknowns")
	  * But normies have a hard time playtesting blockouts, you'll likely have to art pass first
	  * "Blind" playtest: a public playtest but with minimal guidance or prompting; pretend they are playing the level by themselves, alone, and see what they do

## How to find playtesters
  * Critiques: join an online [level design community](../../../appendix/communities.md), ideally a forum or Discord with specific experience in the genre or game engine.
	  * If possible, try to do an in-person playtest. See if there's a local [International Game Developers Association (IGDA) chapter](https://igda.org/) and/or indie meetup.
	  * You need people with enough game design experience to contextualize their feedback appropriately -- people who know how to look past unfinished systems, obvious bugs, or placeholder art, and get to the real problems at the heart of the design.
  * Public playtests: put your level in front of friends or family members, who are often socially / emotionally obligated to engage with your interests.

## How to run a playtest

There are many ways to run a playtest session.

Below is a general process for an in-person public playtest:

### 1. Prepare for playtest

Before you playtest, you should figure out what you're testing! Treat it like a science experiment -- form a hypothesis and design a procedure.

Here's a basic playtest prep checklist:
  * (on) [ ] Scope: How much of the game / level are you testing? How long will it take? (example: "the first half of level 2, for 15 minutes max")
  * (on) [ ] Focus: Which parts are most important to test? What are your biggest questions? (e.g. "is the level exit clear enough? is the boss too difficult?")
  * (on) [ ] Briefing: What instructions will you give to the playtester? Any content warnings? (e.g. "use WASD to move, but don't press Space, I haven't fixed the jump yet... oh and the game has spiders, are you OK with spiders?")
  * (on) [ ] Data: What data are you collecting? How will you collect it? (e.g. use stopwatch app to time how long it takes for them to reach boss #1)
  * (on) [ ] Notes: Are you taking notes / recording observations? How, where? (e.g. write notes in notebook with a pen... oh no I forgot to bring a pen!...)

### 2. Brief playtester

Briefly introduce the concept and how long the playtest session will run, set some basic expectations to respect the playtester's time and energy. If the playtest session may contain jump scares, spiders or insects, flashing or flickering lights, sexual content, or graphic/explicit violence, then give a content warning and get the player's informed consent.

You can also tell the playtester what you want feedback on, and set some basic boundaries and focus for the playtest. A more specific briefing is very helpful if your playtester is a fellow designer, so they can tailor their feedback.

Example briefings:
  * "use WASD and mouse... have fun"
  * "I'm looking for combat ideas, tell me if the encounters are any good"
  * "I haven't art passed the level yet so just focus on layout, these are all placeholders"
  * "try to use the double jump a lot, I want to see if it works well for this level"
  * "the layout is final and we can't change it for budget reasons, so please only give me feedback on enemy placement and pickups"

But keep it brief. Don't over-brief and don't dwell too much on disclaimers, especially if you're having other developers playtest. As designers we often feel insecure or anxious about how our work will be received, but We understand your levels will be unfinished or work-in-progress, with placeholder assets and bugs everywhere.

### 3. Observe playtest / collect telemetry

Most of the time should be spent watching the screen, taking notes about player behavior, reactions, or anything that needs fixing. Make sure to watch from a short distance behind the playtester(s), don’t just breathe over their shoulder.

Feel free to ask brief clarifying questions about the playtester's behavior or thought process, but resist the urge to interrupt the playtest to apologize or explain. Whenever the playtest goes wrong, let that discomfort and anxiety stew in your mind for a little while. However, if the playtester is definitely stuck or if the level is clearly just broken, then go ahead and intervene.

If it is not an in-person playtest, then ask the tester to record their screen and send a private link to the video upload. Or better yet, the playtester can broadcast a private live stream and take questions via chat or voice. For multiplayer maps, it is best to ask an existing player group, server, or clan to play on the map and allow observers.

#### Collecting data / telemetry

Track basic stats such as play time, deaths, win percentages, etc. Most of this stat collection does not require any special plugins or tools, just attentive note-taking.

Some games can automatically aggregate player data and visualize patterns, especially for multiplayer maps. Do players use the shotgun too often on a map intended for snipers, or are too many players dying outside the spawn room?

Telemetry is automatically collected data sent to a stats server that can track player behavior and display the data in a table / spreadsheet. Types of telemetry include:
  * [Combat](../../combat/) [Data tables with stats for most common weapon, progression, or gear](https://twitter.com/MonsterclipRSPN/status/1268371601348685826)
  * Heatmaps, top-down visualizations of where players frequently move, earn points, score kills, or die.

(TODO: heatmap example)

### 4. Debrief playtester

Ask for feedback and debrief the playtester.

Have a few survey questions ready for the playtester. You could ask comprehension questions ("Did you notice the orange light above the door? What do you think it meant?") or ask for more subjective opinions ("Did the boss fight feel easy or difficult?)

Be kind and respectful to your playtesters even if they're giving you feedback that you don't necessarily want to hear. If someone offers suggestions in good faith, smile and take it with grace no matter what. The suggestion itself might be a poor solution to a design problem, but the reason for the suggestion -- and the issue it highlights -- is almost always real and valid.

But also remember, the playtest session is not for the tester's benefit. If the playtester has a harmful attitude or gives abusive feedback, especially at an in-person playtest session, then you can totally just end the playtest and ask them to stop playing or talking.

### 5. Analyze playtest data

After the playtest, you need to figure out what the heck happened and what you're going to do about it.
> "We do a lot of playtesting at our studio, and we have very good telemetry tools for recording data from the playtest that we can analyze after the fact.
>
> This telemetry [pictured below] is from a pre-release 20 player playtest. [...] The bottom numbers show different armor sets on each row, but different days from left to right. These let me see patterns in terms of popularity of gear, where in the game it's popular, how long players stay on the same gear, when they switch... and I use these charts to identify clumping that might be unhealthy.
>
> ... At the start of the game there's not many armors available, so everybody is using one of the first three [...] But what's happening here? A lot of people are sticking on this Alfheim armor. Is that something I should look into? (Spoiler, we did nerf the Alfheim armor...) So it's about looking at the data to reinforce your expectations, to have a healthy spread."
> -- Rob Meyer, ["Reckoning With Fate: Combat Design at the Scale of Ragnarok" (2023) (YouTube)](https://youtu.be/6iTBqcBv5QA?t=1490)

## How to be a useful playtester for someone else

The goal of a playtest is to help the designer predict whether their game works for their audience. It's not about the player's performance. Watch out for these common tendencies:
  * New to games / game dev: too "nice", doesn't verbalize problems or frustrations
  * Gamers: too nitpicky, exaggerates small problems, performs too much

### Best practices for critiquing a fellow designer

#### Briefing
  1. If you're unfamiliar with the genre or design style, say so.
  2. Ask "what do you want feedback on?"
  3. Ask "is there anything I should know before I start?"

#### Playing
  * Think aloud, try to say what you're thinking constantly. No one can read your mind. At the same time, don't be offended if the dev ignores what you say.
  * Don't nitpick unless the dev asks you to. If you break the game, tell the dev and then move on. Unless the dev asks you to repeat the game breaker for analysis, don't continue to break the game in the same way -- don't seek to embarrass or humiliate the dev.
  * Be honest with expressing your emotions. If you like something, say so. If something confuses or surprises you, say so.

#### Debriefing
  * Say what was memorable to you, positive or negative.
  * Ask questions about intent and planned solutions, make it into a conversation.

## Example playtesting processes

### Playtesting at Valve

At Valve Software, level designers playtest every Friday across a variety of different playtester types (fellow designers, non-designers, non-dev staff, sometimes "open" public testing). Playtesting is fundamental to their design process and drives many of their decisions every week. Valve level designer Phil Co discusses their process:
> On a typical project at Valve, the cabal (smaller subset of the team which consists of 6-8 people) works on a weekly cycle. Every Friday, we would playtest the section of the game that we're responsible for with someone from outside the team (even outside of the company depending on how far along we are). Everything we do during the week is focused on that Friday playtest. [emphasis added]
>
> On Mondays, we have meetings where we decide what the goals are for the playtest and who is responsible for each task. [...] You might have to prototype a new mechanic which would involve a programmer, or you might have to perform an art pass of your level which would involve an artist.
>
> We learn everything from playtests, however, so we might have too much of one particular gameplay and the playtester suffers from fatigue. We correct this issue in multiple ways.
>
> For example, in [Half-Life 2] Episode 2, where the player gets the car on the bridge, we decided to add a combat high moment. Most of the level up to getting the car is combat but with just a few enemies at a time. It was made to be sort of a funhouse of zombies. We added the building where you pop the roof panels off so that Alyx can help you with the sniper rifle based on our playtesting feedback.
> -- Phil Co, from ["Building the levels: An exclusive interview with Valve level designer Phil Co" (Interlopers.net)](https://www.interlopers.net/articles/phil-co-interview), circa 2013

## Player data and analytics

## Further reading on playtesting
  * [GDC 2009: "Valve's Approach to Playtesting"](https://www.youtube.com/watch?v=Ij2nmt3EuJY) ([slides via gdcvault.com](https://www.gdcvault.com/play/1566/Valve-s-Approach-to-Playtesting), free) by Mike Ambinder is the foundational industry text, covering playtesting fundamentals. Ambinder outlines the core bread and butter "direct observation" and iteration process at Valve, which is definitely the most helpful thing for the average level designer. There are two important historical notes: (1) data science / telemetry is now much more important in the industry, (2) biometrics like heartrate monitoring / brain wave recording / eye gaze tracking is rare in the industry, and other studios think it's "more trouble than it's worth" for level design. (Ambinder is an experimental psychologist, so of course he favors biometrics.)
  * [GDC 2017: "Playtesting - Avoiding Evil Data"](https://www.gdcvault.com/play/1024401/Playtesting-Avoiding-Evil-Data) ([slide PDF](https://ubm-twvideo01.s3.amazonaws.com/o1/vault/gdc2017/Presentations/deJongh_PlaytestingAvoidingEvilData.pdf), [video via YouTube](https://www.youtube.com/watch?v=6EUeYu0aPn4)) by Adriaan de Jongh covers modern playtesting practices, with practical tips for how and when to run playtests. De Jongh argues "evil data" is "playtest results that are distracting, unclear, or misleading", so it's important to focus on frequent direct observation with a variety of playtester demographics. Don't bother with forms / surveys / questionnaires, instead send a template email to remote playtesters to record their screen and voice with [Open Broadcaster Software (OBS)](https://obsproject.com/) and then upload an unlisted video.
