# Changelog

## 2.1.1

- Added explicit balanced level-5 starter plans for Data, R2-D2 and WALL-E in Red, Blue, Yellow, Gold, Silver and Crystal without duplicating the normal laboratory trio.
- Added an in-game player-to-robot trade flow requiring both trainers to be on the same map.
- Robot-to-robot and player trades now trigger genuine trade evolutions, including Gen 2 held-item requirements and consumption.
- Protected starters, Eggs, aces, signature/bonded partners and the robot's final usable party member from trade offers.
- Added a completely private Gen 2 Day-Care state for every robot; it never reads or mutates the player's party, deposited parents, Egg, breeding counters or flags.
- Robots physically visit Route 34 to deposit compatible owned parents, continue travelling while the Egg develops, return to collect it and pay their own Day-Care fee.
- Added Gen 2 Egg Group, gender, Ditto, matching-DV, base-form, hatch-cycle, inherited-DV, shared level-up move and father-side TM/HM/Egg Move rules.
- Bundled Crystal's canonical Egg Move lists and combined them with the live registry and offline Gen 2 competitive sets when selecting legitimate breeding projects.
- Bred Pokémon hatch at level 5, retain parent provenance and inherited Egg Moves, enter the robot's party or PC, and are trained through the normal progression system.
- Added private-state, compatibility, legal Egg Move, fee, parent-return and hatch regressions.

## 2.1.0

- Moved the one-to-four robot selector into Oak's standard introduction immediately after naming the player in both Gen 1 and Gen 2.
- Added a persistent developing voice profile for Ultron, Data, R2-D2 and WALL-E, shaped by player-battle wins, losses and repeated meetings.
- Every player challenge now begins with the attacking robot's current thought in the game's standard text box; the battle starts only after the text is closed.
- Completely rewrote the README around the one-to-four robot roster, independent progression, relationships, evolving dialogue, companions and double battles.

- Added same-map **ACCOMPANY ME** and **STOP ACCOMPANYING** actions for every robot personality, with one persistent companion at a time.
- Embedded the required Double Battles v0.6.1 battle, turn-order, targeting, switching, faint, experience, HUD and compatibility machinery.
- Double battles now activate only while a robot accompanies the player; ordinary play remains single-battle only.
- Companion Pokémon come from the selected robot's persistent party and are controlled exclusively by that robot.
- Once one opposing wild Pokémon has fainted, a companion with an owned Poké Ball can spend its turn making a normal generation-specific capture attempt. Successful captures join that robot's party or PC, never the player's collection.
- The player and every robot are now prevented from throwing a Poké Ball while two opposing Pokémon remain active. The player's selected ball is returned and the battle explains that aiming at two Pokémon is impossible.
- Added doubles training for focus fire, safe foe-wide attacks, ally-damaging spread avoidance, survival and personality-weighted support decisions.
- Declared the standalone `double_battles` mod incompatible to prevent two battle decorators from competing.
- Added companion persistence and double-battle decision regressions.

## 2.0.0

- Added a new-save opening selector for one to four autonomous robot rivals, capped at four.
- Added Data, R2-D2 and WALL-E with scholar, explorer and collector personalities alongside Ultron's competitive strategist identity.
- Migrated the standalone engine from one serialized rival to an independently serialized roster while preserving `engine.rival` and all existing one-Ultron saves.
- Each robot owns its own Pokémon, PC, items, money, badges, position, objectives, opponent memory, confidence and relationship bonds.
- Added multi-robot physical spawning, independent movement, attached nameplates, interaction targeting and player battle ownership.
- Added **ROBOT RIVALS** selection and **RELATIONSHIP NETWORK** pages to the Start-menu Ultron section.
- Activated the existing rival skirmish, legitimate prize transfer, team observation, counter-building, trading, Championship and relationship systems for the standalone roster.
- Added same-map knowledge exchange with source attribution and shared-journey relationship effects.
- Added rivalry pressure: agents behind a peer in badges or levels prioritise legitimate catches or training.
- Added migration, four-agent construction, selection, serialization, information exchange, relationship and motivation regressions.

## 1.8.1

