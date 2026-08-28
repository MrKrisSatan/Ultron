# Ultron v2.1.0

Ultron is a standalone living-rival mod for Gen1Recomp and Gen2Recomp. A new save can contain **one to four autonomous robot trainers**, each pursuing the Pokémon League alongside the player rather than waiting on a route as a conventional NPC.

The World is not required. When installed, it is used only through supported optional integrations.

## Choose your robot roster in Oak's introduction

After the player finishes entering their name, Oak asks how many robot rivals should share the save. This choice is part of Oak's normal introduction in both supported generations:

- **Gen 1:** immediately after Oak confirms the player's name.
- **Gen 2:** immediately after the player-name screen.
- Available answers are **one, two, three or four**.
- The selection is permanent for that save and is stored before the robots begin their journeys.
- Existing saves remain compatible and retain their current roster and progress.

## Up to four independent robot rivals

| Slot | Robot | Starting character | Developing voice |
|---:|---|---|---|
| 1 | **Ultron** | Analytical, competitive and confident | Becomes more calculating after defeats and bolder after victories |
| 2 | **Data** | Precise, inquisitive and evidence-led | Talks in hypotheses, corrections and observed patterns |
| 3 | **R2-D2** | Daring, loyal and mischievous | Develops a spirited, humorous rivalry with the player |
| 4 | **WALL-E** | Gentle, persistent and protective | Expresses growing courage, attachment and sporting respect |

Every robot has its own party, PC boxes, money, inventory, Poké Balls, TMs, HMs, badges, objectives, map position, memories, relationships and battle record. They do not share artificial progress.

The robots can meet, battle one another, exchange observed information, trade eligible duplicate Pokémon and develop friendships, mentorships, competitive respect, rivalries, feuds and arch-rivalries. A robot falling behind its peers receives motivation to catch and train legitimately rather than free levels or Pokémon.

## Thoughts before player battles

Before a robot attacks or begins a **Battle Me Now** challenge, it speaks through the game's standard text box. The battle starts only after the player closes that text.

These are not fixed trainer quotes. Each robot keeps a persistent voice profile shaped by its history against the player. Wins can increase confidence, losses encourage analysis and adaptation, repeated meetings develop familiarity, and long rivalries produce more established speech. The result is a distinct voice for Ultron, Data, R2-D2 and WALL-E that changes over the life of the save.

## Legitimate autonomous progression

Each robot:

- Physically travels through collision cells, map seams, doors, caves and warps.
- Catches Pokémon available through the live encounter registry, including compatible mod-added species.
- Trains and evolves Pokémon through their registered legal requirements.
- Buys supplies, heals, earns and loses money, and maintains its own Bag and PC.
- Challenges trainers, Gym Leaders, the Elite Four and the Champion.
- Returns to its last visited Pokémon Center—or home before visiting one—after a blackout.
- Uses private campaign state and never advances or borrows the player's story flags.
- Must own and teach required HMs before using them to cross field obstacles.
- Uses bundled Gen 1 and Gen 2 guide knowledge to prepare for major fights, including finding a legitimate answer to Whitney's Miltank.
- Builds teams from live species data, learnsets, evolutions, TM/HM compatibility and bundled offline competitive knowledge.
- Can use supported fishing, Bug-Catching Contest, Safari Zone, Wonder Trade and Mystery Gift integrations when the current game or another mod exposes them.

Player battles carry real stakes. The loser pays prize money from their own funds. A robot also loses money when trainer or wild battles cause it to black out.

## Learning from the player and one another

Robots observe revealed Pokémon, levels, moves and contiguous player travel. They can learn a dungeon exit by following the player and can share confirmed route or battle knowledge with the other robots.

Direct observations remain more trusted than imported or second-hand information. If a robot knows the player's team substantially outlevels its own, it prioritises catching, training and team preparation before seeking another rematch.

Portable training-data import and export shares confirmed strategic knowledge without copying Pokémon, levels, badges, money, inventory, story progress or personal chat history. Imported knowledge is stored with the save data rather than inside the mod directory.

## Companions and embedded double battles

Talk to a robot on the same map and select **Accompany Me**. One robot can accompany the player at a time. While accompanied:

- Eligible wild and trainer encounters become double battles.
- The player controls only the player's Pokémon.
- The companion independently controls its own Pokémon, targets, moves, switches and items.
- Companion damage and experience persist after battle.
- Without a companion, normal battles remain single battles.

The required double-battle systems are embedded in Ultron. The standalone `double_battles` mod is therefore marked incompatible.

Neither the player nor a robot can throw a Poké Ball while two opposing Pokémon remain active. The selected player ball is returned and the battle displays: **“It's no good! It's impossible to aim at two Pokémon at once!”** Once one wild opponent faints, a companion may spend one of its own Poké Balls on a normal generation-specific capture attempt. A successful catch belongs to that robot's party or PC.

## Interaction and menus

The Start menu contains an **ULTRON** section with:

- Robot roster and active-robot selection
- Relationship network
- Status and party
- Thoughts and knowledge
- Partner legacy, chronicle and Hall of Fame
- Settings and achievements
- Training-data import and export
- Message Ultron
- Latest news

Talking to a visible robot opens that individual robot's interaction menu. Its attached nameplate follows its live overworld sprite and is hidden behind menus, text boxes, naming screens, battles and transitions.

## Configurable rules

Persistent settings include Catch Legendaries, Forgettable HMs, Reusable TMs, Periodic Challenges, News Ticker, Name Tags, Watch Player Battles, Daily Routines and Nickname Partners. Disabling presentation options does not disable physical movement, economy, blackouts or campaign progression.

## Installation

1. Download [`Ultron_v2.1.0.zip`](https://github.com/MrKrisSatan/Ultron/releases/download/v2.1.0/Ultron_v2.1.0.zip).
2. Install or extract it as the `ultron` mod directory.
3. Confirm that `manifest.json` and `main.lua` are directly inside that directory.
4. Start a new Red, Blue, Yellow, Gold, Silver or Crystal save to choose one to four robots during Oak's introduction.

Ultron remains dormant until the player's starter is committed. Existing saves migrate without teleporting an established robot to the player.

## Compatibility

- Games: Red, Blue, Yellow, Gold, Silver and Crystal through their recomp clients.
- The World: optional supported integration.
- Colosseum UI Overhaul: optional presentation compatibility.
- Standalone Double Battles: incompatible because Ultron embeds and controls the required companion-only implementation.
- Link play: protected by the mod's battle-affecting compatibility declaration.

## Release and validation

Current release: **[v2.1.0](https://github.com/MrKrisSatan/Ultron/releases/tag/v2.1.0)**.

See [CHANGELOG.md](CHANGELOG.md) for version history and [RELEASE_NOTES.md](RELEASE_NOTES.md) for the release summary.
