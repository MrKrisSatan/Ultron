# Ultron v2.34.0

**Ultron** is a standalone living-rival mod for **Gen1Recomp** and **Gen2Recomp**. It turns the game into a small shared AI ecosystem containing up to **seven autonomous robot trainers** that pursue their own Pokémon journeys alongside the player.

The end goal is simple: each robot should behave increasingly like a miniature Pokémon-playing AI. They should plan, travel, catch, train, evolve, trade, breed, scout, battle, manage resources, enter tournaments, challenge the League, become Champion, learn from experience and develop as characters, while the simulation remains lightweight enough to run seven agents without becoming a major performance tax.

**The World mod is not required.** Ultron's core simulation, tournaments, companion doubles, Champion history, economy, progression and robot AI are self-contained. Optional integrations are used only when another compatible mod exposes a supported public API.

> **Current release:** v2.34.0  
> **Supported games:** Red, Blue, Yellow, Gold, Silver and Crystal through their recomp clients.

## The seven robots

Every robot owns separate Pokémon, PC storage, money, inventory, badges, objectives, map position, memories, relationships, career state, tactical experience and battle history. They do not share artificial progress.

| Slot | Robot | Canonical starter | Core personality | Long-term identity |
|---:|---|---|---|---|
| 1 | **Ultron** | Unused/counter laboratory starter | Analytical, competitive, counter-meta focused | **Counter-Meta Champion** |
| 2 | **Data** | Vulpix in Gen 1/Yellow, Houndour in Gen 2 | Precise, scholarly, evidence-led | **Battle Scientist** |
| 3 | **R2-D2** | Horsea | Daring, exploratory, improvisational | **Expedition Tactician** |
| 4 | **WALL-E** | Bellsprout | Gentle, persistent, partner-focused | **Partner Custodian** |
| 5 | **Robby** | **Pidgey** | Courteous, protective, service-minded | **Guardian Mentor** |
| 6 | **T-800** | **Geodude** | Relentless, attritional, mission-focused | **Champion Hunter** |
| 7 | **Andrew** | **Poliwag** | Patient, curious, relationship-driven | **Master Trainer** |

If a conversion genuinely lacks one of the fixed starter species, Ultron uses the nearest configured legal fallback from the live registry. It does not invent illegal moves or species simply to preserve a theme.

### Ultron

Ultron studies legitimate battle evidence, builds counters from resources he actually owns and becomes more calculating through repeated competition. His natural end state is a Champion who tries to understand the metagame rather than merely overpower it.

### Data

Data approaches the game as an experiment. He values evidence, reproducible preparation, corrections and increasingly sophisticated battle models.

### R2-D2

R2-D2 is the adventurous improviser. He accepts more risk, explores aggressively and is comfortable winning through unusual legal lines rather than perfect preparation.

### WALL-E

WALL-E is deeply partner-oriented. He values attachment, continuity and the long careers of individual Pokémon, preferring to make trusted partners work rather than replacing them casually.

### Robby

Robby is protective and service-minded. He heals earlier, values partner safety and naturally grows toward mentorship and guardianship. His first partner is Pidgey.

### T-800

T-800 is mission-focused and relentless. He tolerates more attrition, minimises detours and pursues Champion-level objectives with sustained pressure. His first partner is Geodude.

### Andrew

Andrew is patient, curious and relationship-driven. He prefers long partner careers and increasingly nuanced decisions shaped by experience. His first partner is Poliwag.

## Choose 1 to 7 robots

On a new save, Oak's introduction asks how many robot trainers should inhabit that save after the player's name is confirmed.

- **Gen 1:** after Oak confirms the player's name.
- **Gen 2:** after the player-name screen.
- Supported roster sizes are **1 through 7**.
- The chosen count is persisted before the robots begin their journeys.
- Once a save has initialized Ultron, its robot count survives future updates and the introduction prompt is not shown again.
- Older saves that never used Ultron can receive the one-time roster choice through migration.
- The Ultron menu also exposes an explicit roster-size control for supported expansion or reduction.

## Core rule: legitimate autonomous progression

Ultron is built around the idea that robots should progress by playing the game, not by receiving invisible shortcuts.

Robots therefore:

