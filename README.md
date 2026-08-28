# Ultron

Ultron is a standalone living AI rival for Gen1Recomp/Gen2Recomp games. It does
**not require The World**. If The World is installed, Ultron detects it only for
optional integration such as sharing the existing AI-rival news ticker.

## Core behaviour

- Exactly one persistent rival, permanently named **Ultron**.
- Red/Blue and Gold/Silver/Crystal: Ultron takes the third unused canonical
  starter after the player and the normal rival. Yellow: Ultron starts with
  Clefairy.
- Ultron does not participate in The World's opening gauntlet.
- Ultron owns his own money, bag, Poké Balls, TMs/HMs, party and PC boxes.
- Ultron physically traverses collision cells and real map seams/warps. The
  off-screen simulator advances the same physical route rather than granting
  destination teleports.
- Campaign travel resolves undefeated trainers on the maps Ultron crosses; when
  trainer coordinates are available, he walks adjacent before the battle.
- Blackout is the sole normal relocation exception: like the player, Ultron
  returns to the last Pokémon Center he actually visited, or the player's home
  before his first Center visit.
- Ultron catches Pokémon, trains, evolves, earns badges, challenges the League,
  shops, heals and can periodically challenge the player when both occupy the
  same map.
- Direct battles trust Ultron's live NPC when he is visibly beside the player,
  even if an older saved route snapshot has not caught up yet.
- Player battles use real two-way prize money. The loser pays from their own
  purse; Ultron also drops money when a trainer or wild battle blacks him out.
- Ultron's badges and campaign state are private. He never advances the
  player's story flags and never borrows the player's flags to cross a gate.
  Field obstacles still require an owned HM taught to an active Pokemon.
- Competitive preparation uses the bundled offline Gen 1/Gen 2 Smogon snapshot,
  opponent memory, counters, synergy, coverage, items and legal moves.
- Gen 1 and Gen 2 guide knowledge gives Ultron Gym-specific preparation goals.
  For example, before Whitney he seeks a legitimate Fighting, Rock, Ghost or
  status answer to Miltank rather than receiving a counter for free.
- Species knowledge is rebuilt from every live Pokemon registry. Mod-added and
  later-generation Pokemon on the current route can therefore be encountered,
  caught, trained and evolved using their registered stats, learnsets,
  evolution methods and TM/HM compatibility.
- Fishing encounters are read from the live encounter tables. When installed
  systems expose supported AI entry points, Ultron can also use Bug-Catching
  Contests, Safari Zones, Wonder Trade and Mystery Gift.
- All 46 imported World rival personality profiles are fused into Ultron's one
  persistent personality.
- The player can type messages to Ultron. His compact offline language system
  grounds replies in battle history, location, badges, catches, motivation and
  recent conversation memory.
- Training data can be imported through the game client and exported through a client
  Save-As flow without copying another player's party, badges, money, inventory or
  personal chat history. Imported collective knowledge is absorbed into Ultron's persistent user/save data outside the mod directory, so replacing the mod during an
  update does not erase it.

## Rivalry, legacy and collective learning

Ultron now builds a persistent career history around the player rather than treating
each rematch as an isolated encounter. Rivalry advances through named stages based
on repeated battles, results, Champion history and conversation tone. Every player
battle is archived in a bounded battle notebook with location and known team data.

After enough real service, one Pokemon can become Ultron's permanent signature
partner. The choice emerges from actual team history instead of a predefined species,
and the partner receives no artificial stat boost. It is simply protected from
ordinary voluntary PC rotation and remains Ultron's defining ace. Pokemon that build
strong personal bonds can now receive a nickname chosen by Ultron. The nickname is
stored on that individual Pokemon, survives evolution and PC movement, and is not
rerolled on every load.

Every League-winning team is preserved in Ultron's personal Hall of Fame. Once he
has reached Champion status he also chooses a persistent post-Champion objective,
such as perfecting his team, completing the Pokedex, pursuing legendaries, defending
an unbeaten reign or solving the player's team.

Imported community training data now carries provenance inside Ultron's save.
Species, move, lead, player-level and observed-exit evidence remembers how many independent Ultron sources
support it, and collective team planning ranks higher-confidence consensus ahead of
weak one-off observations. Portable exports can pass confirmed dungeon exits and
battle knowledge onward without granting progress, levels, Pokémon or items.

## Ultron chooses his own appearance

On first activation, Ultron selects one safe overworld trainer sprite from the
live game's compatible walker pool using his own persistent seed. The player does
not choose it. That sprite is then locked for the entire save. Visual replacement
mods may still replace the artwork behind the logical sprite id.


## Start menu and configurable Ultron rules

The normal game Start menu now contains a dedicated **ULTRON** section. It gives
quick access to status/party information, **Thoughts**, **Knowledge**, settings,
training-data import/export, message input, the latest news update and Ultron achievements. **Thoughts** explains his current goal, destination, rematch readiness, navigation pressure and the evidence behind his player-team model. **Knowledge** lists learned route exits with confidence and provenance, observed battles and collective sources. The deeper in-world
Ultron interaction menu remains available when you physically meet him.