- Added **Thoughts** pages to both Ultron menus, explaining his current goal, destination, rematch readiness, navigation recovery and known player level comparison.
- Added a **Knowledge** page showing learned exits, observation counts, collective sources and each displayed route's confidence and provenance.
- Route knowledge now distinguishes player-witnessed, self-discovered and imported evidence; repeated confirmations increase confidence.
- Imported route confidence is deliberately capped below directly witnessed evidence, and conflicting exits are selected by confidence before recency.
- Collective training exports retain route confidence while remaining compatible with v1 training packages.
- Added regressions for route provenance, confidence exchange, preparation explanations and knowledge-page output.

## 1.8.0

- Ultron now observes the player's contiguous overworld movement and records recent map exits with their entry and exit coordinates.
- When strategic navigation fails in a dungeon or interior, Ultron follows the visible player and can reuse the learned exit after the player crosses maps.
- Player-observed routes can be exported and imported with collective training data, allowing another Ultron to reuse shared dungeon exits.
- Ultron now learns the player's species, levels and revealed moves from every battle he can physically observe, not only Gym and League battles.
- Shared training packages now carry player-level evidence alongside route knowledge.
- A known player level advantage unconditionally suppresses automatic and immediate rematches; Ultron catches when his team has space and Poké Balls, otherwise he trains until the gap closes.
- Added save-migration and regression coverage for player movement observation, learned exits, portable route/level data and rematch preparation priorities.

## 1.7.4

- Fixed name-plate projection in wide and survey overworld layouts by mapping through the renderer's world viewport rather than its separate 160x144 UI rectangle.
- Fixed Pokemart supply runs remaining in the player's bedroom when the strategic graph cannot start a route from an interior reverse warp.
- Interior travel now reconstructs the first hop from live warp definitions and reachable neighbouring maps before local pathfinding begins.
- Added regressions for wide-world name-plate projection and recovery from a missing interior route.

## 1.7.3

- Fixed the name plate using the camera-less public World API facade for projection, which left it displaced by the map's scroll offset.
- Name plate projection now resolves the real camera-owning overworld state from the active screen stack before using compatibility fallbacks.
- Added regression coverage proving the plate moves exactly one screen pixel for every one-pixel camera scroll while remaining anchored to Ultron's live sprite frame.
- Ultron now supplies his legitimately owned healing and status-recovery items to the battle AI, and every used item is consumed from his persistent inventory.
- Added regression coverage for Gen 1 item selection, locked actions, empty inventory handling, and Gen 2 post-battle inventory reconciliation.
- Fixed supply-run navigation looping inside the player's room by resolving `LAST_MAP` interior exits to their real local stair or doorway tile.
- Strategic travel now waits for valid exit metadata instead of falling back to random room wandering when a next map is already known.

## 1.7.2

- Fixed BATTLE ME NOW on current Gen1Recomp builds that expose the live overworld through the screen stack instead of `game.overworld`.
- Added a safe built-in trainer-class fallback when the custom trainer registry is unavailable at battle construction time; Ultron's real party still replaces the shell through the scoped party hook.
- Updated Gen 2 launching to use the same authoritative live-overworld resolver and to respect an explicit `startBattle` refusal.
- Battle launch failures now report the exact failed client capability instead of only a generic refusal.

## 1.7.1

- Fixed Message Ultron so B exits immediately when the message field is empty, while B continues to delete entered characters.
- Fixed message completion and cancellation stack handling in both Gen 1 and Gen 2 clients, including Gen 2's caller-owned keyboard close.
- Name plates are now suppressed behind every menu, text box, naming keyboard, battle and transition.
- Anchored Ultron's name plate to the live renderer's exact sprite frame origin, including custom-size and re-anchored overworld sprites.

## 1.7.0
- Fixed BATTLE ME NOW falsely reporting that Ultron is off-map when his live NPC is visibly beside the player.
- Added symmetric player battle prize money: the loser pays from their actual purse and the winner receives the paid amount.
- Ultron now loses money on trainer/wild blackouts before returning to his last visited Center or home.
- Added Gen 1/Gen 2 Gym guide preparation, including legitimate counter-hunting for Whitney's Miltank.
- Added a live species-knowledge index covering all Pokemon registered by the game or installed mods, including learnsets, evolutions and compatibility data.
- Expanded encounter discovery to grass, water, fishing rods and time-of-day tables, allowing legal catches from installed encounter providers.
- Added optional AI adapters for fishing, Bug-Catching Contests, Safari Zones, Wonder Trade and Mystery Gift.
- Expanded evolution handling to registered level, friendship, stone/item and trade-stone methods; required items are consumed.
- Audited story isolation: Ultron retains private badges/campaign state, never writes player story flags, and must own and teach required HMs for physical travel.
- Added regression coverage for map authority, money transfers, blackout stakes, guide knowledge, encounter breadth, activity adapters and evolution prerequisites.