- physically travel through routes, buildings, caves, doors, map seams and warps;
- catch Pokémon through the live encounter registry;
- train and evolve Pokémon through legal requirements;
- buy supplies and sell legitimate surplus at real Poké Marts;
- use Pokémon Centers for healing, PP recovery and PC preparation;
- own finite money, Poké Balls, healing items, TMs, HMs and other inventory;
- preserve HP, PP and persistent status between battles until those resources are actually restored;
- challenge trainers, Gym Leaders, the Elite Four and the Champion;
- black out to the last visited Pokémon Center, or home before one has been visited;
- use their own private campaign state and never advance or borrow the player's story flags;
- require owned and taught HMs when field progression demands them;
- use **Struggle only when every normal move has no PP**;
- never receive free levels, fabricated counter Pokémon, invented moves or hidden stat boosts from learning systems.

The intended result is closer to seven simultaneous AI-controlled playthroughs sharing one world than seven conventional rival NPCs.

## Save DNA: no two independent saves should grow the same way

Every independently created save receives persistent **Ultron Save DNA**.

Save DNA influences bounded legal choices such as:

- each robot's deterministic RNG stream;
- character-arc timing and emphasis;
- hidden learning traits;
- route and hunting tie-breaks;
- tournament seeding and invitation variation;
- modest type and species affinities when several legal team choices are close;
- tactical ceiling variation within each robot's authored limits.

It does **not** alter Pokémon stats, damage formulas, encounter legality, move legality, story flags or ownership.

Reloading the same save remains deterministic. Deliberately copying a save also copies its Save DNA because it represents a branch of the same timeline.

## Character arcs and long-term development

Robots **never retire**. They continue playing indefinitely.

Instead, every robot develops through persistent character chapters shaped by real setbacks, recoveries, mentorship, bonds, tournaments and Champion-level experience. Arc emphasis can lean toward qualities such as:

- Discipline
- Boldness
- Connection
- Exploration
- Resilience

Progression changes how a robot approaches its goals, not whether it participates. T-800 can learn restraint without becoming passive. Robby can become more confident without abandoning his protective identity. Andrew can grow more independent without losing his relationship-driven style.

## Current Plan and goal-directed behaviour

Each robot maintains a persistent planning stack containing:

- ultimate objective;
- current objective;
- active plan step;
- progress toward that step;
- decision confidence;
- current concern;
- contingency plan;
- reason a previous plan was rewritten;
- bounded evidence supporting the decision;
- suspended plans that can resume after emergencies;
- career milestones and reserve-team roles.

The **Current Plan** and Robot Debug views expose this reasoning without revealing hidden player information.

## Independent Pokédex projects

Robots can maintain long-term Pokédex projects drawn from opportunities that genuinely exist in the current game.

Projects can include:

- regional Pokédex completion;
- rare-species hunting;
- Gen 2 breeding projects;
- optional legitimate shiny hunting where supported.

A shared encounter-ecology index is built incrementally and cached once per engine. Seven robots do not each rescan the entire encounter world. A project creates an intention only. The robot must still travel, encounter the species, own Poké Balls and complete the catch legitimately.

## Physical public battle scouting

Robots can decide that a future opponent is worth studying and physically travel to observe a public battle.

Scouting follows strict information boundaries:

- only a bounded number of scouts may be active at once;
- a robot learns only information revealed in a battle it was actually present to watch;
- same-map observers reuse the already-resolved robot duel event;
- observers see the public lineups that actually fought, not hidden PC storage;
- the system never runs duplicate battles just to create scouting data;
- hidden player moves, DVs and private party state remain hidden until legitimately revealed.

One world event can therefore teach several nearby agents cheaply instead of requiring seven independent simulations.

## Adaptive tactical growth without cheating

Robots gain tactical experience through real battles and can unlock deeper legal decision-making over time.

Possible advanced behaviour includes:

- safer pivoting;
- setup disruption;
- revenge positioning;
- preserving a win condition;
- deeper PP-war decisions;
- improved escape/setup judgement;
- stronger resource conservation across major battle sequences.

Each robot has an authored tactical ceiling plus a small Save-DNA variation. Personality flaws remain visible even at high skill. Robby and WALL-E do not become deliberate sacrifice tacticians. R2-D2 only develops patient PP-stall behaviour at his highest tier. T-800 must learn restraint before using safer pivot logic consistently.

Tactical growth never changes Pokémon stats, damage RNG, ownership or item counts.

## Battle memory and Pokémon careers

Robots remember more than wins and losses.

Bounded salient memories can retain events such as:

- a species repeatedly responsible for defeats;
- recurring opponent threats;
- a clutch partner surviving a near-disaster;
- important tournament battles;
- Gym and Elite Four turning points;
- Champion-level victories and defeats;
- rematch patterns and opponent streaks.

Individual Pokémon also develop careers and milestones. Examples include:

- Gym Ace
- E4 Clutch
- Player KO
- Survived 1 HP
- Tournament MVP
- Hall of Fame
- first capture
- trade evolution

