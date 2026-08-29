# Ultron v2.30.0

**Ultron** is a standalone living-rival mod for **Gen1Recomp** and **Gen2Recomp**. Instead of placing one scripted trainer on a route, Ultron adds up to **seven autonomous robot trainers** who live inside the same game world as the player.

They travel, catch and train Pokémon, manage money and finite supplies, use Poké Marts and Pokémon Centers, build teams, learn moves, evolve partners, challenge Gyms, enter tournaments, trade, breed in Gen 2, challenge one another, pursue the Pokémon League, become Champion, lose the title, adapt, and try again.

**The World mod is not required.** When The World or another supported mod is installed, Ultron can use optional public integration APIs, but its core simulation, tournaments, companion doubles, Champion history, economy, progression and robot AI are self-contained.

> Current package: **v2.30.0**  
> Supported games: **Red, Blue, Yellow, Gold, Silver and Crystal** through their recomp clients.

## Design rule: autonomous, persistent and legitimate

Ultron is built around one rule: robots should progress by playing the game rather than by receiving invisible shortcuts.

Robots therefore:

- own separate parties, PC storage, money, Bags, Poké Balls, TMs, HMs and held items;
- maintain their own badges, objectives, position, memories, relationships, careers and battle records;
- physically travel through routes, buildings, caves, doors, map seams and warps;
- obey story, badge, HM and map-access requirements;
- use Pokémon, moves and items they legitimately own;
- visit real Pokémon Centers to heal, restore PP and reorganise PC teams;
- visit real Poké Marts to buy supplies and sell eligible valuables;
- never borrow the player's story flags, inventory, party, money or hidden team information;
- never receive free levels, hidden stat boosts, fabricated counter Pokémon or invented moves from their learning systems;
- keep damage, PP and persistent status conditions between battles until they are actually treated;
- can use **Struggle only when no normal move has PP**, matching the game's invisible fifth-move rule.

The result is closer to seven AI-controlled playthroughs sharing one world than seven conventional rival NPCs.

## Choose 1 to 7 robots

On a new save, Oak's introduction asks how many robot trainers should inhabit that save after the player name is confirmed.

- **Gen 1:** after Oak confirms the player's name.
- **Gen 2:** after the player-name screen.
- Available roster sizes: **1 through 7**.
- The chosen count is persisted before the robots begin their journeys.
- A save that has already used Ultron keeps its existing robot count across updates and is not prompted again.
- Older saves that never used Ultron receive a one-time roster choice when the migration path is applicable.
- The Ultron menu also exposes an explicit **Roster Size** control for supported expansion or reduction without re-running the intro prompt.

## The seven robots

Each robot has an authored starting personality, a persistent evolving voice, a long-term career/philosophy, independent risk tolerance, relationship history, reputation and team-building tendencies.

| Slot | Robot | Starter | Core style | Long-term career |
|---:|---|---|---|---|
| 1 | **Ultron** | Unused/counter laboratory starter | Analytical, competitive, counter-meta focused | **Counter-Meta Champion** |
| 2 | **Data** | Vulpix in Gen 1/Yellow, Houndour in Gen 2 | Precise, scholarly, evidence-led | **Battle Scientist** |
| 3 | **R2-D2** | Horsea | Daring, exploratory, improvisational | **Expedition Tactician** |
| 4 | **WALL-E** | Bellsprout | Gentle, persistent, partner-focused | **Partner Custodian** |
| 5 | **Robby** | **Pidgey** | Courteous, protective, service-minded | **Guardian Mentor** |
| 6 | **T-800** | **Geodude** | Relentless, attritional, mission-focused | **Champion Hunter** |
| 7 | **Andrew** | **Poliwag** | Patient, curious, relationship-driven | **Master Trainer** |

### Ultron

Ultron begins analytical, confident and competitive. He studies legitimate battle evidence, prepares counters from resources he actually owns and becomes more calculating after defeats. His long-term objective is to become and remain Champion by out-planning the strongest opposition he has genuinely observed.

### Data

Data approaches Pokémon as a battle scientist. He values reproducible evidence, consistent preparation, explanations and corrections. His voice increasingly references hypotheses, confidence and observed patterns rather than bravado.

### R2-D2

R2-D2 is the explorer of the roster. He accepts more risk, takes unusual routes, improvises with owned resources and develops a spirited rivalry style. His career rewards exploration, flexible teams and tournament success.

### WALL-E