## 1.6.0
- Fixed the post-blackout home stall: Ultron no longer overwrites the AI decision made after healing, so he physically resumes his journey after waking at home/Center.
- Added persistent loss-driven Determination. Losing to the player temporarily increases training, Center counter-preparation and legal same-map rematch pressure.
- Counter-building remains observation-limited: Ultron uses only Pokemon/moves actually revealed in battles he fought or physically observed, plus separately imported collective priors. No hidden player party inspection is introduced.
- Home is no longer treated as a hidden Pokemon Center/Pokemart. Counter-team PC/TM work waits for a real Center and purchases/sales wait for a real Mart.
- Added explicit Colosseum Inspired UI compatibility (`colosseum_ui_overhaul`) as an optional dependency. Name tag/news draw after its final HUD layers and name-tag projection now has a robust window/letterbox fallback when normal viewport fields are absent.
- Moved BATTLE ME NOW to the top of Ultron's direct interaction menu so it remains visible in Colosseum's shorter hanging generic-list viewport.
- Added Partner Chronicle: famous Gym/League/player/title/rematch victories, opponent-specific partner trust, and browsable historical Hall of Fame pages.
- Anti-player team selection can modestly recall partners with proven PLAYER trust, without changing stats or creating Pokemon/items.

## 1.5.0

- Added persistent per-Pokemon bond identities so duplicate species keep separate histories.
- Added individual partner battle records: trainer, Gym, League and player wins/losses, blackouts, comeback rematches and Hall of Fame appearances.
- Added partner progression tiers: Rookie, Trusted Partner, Veteran, Hall of Famer and Ultron Legend.
- Hall of Fame teams now preserve individual bond IDs as well as species/nickname data.
- Signature partners now lock to the individual Pokemon rather than only its species.
- Veteran loyalty influences voluntary team selection without modifying stats.
- Proven player-match partners receive a modest recall preference for anti-player rematch teams.
- Added PARTNER LEGACY to the Start-menu Ultron section.
- Added OLD GUARD, COMEBACK PROTOCOL and DYNASTY achievements.
- Ultron conversation can reference his signature partner's personal battle/Hall-of-Fame history.

## 1.4.0

- Fixed the white-screen regression when leaving Ultron Settings: child menus no longer trigger a second stack pop that can remove the underlying overworld screen.
- Audited every player-facing Ultron page and return path, including direct NPC interaction, Start -> ULTRON, Settings, Training Data, text pages, Back and B/Cancel navigation.
- Training-data import now runs through a game/client file picker instead of a hard-coded sidecar filename.
- Imported collective knowledge is merged into Ultron's persistent save/user-data state outside `mods/ultron`, so normal mod updates do not overwrite it.
- Desktop export now uses a native Save-As dialog and writes the training package to the exact destination selected by the player.
- Android/iOS import now reuses Gen1Recomp's engine-owned system document picker with a feature-specific ownership marker around the shared staging file.
- Added attachment-driven Pokemon nicknames. Ultron may nickname a Pokemon only after sufficient personal bond, signature-partner status, or sustained active-party service.
- Personal nicknames persist on the individual Pokemon through save/load, evolution and PC movement, and never grant artificial stat bonuses.
- Added PARTNER BONDS to the Ultron dashboard, nickname/species display in party history, and the NICKNAME PARTNERS setting.
- Added the NAMING RIGHTS achievement for Ultron giving a bonded Pokemon a personal nickname.
- Battle-party and Hall-of-Fame snapshots now preserve Ultron-assigned nicknames where the host display supports them.

## 1.3.0