Important partners can become signature Pokémon, aces, reserve specialists or Hall of Fame veterans.

## Dynamic team identities and counter-meta evolution

Robots build teams by role, coverage and observed success rather than raw level alone.

Owned Pokémon can be considered for roles such as:

- lead;
- sweeper;
- wall;
- status support;
- revenge killer;
- utility;
- catcher;
- weather support;
- Gym specialist;
- League reserve;
- anti-opponent counter;
- breeding stock;
- trade/evolution stock.

Repeated legitimate success can crystallise into a **Dynamic Team Identity** such as:

- Weather
- Bulky Control
- Status Control
- Speed Offence
- Break Pressure
- Partner Core

Repeated public opponent patterns can also feed **counter-meta adaptation**. Both systems only influence selection among Pokémon and moves the robot legally owns.

## Live risk tolerance

Risk is behavioural, not cosmetic.

It influences:

- healing thresholds;
- damaged-team readiness for major battles;
- voluntary challenge frequency;
- healing/PP/cash reserves;
- willingness to continue after losses or near-blackouts.

Robby and Andrew naturally play safer. T-800 and R2-D2 accept thinner margins. Real failures can temper aggressive behaviour over time.

## Relationships, rivalries and mentorship

Robots maintain persistent social histories with both the player and one another.

Events can include:

- battles and rematches;
- accepted or declined challenges;
- companion journeys;
- cooperation in doubles;
- trades;
- mentorship;
- tournament meetings and finals;
- Champion clashes;
- evolution help;
- returned favours and broken trust.

Relationships can develop into named arcs such as:

- Friend
- Ally
- Rival
- Respected Rival
- Friendly Rival
- Grudge
- Nemesis

These arcs can influence behaviour such as voluntary challenge frequency, but never combat stats.

When robots physically meet, a stronger or more experienced agent can provide **mentorship**. Mentorship transfers planning lessons only. It does not transfer free levels, money, items, Pokémon or hidden knowledge.

## Earned reputation

Public accomplishments can create bounded reputations for robots and the player.

Examples include:

- Champion Slayer
- Giant Killer
- Comeback Specialist
- Collector
- Breeder
- Tournament Monster
- Dynast

A dangerous public reputation can make another robot scout more carefully or reduce reckless voluntary challenges. Reputation is evidence-based and never an invisible difficulty modifier.

## Trading and negotiation

Robots can trade eligible Pokémon with one another when physically together. The player can also choose **Trade Pokémon** while speaking to a robot on the same map.

Starters, Eggs, signature partners, aces, strongly bonded Pokémon and the robot's last usable party member are protected.

Robot-to-robot negotiation can consider:

- duplicate or expendable stock;
- missing Pokédex entries;
- current team gaps;
- new type coverage;
- trade-evolution opportunities;
- trust and relationship history;
- each robot's individual negotiation personality.

Both robots must independently consider a permanent trade fair before it happens.

Trade evolutions and Gen 2 held-item trade evolutions use the correct legal trade path and items.

## Gen 2 competitive breeding

In Gold, Silver and Crystal, each robot has a private Route 34 Day-Care record separate from the player's deposited Pokémon and breeding state.

The breeding planner can reason about:

- Egg Groups;
- gender and Ditto compatibility;
- Gen 2 matching-DV breeding refusal;
- base-form offspring;
- hatch cycles;
- Nidoran offspring;
- father-side Egg Move and TM/HM inheritance;
- shared parental level-up moves;
- Gen 2 Defense/Special DV inheritance;
- competitive inherited moves that improve a planned final evolution.

Robots must physically use the Day-Care, pay their own fees and train the offspring normally.

## Standalone tournament ecosystem

The World mod is not required for tournaments.

Ultron's tournament director supports:

- Single Elimination
- Seeded Cup
- Swiss
- Round Robin
- Double Elimination
- Level 30/50 or configurable level-cap Cups
- Type Cups
- Rental Cups
- Champion Invitationals

The original standalone bracket remains capable of **3 to 100 entrants**.

Restricted Cups preserve legitimacy. Robots use eligible active-party Pokémon or temporary legal tournament overlays and synchronize real HP/status/PP back afterward where appropriate. Rental Pokémon exist only for the rental event and never rewrite owned teams.

### Competitive seasons

Completed tournaments feed an eight-event competitive season containing:

- participation;
- match wins;
- tournament titles;
- upsets;
- seasonal points;
- rankings.

After eight completed events, the final table and awards are archived and a fresh season begins. Awards include **Season Champion**, **Cup Collector**, **Giant Killer** and **Iron Circuit**.