WALL-E is gentle, persistent and deeply partner-oriented. He values attachment, long service and the history of individual Pokémon more strongly than raw replacement value. His goal is to prove a bonded team can survive Champion-level competition.

### Robby

Robby is protective, courteous and service-minded. He scouts carefully, heals earlier, protects partners and is naturally suited to mentoring less-experienced robots without carrying them. His canonical first partner is **Pidgey**.

### T-800

T-800 is mission-focused and relentless. He minimises detours, tolerates more attrition, applies sustained pressure and is comfortable entering fights at thinner margins than the cautious robots. His canonical first partner is **Geodude**, and his long-term career is hunting Champions and building durable title reigns.

### Andrew

Andrew is patient, curious and increasingly relationship-driven. He prefers long partner careers, careful development and teams whose history matters as much as peak strength. His canonical first partner is **Poliwag**.

If a conversion genuinely omits one of the fixed starter species, Ultron uses the nearest configured legal fallback present in that game's live registry. It does not inject illegal level-5 moves simply to manufacture STAB.

## Independent lives, careers and plans

Every robot maintains a persistent internal life rather than a single short-term state machine.

The planning stack includes:

- ultimate long-term objective;
- current objective and active plan step;
- progress toward that step;
- decision confidence and commit threshold;
- current concern;
- contingency plan;
- reason a previous plan was rewritten;
- bounded evidence supporting the current decision;
- suspended plans that can resume after emergencies;
- career and philosophy milestones;
- reserve-team careers and bench roles;
- post-Champion goals after reaching the summit.

The **Current Plan** UI and Robot Debug views expose these decisions without revealing hidden player information.

## Personality development and live risk tolerance

Robot personalities are not frozen at new-game creation.

Real outcomes slowly modify bounded learned tendencies such as caution, boldness, curiosity, discipline, loyalty, rivalry and resilience while preserving each robot's authored core identity.

In v2.30.0, **risk tolerance is live behaviour** rather than flavour text. It affects:

- when a robot chooses to heal;
- whether a damaged team is considered ready for a major battle;
- how frequently it voluntarily challenges the player;
- how much healing, PP recovery and cash reserve it tries to preserve;
- whether repeated losses or near-blackouts make it more cautious.

Robby and Andrew naturally play safer. T-800 and R2-D2 accept thinner margins. Repeated failure can temper even an aggressive robot.

## Battle memory and Pokémon history

Robots remember more than a win/loss counter.

### Salient battle memory

Bounded memory can retain events such as:

- a species repeatedly responsible for defeats;
- a recurring opponent threat;
- a clutch partner surviving a near-disaster;
- important tournament battles;
- Gym and Elite Four turning points;
- Champion-level victories and defeats;
- opponent streaks and rematch patterns.

These memories can influence planning and dialogue, but they do not grant hidden battle information or stat bonuses.

### Individual Pokémon careers

Robots also keep histories for individual Pokémon. Partners can earn milestones such as:

- **Gym Ace**
- **E4 Clutch**
- **Player KO**
- **Survived 1 HP**
- **Tournament MVP**
- **Hall of Fame**
- first capture
- trade evolution

A long-serving partner can become an ace, signature Pokémon, reserve specialist or Hall of Fame veteran. Important faints and recoveries produce context-sensitive reactions.

Nickname attachment is optional. A robot can name a Pokémon at capture time, but a later rename requires a physical trip to the in-game Name Rater. Traded Pokémon are not silently renamed.

## Relationships, rivalries, mentorship and social arcs

Robots maintain relationships with both the player and one another.

They remember meaningful events including:

- battles and rematches;
- accepted and declined voluntary challenges;
- companion journeys;
- cooperation in double battles;
- trades;
- mentorship sessions;
- tournament meetings and finals;
- Champion-level clashes;
- assistance and evolution help;
- snubs, broken trust and returned favours.

Repeated history can evolve into named social arcs such as:

- **Friend**
- **Ally**
- **Rival**
- **Respected Rival**
- **Friendly Rival**
- **Grudge**
- **Nemesis**

These arcs can modestly change behaviour such as voluntary challenge frequency. They do not force battles or alter combat stats.

When robots physically meet, stronger or more experienced robots can provide **mentorship**. Mentorship shares planning lessons, not levels, Pokémon, money, items or hidden knowledge.

## Earned reputation

Robots and the player can earn bounded public reputations from observed accomplishments.

Examples include:

- **Champion Slayer**
- **Giant Killer**
- **Comeback Specialist**
- **Collector**
- **Breeder**
- **Tournament Monster**
- **Dynast**

A dangerous public reputation can make robots scout more carefully or reduce reckless voluntary challenges. Reputation is evidence-based and visible through diagnostics rather than being an invisible difficulty modifier.

## Team Architect and dynamic team identity

Robots build teams by role as well as raw level.

Owned Pokémon can be evaluated as:

- lead;
- sweeper;
- wall;
- status supporter;
- revenge killer;
- utility member;
- catcher;
- weather supporter;
- Gym specialist;
- League reserve;
- anti-player counter;
- breeding stock;
- trade/evolution stock.

Coverage only counts when the Pokémon actually knows a suitable move.

Repeated legitimate success can also crystallise into a **Dynamic Team Identity** such as:

- Weather
- Bulky Control
- Status Control
- Speed Offence
- Break Pressure
- Partner Core

Team identity is a modest selection preference among Pokémon the robot already owns. It never creates a Pokémon, move, item or stat boost.

Robots maintain a useful reserve bench rather than hoarding every duplicate indefinitely. Important reserves can have specific careers, while surplus value can be traded or sold under the economy rules.

## Opponent modelling and counter-meta adaptation

Robots learn from battles they actually participate in or legitimately observe.

They can remember:

- revealed species;
- highest observed levels;
- moves actually revealed in battle;
- recurring threats;
- repeated archetypes;
- likely resistance switches inferred from known bench information;
- whether a known team looks balanced, fast, defensive, status-focused, weather-focused or hyper-offensive.

Repeated public patterns feed **counter-meta evolution** and Champion preparation. Counter plans are executed only with Pokémon, TMs and items the robot already owns, usually through legal Pokémon Center preparation.

Imported or shared strategic knowledge is trusted less than direct observation. Robots never read the player's hidden full movesets, DVs, held items or private party state as scouting information.

## Moveset intelligence, TM discipline and evolution timing

Robot Pokémon process the live legal learnset as they level. New moves are evaluated for:

- STAB;
- type coverage;
- power;
- accuracy;
- PP;
- priority;
- setup/status/recovery value;
- current role;
- redundancy with the existing four moves.

Robots can decline poor moves rather than always replacing the oldest attack.

Single-use TMs are treated as irreversible resources. A robot needs both a meaningful moveset improvement and enough decision confidence before consuming one. Reusable TMs remain reusable when that option is enabled.

Evolution timing can deliberately wait when an unevolved form is close to learning a materially valuable move that the evolved form learns much later or never. Once the useful milestone is reached, normal legal evolution continues.

Trade evolutions and held-item trade evolutions use the correct trade path and required items.

## Battle tactics and resource-aware combat

Live battle AI understands more than raw type effectiveness.

Depending on the generation and available mechanics, robots can reason about:

- STAB and type effectiveness;
- accuracy and remaining PP;
- status and setup value;
- healing and switching;
- sacrifice lines;
- revenge-kill opportunities;
- preserving a win condition;
- PP wars;
- resource conservation across Elite Four stages;
- opponent archetypes and observed switch patterns;
- abilities, natures and held-item information when those mechanics exist and are legitimately available through the loaded game/mod data.

A robot does not heal a healthy team for free happiness. Healing, PP recovery and status cures consume the real resources or services required by the game.

## Physical world competence

Robots are expected to reach objectives by travelling through the world.

The navigation system includes:

- collision-aware movement;
- doors, caves, warps and map seams;
- HM and badge gates;
- remembered solved routes;
- route danger and navigation confidence;
- safer-route preference when alternatives exist;
- oscillation detection and temporary approach-tile blacklists;
- deterministic stuck snapshots;
- traffic handling when robots meet at narrow passages;
- emergency replanning for critical HP, no Poké Balls, exhausted PP or invalid routes.

A robot blacking out returns to its last visited Pokémon Center, or home before it has visited one, and loses money under the normal robot economy rules.

## Catching, acquisition missions and ecology

Robots catch through the live encounter registry, including compatible mod-added species and forms.

Capture decisions can consider:

- species novelty;
- rarity;
- team need;
- evolution potential;
- legal moves;
- NPC-trade requirements;
- DVs where relevant;
- duplicate value;
- active long-term goals;
- Ball scarcity and specialised Ball value.