Ultron's saved standalone settings currently include:

- **Catch Legendaries**: when off, Ultron can research or witness legendary Pokemon
  but cannot select one as a catch target or catch one from a legal encounter pool.
- **Forgettable HMs**: when on, Ultron may optimise an HM move away and later reteach
  the owned HM when physical field travel requires it.
- **Reusable TMs**: when on, an owned TM remains available after teaching it.
- **Periodic Challenges**, **News Ticker**, **Name Tag**, **Watch Player Battles**, and
  **Daily Routines** control optional rivalry/presentation behaviours.
- **Nickname Partners** allows Ultron to give a personal nickname to a Pokemon only
  after a sufficiently strong bond or long service history develops.

These options do not disable Ultron's identity, economy, physical travel, blackout
rules, trainer/Gym progression or League journey. Existing saves migrate with the
old behaviour preserved as the default.


## Client-managed training exchange

**Import Training Data** opens the game/client file picker. The selected package is
validated, merged into Ultron's knowledge, and then lives in the normal persistent
Ultron save/user-data state. The imported package is not copied into `mods/ultron`, so
updating or replacing the mod directory cannot wipe the learned knowledge.

On desktop, **Export Training Data** opens a native Save-As dialog and writes the
training package to the exact location selected by the player. Android/iOS import uses
Gen1Recomp's engine-owned system document picker. Current mobile builds do not expose a
generic writable Save-As bridge to sandboxed mods, so Ultron refuses to pretend a fixed
mod-folder export is user-selected; a compatible client Save-As bridge can be adopted
when the host exposes one.

## Achievements

Ultron now keeps his own persistent achievement record. The first set includes
First Blood, Not Again, Signature Bond, Machine Champion, Cartographer, Collective
Mind and Legend Thief. They are derived from real saved history rather than debug
flags, and new unlocks can be reported through Ultron's news system.

## News ticker

Ultron has his own scrolling AI-rival news ticker. It reports important current
updates such as badges, catches, training, player battles, supply runs and
blackouts. When The World is also installed and exposes its rival news manager,
Ultron submits headlines to that ticker and suppresses the duplicate Ultron bar.

## Partner legacy and rematch memory

Ultron now tracks each Pokemon as an individual teammate using a persistent internal bond ID. Two Pokemon of the same species therefore keep separate histories. Battle service, trainer wins, Gym wins, player wins, League wins, comeback rematches and Hall of Fame appearances build a partner legacy without changing battle stats.

Long-serving partners become Trusted Partners, Veterans, Hall of Famers and eventually Ultron Legends. Veterans are less likely to be voluntarily boxed, and a partner that has already helped defeat the player receives a modest team-selection preference during an anti-player rematch build. The signature partner is locked to the individual bond ID rather than merely the species, so evolution and duplicate species cannot move the signature to the wrong Pokemon.

The Start menu's **ULTRON** section includes **PARTNER LEGACY**, showing the strongest individual histories, comeback wins and Hall of Fame lineage.

## Installation

1. Download `Ultron_v1.8.1.zip` from the GitHub release or `dist/`.
2. Install/extract it as the `ultron` mod directory so `manifest.json` and
   `main.lua` are at the mod root.
3. Start Red, Blue, Yellow, Gold, Silver or Crystal.
4. Ultron remains dormant until the player's starter is committed, then begins
   his own campaign.

## Compatibility

The World is optional. When both are present, World settings may inform canonical
starter compatibility and the two mods share one ticker where supported, but
Ultron's AI engine, save state, movement, economy, battle simulation, navigation,
competitive data and chat systems remain local to Ultron.

## Release

Current release: **v1.8.1**. See [CHANGELOG.md](CHANGELOG.md) and
[docs/VALIDATION.md](docs/VALIDATION.md).


## Determination and honest rematches

A loss to the player raises Ultron's temporary Determination. After the normal player-style blackout return and heal, Ultron resumes his physical journey. If he has learned enough from the battle, he can walk to a real Pokemon Center and reorganise his own party/PC/TMs into a legal counter-team. He never reads unrevealed player Pokemon or hidden moves. Determination also shortens later same-map challenge cadence without creating Pokemon, money, levels, moves or items.

## Colosseum Inspired UI compatibility

`colosseum_ui_overhaul` is optional. When present, Ultron keeps its own gameplay logic but renders its attached name tag/news after the Colosseum HUD layer. `BATTLE ME NOW` is kept at the top of the direct interaction list for the overhaul's shorter hanging menu viewport.

## Partner Chronicle

Major wins become partner memories. Individual Pokemon build trust against opponent contexts such as the player, Gyms, League and title defences. The Start-menu Ultron section exposes Partner Chronicle and Hall of Fame history; trust can modestly influence voluntary team recall but never battle stats.