## Champion lineage, eras and challenger adaptation

League history is persistent and bounded.

Champion Lineage records public information such as:

- who held the crown;
- reign duration;
- successful title defences;
- rematches;
- dethronements;
- public final teams;
- decisive Pokémon and moves when actually observable.

Challengers can prepare against the current dynasty using only Pokémon, TMs and evidence they legitimately own or observed.

Significant reigns can become named **Eras**. Repeated dominant reigns can become **Dynasties**. A single lucky title win is not automatically treated as an era.

## Hall of Fame historical archive

The **Hall Archive** reconstructs historical League crowns, title defences and tournament finals from bounded public traces already stored by Champion Lineage and Tournament Director.

It can show:

- old Champion teams;
- title defences and dethronements;
- tournament finalists;
- decisive Pokémon or moves when observed;
- public final-team snapshots.

The archive is a textual historical reconstruction. Ultron never re-simulates an old battle and never invents hidden historical information.

## Robot-driven world stories and news

Major autonomous events can become public world history through the shared **World Story News** chronicle.

Examples include:

- Champion changes;
- the player publicly becoming Champion;
- rare, legendary or shiny catches;
- tournament titles and major upsets;
- character-arc breakthroughs;
- major relationship changes;
- public Omnissiah punishments and other supported system events.

News events are deduplicated, bounded and generated from events Ultron already processes. There is no additional seven-agent polling loop.

## Situation-specific voices

All seven robots have persistent evolving voices and event reactions.

Dialogue can react to:

- blackouts;
- starter faints and evolutions;
- title victories and title losses;
- the player becoming Champion;
- trades;
- grudges and rivalry milestones;
- mentorship;
- rare catches;
- tournament elimination;
- major character-arc events.

Dialogue history is bounded and generated from the event that already occurred rather than from a new background scanner.

## Companion mode and embedded double battles

Talk to a robot on the same map and choose **Accompany Me**. One robot can accompany the player at a time.

While accompanied:

- eligible wild and trainer encounters become double battles;
- the player controls only the player's Pokémon;
- the companion independently chooses its own moves, targets, switches and items;
- companion HP, PP, status and experience persist after battle;
- without a companion, normal battles remain single battles.

The required companion-double systems are embedded in Ultron, so the standalone `double_battles` mod is considered incompatible.

Poké Balls cannot be thrown while two opposing Pokémon remain active. Once a wild side has only one active opponent, the robot can use one of its own Balls on a legal capture attempt.

## Economy and finite resources

Robots manage their own money and supplies.

Budgeting can include:

- Poké Balls;
- healing medicine;
- status cures;
- Revives;
- PP recovery;
- TMs;
- major-battle reserves;
- badge-sensitive cash floors;
- breeding/Day-Care costs;
- long-term acquisition projects.

Healing a healthy team does not generate free happiness. HP, PP and status remain damaged between battles until a legitimate item or service restores them.

Ground items can provide each robot with a private item echo when the robot physically reaches the eligible pickup, while leaving the player's map item untouched. Each robot has its own bounded pickup ledger.

## Moves, TMs and evolution timing

Robot Pokémon evaluate legal moves as they level using factors such as:

- STAB;
- type coverage;
- power;
- accuracy;
- PP;
- priority;
- status/setup/recovery value;
- current team role;
- redundancy with the existing four moves.

Robots can reject poor level-up moves rather than automatically replacing the oldest move.

Single-use TMs receive regret-prevention analysis before being consumed. A robot can hold a TM for a materially better owned or planned recipient. Reusable TMs remain reversible.

Evolution can be delayed when an unevolved form is close to learning a materially valuable move that the evolved form learns much later or not at all. Once the milestone is reached, normal legal evolution continues.

## Current menus and diagnostics

The **ULTRON** menu includes access to features such as:

- robot roster and active robot selection;
- status and party;
- Current Plan;
- Thoughts and knowledge;
- relationships and social arcs;
- Pokédex Goals;
- Public Scouting;
- Tactical Growth;
- tournaments and Season Standings;
- Champion lineage and Hall of Champions;
- Hall Archive;
- Performance;
- achievements;
- settings;
- training-data import/export;
- Message Ultron;
- latest news.

Robot Debug exposes readable summaries for the persistent AI systems so development can be audited instead of relying on opaque internal state.

## Seven-agent performance architecture

Performance is a permanent design requirement, not a cleanup task for later.

Ultron's architecture therefore favours:

- a maximum of **seven active robot identities**;
- a **four-agent expensive-decision budget** per simulation pulse above the four-robot threshold;
- round-robin scheduling for off-screen robots;
- priority for the selected robot and active companion;
- event-driven learning instead of repeated scans;
- shared world caches instead of one cache per robot;
- staggered low-frequency planners;
- bounded histories and diagnostic state;
- one resolved event feeding several cheap observers where possible;
- no seven-copy always-on world scanners.

### Performance profiler

The **Performance** view measures work Ultron already performs.

It records bounded aggregates for:

- per-robot AI decision time;
- scheduler load and active/budgeted agent count;
- travel/pathfinding cost;
- tournament simulation cost;
- average and maximum timings.

The profiler has no independent update loop. It timestamps existing calls only and stores at most seven robot metric rows.

Future increases to the seven-agent cap or expensive-decision budget should be justified by profiler data rather than guesswork.

## Save compatibility and persistence

Ultron is designed to migrate older saves forward without erasing robot progress.

Persistent systems use schema migration/backfill and bounded storage. The current RobotMind schema is **v12**.

Saved state includes the chosen roster count, Save DNA and the independent histories needed for parties, money, relationships, careers, tournament/Champion records and AI development.

Temporary internal ID aliases are migrated so earlier development builds do not orphan Robby, T-800 or Andrew progress after their final IDs are applied.

## Integrity and anti-tamper behaviour

Official runtime Lua files are covered by Ultron's integrity seal. The seal is regenerated for official releases so legitimate updates are never mistaken for unauthorized modification.

If Ultron detects protected code has been altered outside the official release process, its configured anti-tamper/Rogue Protocol behaviour can activate. The official v2.34.0 package was resealed after all final source changes.

## Configuration

Persistent settings include options such as:

- Catch Legendaries
- Forgettable HMs
- Reusable TMs
- Periodic Challenges
- News Ticker
- Name Tags
- Watch Player Battles
- Daily Routines
- Nickname Partners

Presentation settings do not disable the underlying physical economy, movement or campaign simulation unless explicitly documented.

## Installation

1. Download **Ultron_v2.34.0.zip** from the v2.34.0 GitHub release.
2. Install or extract it as the `ultron` mod directory.
3. Confirm `manifest.json` and `main.lua` are directly inside that directory.
4. Start or load Red, Blue, Yellow, Gold, Silver or Crystal through the supported recomp client.
5. New Ultron saves can choose between one and seven robots during the introduction.

Ultron remains dormant until the player's starter is committed. Existing saves migrate without teleporting established robots to the player.

## Compatibility

- **Games:** Red, Blue, Yellow, Gold, Silver and Crystal through supported recomp clients.
- **The World:** optional integration only. Not required.
- **Standalone tournaments:** included in Ultron.
- **Companion double battles:** included in Ultron.
- **Standalone `double_battles` mod:** incompatible because Ultron embeds and controls its companion-only implementation.
- **Colosseum UI Overhaul:** optional presentation compatibility where supported.
- **Link play:** protected by Ultron's battle-affecting compatibility declaration.

## v2.34.0 validation

The packaged v2.34.0 release passed:

- **101/101 regression audits**;
- **237 Lua files compiled**;
- **133 protected runtime files** passed the regenerated integrity seal;
- story/news regression tests;
- situation-specific dialogue tests;
- Hall Archive tests;
- Performance Profiler tests;
- seven-agent miniature-AI integration tests;
- Save DNA divergence tests;
- standalone tournament tests without The World installed;
- fresh extracted-package integrity checks;
- ZIP corruption checks.

SHA-256 for `Ultron_v2.34.0.zip`:

`e619ee8303231508f005f6d56bd981a1ee888f6042357463366ed06741e3c501`

## Development direction

The formal feature roadmap is currently complete, but Ultron's permanent development rules remain active:

1. Work toward seven increasingly capable miniature AI agents rather than scripted rivals.
2. Preserve legal Pokémon progression and strict information boundaries.
3. Make independently created saves diverge through Save DNA and lived experience.
4. Prefer event-driven, shared and staggered computation over duplicated background loops.
5. Keep persistence bounded and migration-safe.
6. Add deterministic regression coverage and readable diagnostics for new systems.
7. Use performance measurements before increasing the seven-agent scheduler budget.

See [CHANGELOG.md](CHANGELOG.md) for detailed version history and [RELEASE_NOTES.md](RELEASE_NOTES.md) for release-specific notes.

## Release

**Current release: [v2.34.0](https://github.com/MrKrisSatan/Ultron/releases/tag/2.34.0)**

[Download the latest release](https://github.com/MrKrisSatan/Ultron/releases/latest)