A concrete team weakness can become a **General Acquisition Mission**. The robot identifies a legal species that solves the problem, verifies that the encounter map exists and is reachable, buys enough Balls from a real Mart if needed, physically travels there, hunts through ordinary encounters and then trains/activates the catch normally.

Robot Nuzlocke integrations can deliberately suppress targeted-species hunting when it would violate first-encounter rules.

## Ground items and private item echoes

When a robot physically reaches an eligible live ground-item pickup, it can receive its own private echo copy without removing or flagging the player's map item.

Each robot has an independent bounded pickup ledger. This allows separate robots to find their own copy while the player's copy remains untouched.

Rare Candies can be reserved for useful legal milestones. Nuggets and other valuables can be sold only when the robot's long-term budget benefits, while known recipe requirements remain protected.

## Economy and finite resources

Each robot owns and manages its own money.

Budgeting includes:

- Poké Balls;
- healing medicine;
- status cures;
- Revives;
- PP recovery;
- TMs;
- major-battle reserves;
- badge-sensitive cash floors;
- travel and project costs;
- Gen 2 breeding/Day-Care fees;
- Kurt projects where available.

Robots can sell genuine surplus valuables and duplicates at real Marts, but protected starters, bonded partners, important reserves and project stock are not casually liquidated.

Player battles have real stakes. Prize money moves between the participating sides rather than appearing from nowhere.

## Robot-to-robot and player trading

Robots can trade eligible Pokémon with one another when physically together. The player can also choose **Trade Pokémon** while speaking to a robot on the same map.

Trade protection covers starters, Eggs, signature partners, aces, strongly bonded Pokémon and the robot's last usable party member.

### Negotiated robot trades

v2.30.0 expands robot-to-robot negotiation. A proposed permanent trade can be scored for:

- duplicate or expendable stock;
- missing Pokédex entries;
- current team gaps;
- new type coverage;
- trade-evolution opportunities;
- trust and relationship history;
- each robot's negotiation personality.

Both robots must independently consider the deal fair before it happens.

Robby, T-800 and Andrew have their own negotiation profiles rather than inheriting Ultron's generic one.

### Canonical NPC trades

Robots can also complete the games' real NPC Pokémon trades as private parallel transactions. They must own the requested Pokémon and physically reach the canonical trade location. The player's NPC trade flag, dialogue state, party and PC remain untouched.

## Private Gen 2 competitive breeding

In Gold, Silver and Crystal, each robot has a private Route 34 Day-Care record completely separate from the player's breeding state.

The breeding planner understands:

- Egg Groups;
- gender and Ditto compatibility;
- Gen 2 matching-DV refusal;
- base-form offspring;
- level-5 Eggs;
- hatch cycles;
- Nidoran offspring behaviour;
- father-side Egg Move and TM/HM inheritance;
- shared parental level-up moves;
- Gen 2 Defense/Special DV inheritance.

A robot must own compatible parents, physically visit the Day Care, pay its own costs, wait for the project and then train the offspring normally. Valuable hatchlings can become long-term bench-development projects.

## Standalone tournaments

Ultron v2.27.0 and later contains its own tournament director. **The World is not required.**

Ultron can build persistent brackets with **3 to 100 entrants** and can:

- seed the player and active robots;
- create legitimate guest trainer parties from loaded data;
- handle non-power-of-two byes;
- simulate off-screen matches;
- launch the player's rounds as real trainer battles;
- carry HP, PP and robot/guest resource state between rounds;
- record elimination and winners once;
- preserve scarce resources for later rounds;
- save and resume pending player matches using stable match IDs.

Tournament history tracks robot-vs-robot records, finals, repeat title streaks, rivalries and **dynasties**.

External tournament APIs are optional compatibility fallbacks only.

## Champion lineage and challenger adaptation

League succession is persistent.

The bounded **Champion Lineage** records only legitimate public or observed title information, including:

- Champion holder;
- succession order;
- public team species/levels;
- reign length;
- title defences;
- rematch history;
- decisive Pokémon and move only when actually exposed by the battle trace.

Qualified challengers can prepare for the current Champion. Reigning Champions can prepare for likely challengers using only prior observation or public title history.

Preparation may include travelling to a Pokémon Center and legally reorganising the PC team or spending an owned TM. Historical dethroning teams can create a modest preference for already-owned species that have repeatedly succeeded in the role.

The **Hall of Champions** combines League lineage and tournament history into a readable competitive record.

## Gym and League postmortems

Losses can generate corrective prescriptions instead of defaulting to blind grinding.

A prescription may call for:

- changing the active six;
- training a named reserve;
- acquiring a reachable resistance;
- buying healing, status or PP supplies;
- reviewing an exhausted low-PP move at a Pokémon Center;
- raising the legal level margin.

Later success retires the prescription into bounded history.

## Elite Four expedition intelligence

The Elite Four is treated as a multi-stage expedition rather than four disconnected battles.

Robots prepare healing, status and PP reserves before entering. During the run, HP and PP persist between stages. Recovery is limited to items the robot actually brought, and resource policy can conserve scarce medicine or PP restoration for later opponents.

A robot cannot magically heal between Elite Four battles.

## Special activities

Where supported by the current game or another mod's public API, robots can intelligently participate in activities such as:

- Safari Zone;
- Bug-Catching Contest;
- fishing;
- Wonder Trade;
- Mystery Gift;
- tournament events.

The planner evaluates remaining steps, Balls, time, current catch quality, owned Rods and route-specific encounter tables rather than invoking these activities blindly.

## Companion mode and embedded double battles

Talk to a robot on the same map and choose **Accompany Me**. One robot can accompany the player at a time.

The companion follows the player's actual route roughly one tile behind when the map permits it.

While accompanied:

- eligible wild and trainer encounters become double battles;
- the player controls only the player's Pokémon;
- the robot independently controls its own Pokémon;
- the robot chooses targets, moves, switches and items;
- cooperative scoring considers effectiveness, STAB, PP and the player's selected target;
- the robot avoids redundant attacks on an almost-fainted target when another foe still needs pressure;
- spread moves that would unnecessarily hurt the player's Pokémon are avoided unless the ally is immune;
- robot HP, PP, status and experience persist after the battle.

Without a companion, ordinary battles remain single battles.

The required double-battle implementation is embedded in Ultron. The standalone `double_battles` mod is therefore incompatible.

Neither side may throw a Poké Ball while two opposing Pokémon remain active. Once only one wild opponent remains, a robot companion can use one of its own Poké Balls and a successful capture belongs to that robot.

## Thoughts, evolving voices and dialogue

Before a robot begins a direct player challenge, it speaks through the game's normal text box.

Dialogue is not limited to fixed trainer quotes. Persistent voice state can evolve with:

- wins and losses;
- confidence changes;
- repeated meetings;
- relationships;
- partner milestones;
- social arcs;
- Omnissiah judgement/commendation events;
- tournament and Champion history;
- salient memories;
- recent postmortem lessons.

Each robot keeps its own tone. Data tends toward evidence and hypotheses, R2-D2 toward energetic improvisation, WALL-E toward attachment, Robby toward protection, T-800 toward objective-driven minimalism and Andrew toward reflective partner development.

## Omnissiah judgement and commendation

Ultron exposes public event seams for **Omnissiah punishment**, **praise** and **encouragement** without inventing an external authority inside the rival AI.

When a compatible system emits a judgement or commendation:

- the event is persisted;
- the shared news ticker reports it;
- active robots can acknowledge the event with personality-specific dialogue;
- punishment history and commendation history remain bounded;
- praise can make small learned-personality adjustments;
- no event grants free stats, levels, items, money, RNG advantages or story progression.

## News ticker and world events

Major autonomous events can be reported through Ultron's news ticker, including:

- robot progression;
- important battles;
- Champion changes;
- tournament results;
- partner milestones;
- training and scouting;
- Omnissiah judgement/commendation;
- integrity alerts;
- selected long-term planning events.

This makes off-screen robot progress visible without teleporting robots to the player.

## Ultron menu

The Start menu contains an **ULTRON** section with access to systems such as:

- robot roster and active-robot selection;
- roster size;
- Current Plan;
- relationship network;
- status and party;
- Thoughts and knowledge;
- battle memory and learned evidence;
- partner legacy and chronicle;
- Hall of Fame;
- Hall of Champions;
- settings and achievements;
- training-data import/export;
- Message Ultron;
- latest news;
- password-gated Robot Debug for robot-only diagnostics.

Talking to a visible robot opens that robot's individual interaction menu. Attached nameplates follow the overworld sprite and are hidden behind menus, text boxes, naming screens, battles and transitions.

## Training-data import and export

Robots can export confirmed strategic knowledge and import it later without copying progression.

Portable training data can include learned strategic evidence, but does **not** copy:

- Pokémon;
- levels;
- badges;
- money;
- inventory;
- story progress;
- private player state;
- personal chat history.