- Added persistent Ultron gameplay settings with existing-save migration and all current defaults preserving previous behaviour.
- Added toggles for Catch Legendaries, Forgettable HMs, Reusable TMs, Periodic Challenges, News Ticker, Name Tag, Watch Major Battles, and Daily Routines.
- Catch Legendaries OFF now filters legendary species from both autonomous hunt selection and the legal catch candidate pool while still allowing research/observation.
- Reusable TM and Forgettable HM rules now use Ultron's own standalone settings instead of inherited World option keys.
- Added a dedicated Start -> ULTRON quick-access section with Status/Party, Settings, Import Training Data, Export Training Data, Message Ultron, Latest Update and Achievements.
- Added an Ultron name tag renderer anchored to the live NPC when a safe 2D screen/camera projection is available.
- Added persistent Ultron achievements tied to actual career history: First Blood, Not Again, Signature Bond, Machine Champion, Cartographer, Collective Mind and Legend Thief.
- Achievement unlocks can appear in the news ticker and are visible from the Start-menu Ultron section.
- Optional presentation/rivalry systems can be disabled without disabling Ultron's physical progression, economy, blackout rules, identity or League journey.

## 1.2.1

- Removed the experimental manifest flag.
- Fixed standalone existing-save bootstrap on host builds that expose `game.world` without a Gen 1-style `game.stack`.
- Added standalone NPC materialisation through `game.world.spawnNpc` / `game.world.addRuntimeObject` in addition to the existing WorldAPI and OverworldState paths.
- Added static-collision placement fallback when `MapOverview` is unavailable, while remaining fail-closed on unproven cells.
- Keeps the Engine's live game pointer synchronized after save/overworld transitions.
- Expanded in-game Ultron Diagnostics to distinguish dormant, off-map, unpositioned, and runtime-spawn failures.
- Existing saves still do not teleport Ultron to the player: a newly installed Ultron begins from his canonical starting area and physically travels from there.

## 1.1.1

- Fixed a startup syntax error in the identity-monitoring module on gen1recomp's Lua 5.1-style mod parser.
- Replaced the Lua 5.3-only binary XOR operator with a Lua 5.1-compatible arithmetic checksum.
- Added a release-time Lua 5.1 compatibility audit so unsupported bitwise operators, integer division and goto/labels are rejected before packaging.
- No gameplay behavior from v1.1.0 was removed. Rivalry, signature partner, Hall of Fame, failure memory and collective-training systems remain intact.

## 1.1.0

- Added persistent rivalry stages: Unknown, Rival, Nemesis, Respected Rival, Champion Challenger and Legendary Rival.
- Added a 64-entry player battle notebook with map, result, both known teams and Ultron's team anchor.
- Added relationship-derived signature partners. After enough shared battles, Ultron permanently chooses one partner from actual service history; ordinary PC rotation will not voluntarily box it.
- Added persistent location/failure memory for blackouts, trainer losses, Gym losses and League failures.
- Added a personal Hall of Fame that archives each League-winning team instead of overwriting Champion history.
- Added deterministic post-Champion objectives, including perfect-team, Pokedex, legendary-hunt, unbeaten-reign and player-counter goals.
- Added collective-training provenance and confidence. Imported species/move/lead/map evidence now records how many independent Ultron sources support it, and team planning prioritizes stronger consensus.
- Added Rivalry / Legacy and Training Sources panels to the Ultron menu and grounded chat responses for rivalry, signature partners, Hall of Fame and collective knowledge.
- Rivalry stage and post-Champion goals now influence same-map challenge cadence and competitive preparation frequency.
- Fixed standalone player battle records being incremented twice per battle.
- Synced against the current `MrKrisSatan/Ultron` GitHub v1.0.0 archive before applying this release; the upstream archive matched the local v1.0.0 baseline exactly.

## 1.0.0

- Removed The World as a required dependency; Ultron now vendors and loads its
  own 37-module AI core.
- Added standalone Gen 1/Gen 2 map graph, physical collision travel, battle
  simulation, catching, economy, Gym/League progression and competitive data.
- Added persistent Ultron-only identity, canonical starter rules and private
  money/inventory/PC state.
- Added Ultron-selected first-save appearance, locked for the rest of the save.
- Added same-map autonomous player challenges.
- Added physical route travel with fail-closed collision and real map transitions.
- Added trainer-coordinate approach before required campaign trainer battles when
  the map data exposes a physical trainer position.
- Blackout now returns only to the last visited Pokémon Center or player home.
- Added standalone news ticker and optional merge into The World's AI-rival ticker.
- Added chat input, bounded dialogue memory and battle-history grounding.
- Added offline Smogon-backed competitive team preparation.
- Added portable community training-data export/import with source de-duplication.