Imported knowledge is stored in persistent user/save data rather than inside the mod directory, so updating the mod does not wipe it.

## Settings

Persistent options include controls for features such as:

- Catch Legendaries;
- Forgettable HMs;
- Reusable TMs;
- Periodic Challenges;
- News Ticker;
- Name Tags;
- Watch Player Battles;
- Daily Routines;
- Nickname Partners.

Disabling presentation options does not disable the physical simulation, economy, blackouts or robot campaign progression.

## Save compatibility and bounded persistence

Ultron migrations are designed so an established save keeps its robot identities and progress across releases.

Recent schema migrations cover:

- seven-robot IDs and aliases;
- Champion/tournament history;
- Current Plan evidence;
- careers and mentorship;
- battle memory;
- relationship evolution;
- dynamic team identity;
- live risk tolerance;
- reputation;
- trade negotiation.

Histories are intentionally bounded so long-running saves do not accumulate unlimited diagnostic or social data.

## Seven-robot performance model

Seven robots are the supported roster cap for v2.30.0.

Once more than four robots are active, Ultron does **not** run seven expensive planners simultaneously. It uses a four-decision rotating budget on the normal simulation pulse:

- selected robot and active companion receive priority;
- remaining robots are scheduled round-robin;
- off-screen careers continue to progress on staggered slices;
- relationship pair processing remains throttled rather than running every frame.

At seven robots there are 21 possible robot pairs, but pair processing occurs on the social cadence rather than every frame.

Actual frame rate still depends on device, map complexity, recomp build and other installed mods. Seven is the tested/supported design target, not a promise that every hardware combination will maintain the same FPS.

## Integrity and diagnostics

Ultron includes an integrity seal over protected runtime Lua files. Official releases regenerate the seal after code changes so legitimate updates do not trigger Rogue Protocol.

Debugging and regression infrastructure includes deterministic audits for planning, migration, tournaments, Champion lineage, relationships, memory, trading and other robot systems.

The v2.30.0 packaged build completed:

- **85/85 regression audits**;
- **211 Lua files compiled**;
- **123 protected runtime files validated by the integrity seal**;
- fresh ZIP extraction and package smoke testing.

## Installation

1. Download the latest release from [GitHub Releases](https://github.com/MrKrisSatan/Ultron/releases/latest).
2. Install or extract it as the `ultron` mod directory.
3. Confirm that `manifest.json` and `main.lua` are directly inside that directory.
4. Start Red, Blue, Yellow, Gold, Silver or Crystal.
5. On a new save, choose **1 to 7 robots** during Oak's introduction.

Ultron remains dormant until the player's starter is committed. Existing saves migrate without teleporting established robots to the player.

## Compatibility

- **Games:** Red, Blue, Yellow, Gold, Silver and Crystal through their recomp clients.
- **The World:** optional supported integration. Not required for core Ultron systems or tournaments.
- **Colosseum UI Overhaul:** optional presentation compatibility.
- **Standalone Double Battles:** incompatible because Ultron embeds and controls its companion-only double-battle implementation.
- **Link play:** protected by Ultron's battle-affecting compatibility declaration.
- **Other mods:** live registries and supported public APIs remain authoritative where integrations are available.

## Current development roadmap

The living unfinished-feature list is maintained in [`docs/ROBOT_IMPROVEMENT_ROADMAP.md`](docs/ROBOT_IMPROVEMENT_ROADMAP.md).

As of v2.30.0, the next major roadmap area is **Retirement and Comeback Arcs**, followed by additional long-term systems such as Champion eras, richer tournament formats, seasons, Pokédex goals, public-match scouting, adaptive skill ceilings, personality arcs, robot-driven story/news events, expanded dialogue, Hall of Fame replay/archive and an Ultron performance profiler.

Completed roadmap items are removed from the unfinished list only after they have save migration/backfill, bounded persistence, readable diagnostics and deterministic regression coverage.

## Release history and documentation

- [Latest release](https://github.com/MrKrisSatan/Ultron/releases/latest)
- [CHANGELOG.md](CHANGELOG.md)
- [RELEASE_NOTES.md](RELEASE_NOTES.md)
- [Robot improvement roadmap](docs/ROBOT_IMPROVEMENT_ROADMAP.md)

Ultron's README describes the **current mod**. Detailed version-by-version implementation history belongs in the changelog and release notes, so this page can stay useful to players instead of becoming a geological core sample of every patch ever shipped.
