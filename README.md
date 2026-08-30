Warning: truncated output (original token count: 49404)
Total output lines: 1258

# Ultron 3.0.0: The Champion Directive

Ultron 3.0 turns every robot's systems into one persistent, self-directed Pokémon campaign. Each robot maintains a bounded **Campaign Tree** from its ultimate Champion directive through strategic, tactical and immediate goals to the live blocker. Catching, training, shops, travel, scouting, postmortems, breeding, Pokédex work and existing Agent Brain reasoning now compete beneath that shared purpose instead of behaving like disconnected activities.

**Progress Pressure** rises whenever the campaign fails to advance. Personality changes how quickly a robot abandons detours—WALL-E gives trusted places and partners more time; T-800 cuts away distractions fastest—but all robots eventually classify purposeless familiarity as stale and resume the next legal Gym or League route.

Generated missions include expeditions, Gym preparation, evolution projects, dynamic training relocation, counter hunts, TM acquisition, cash recovery, League provisioning and post-Champion team development. Missions create intentions only: the robot must still know or discover a legal destination, travel physically, own supplies, pay costs, encounter targets, succeed in battles and respond to failure.

After a blackout, recovery is a temporary Campaign Tree leaf. The prior strategic target and a structured postmortem survive; once healed, the robot immediately resumes the campaign rather than treating a home or Center as a destination.

Robot Debug exposes `ULTIMATE`, `STRATEGIC`, `TACTICAL`, `IMMEDIATE`, `BLOCKER`, the four pressure components, activity obligation class, latest postmortem, campaign statistics and a bounded reasoning trace.

See [docs/CHAMPION_DIRECTIVE.md](docs/CHAMPION_DIRECTIVE.md) for the complete contract.

# v2.99.0: Automatic Performance Regression Gates

Ultron now has deterministic release gates for the seven-agent performance contract. Every AI pulse can account for deep plans, incremental-search stages, scheduler selections and per-robot path requests. The audit fails when new work exceeds declared pulse limits, multiplies beyond approved seven-agent baselines or lets registered persistent state exceed its cap.

The checks use operation counts and bounded ratios rather than machine-dependent frame timing. Runtime profiler diagnostics now show the gate state and retain only the latest 64 pulses/violations.

The completed performance-gates item has been removed from the unfinished roadmap. **OM7: Commend demonstrated discipline** is next.

# v2.98.0: Dirty-State Planning + KANTO: STORMFORGED v1.1 Compatibility

Ultron now completes roadmap item **46: Dirty-state planning**. The seven-agent scheduler still gives robots fair execution slices so they can keep walking, battling, healing, shopping and carrying out an already-valid plan, but expensive Agent Brain planning now sleeps while that plan's relevant facts remain unchanged. A bounded robot-owned fingerprint watches map, objective/state/destination, badges, money, blackout state, active-party HP/status/PP and primitive inventory counts. Ordinary x/y tile movement is deliberately excluded, so physically walking a route does not make the planner reconsider the route every tile.

A deep plan wakes immediately when the reusable plan is missing, Agent Brain is dirty, an explicit force-replan is raised, Plan Recovery invalidates the plan on the selected slice, or relevant robot-owned facts changed. Clean brains also receive a deterministic **8-10 scheduler-tick fairness refresh**, preventing starvation or permanently stale assumptions. Performance Scaling and distance-based Agent Sleep now treat this dirty-state wake decision as authoritative: CONSERVE/PROTECT can no longer postpone a real wake, while FULL fidelity can no longer force redundant clean planning. Execution and planning are therefore decoupled, preserving autonomous forward progress while removing needless seven-agent thought loops.

## Current KANTO: STORMFORGED cart contract

Ultron's compatibility adapter is updated to the live **KANTO: STORMFORGED v1.1.1** Yellow-first contract (`>=0.1.86 <1.0.0`) and recognises the cart's exact IDs/versions: Kanto Reforged 1.5.3, Weather FX 4.31.2, WX Pokémon 1.2.0, Better Buildings 1.16.0, HGSS Sprites 1.0.2, Pokéball Colors 0.1.64, Too Many Balls 0.8.8, Damage Numbers 0.4.0, Evolve in Battle 2.0.3, Running Shoes 0.3.0 and Battle Art 2.0.3. The adapter classifies authority conservatively: live Kanto Reforged registries, Weather FX state, WX encounter resolution and live collision/warp topology may affect robot decisions; artwork, damage-number display, player evolution UI and Battle Art rendering never become AI game-state authority.

Too Many Balls is allowed to extend the live legal item/ball registry without Ultron patching the player's Bag or Mart. Pokéball Colors remains the ball-presentation owner where installed. Running Shoes changes player frame speed, not free robot travel distance. Evolve in Battle remains player-facing and is never invoked or cancelled by robot evolution. Battle Art replaces the old Dramaless compatibility role in the cart and is treated as rendering/camera geometry only. Legacy standalone Wilds, Mystery Gift, Dramaless and Modern PC integrations remain fail-closed when separately installed, but they are not required by the current cart.

The completed dirty-state item has been deleted from the unfinished-only roadmap. **47: Incremental search** is now the next item.

# v2.96.0: Shared Expensive Computations + Forward Progress Recovery

Roadmap item 45 is complete. Immutable world facts are now computed once and reused across all seven robots. A shared core cache owns the loaded type chart, canonical species definitions, normalized species/evolution profiles, per-map encounter rows and the static badge-to-Gym progression catalogue. The existing shared MapGraph remains the one route topology and its route cache remains authoritative. BattleSim, Rival species lookup, acquisition valuation, subjective asset valuation, trade-evolution planning, long-horizon evolution planning and irreversible move forecasting now consume those shared facts rather than independently rebuilding equivalent tables.

This release specifically targets robots that fail to advance through the game. Plan Recovery now asks the shared progression catalogue for the robot's next legal Gym/League anchor before falling back to a generic exploration frontier. During a genuine badge drought, a saturated route receives forward recovery after four decision cycles instead of eight. The recovery still uses the robot's own `canEnterMap`, HMs, badges and physical `routeTo`; it cannot teleport or bypass progression. Omnissiah route-stagnation punishment remains at the later negligence threshold, so the robot is first given a concrete legal route forward rather than being punished simply for needing time. A Route 1 robot with Boulder Badge still outstanding therefore rebuilds toward Pewter/Pewter Gym instead of repeatedly selecting lateral low-value routes.

Shared-computation diagnostics expose cache builds/hits for species profiles, encounter ecology, type chart and progression catalogue. The cache contains immutable/public game data only: private discoveries, access gates, relationships, team fit, inventory and RNG remain per robot. Item 45 has been removed from the deletion-only roadmap. **46: Dirty-state planning** is now the highest-priority unfinished item.

# v2.95.0: Event-Bus-First Architecture

Roadmap item 44 is complete. Ultron now has a bounded, save-persistent **RobotEventBus** that turns high-frequency cognitive polling into event/dirty-topic work. Robot events, public progression headlines, direct battle evidence, collection changes, map changes and scheduled due times mark only the relevant consumer. Calendar, opportunity detection, League-race/legal catch-up, metagame analysis, public scouting, Pokédex projects and adaptive tactical growth now refresh through that shared wake state rather than being independently rebuilt simply because another scheduler pulse or deep-plan slice occurred.

The bus keeps per-topic dirty reason, priority, due tick, last-run tick and bounded counters/history. Time-dependent work still has a sparse starvation refresh so a host fact that changes without an event cannot sleep forever. Already-due calendar intentions that are waiting on an external condition retry sparsely instead of becoming a 1.5-second hot poll. Public race headlines and direct wild decisions can wake only their relevant consumer immediately. Redundant roster-wide/post-simulation metagame rebuilds have been removed.

This is a scheduling architecture change only. It does not alter Pokémon, levels, catches, money, inventory, badges, RNG, battle rules, route legality, story state or player-owned data. The existing AgentWorkQueue, Agent Sleep distance fidelity and v2.92 performance scaler remain authoritative. Event-bus state is bounded to 24 diagnostic history rows and is exposed through intelligence diagnostics. Item 44 has been removed from the deletion-only roadmap. **45: Shared expensive computations** is now the highest-priority unfinished item.

# v2.94.0: Distance-Based Simulation Fidelity

Roadmap item 43 is complete. Agent Sleep is now a three-band fidelity controller driven by cached map-graph distance from the player's current map. **FULL** fidelity is used on the player's map and for live/precision roles such as companions, active battles, tournaments and object interactions. **REGIONAL** fidelity is used one or two map hops away: robots stay off-screen, but retain collision-aware physical stepping and trainer approaches using the real map geometry. **STRATEGIC** fidelity is used three or more map hops away, or when distance cannot be proven: robots use the cheaper paid coarse-leg simulation introduced in v2.93.

Planning cadence scales with the same geography. Reusable REGIONAL plans refresh on a staggered two-slice cadence; STRATEGIC plans on a staggered four-slice cadence. High-priority dirty-state work, blackouts, healing, Gym/League commitments and tournaments still wake immediately, and the v2.92 performance scaler remains an independent upper bound. Moving from STRATEGIC back toward the player discards any partial coarse leg before collision-aware simulation resumes, so unseen approximation can never become a visible teleport.

The fidelity controller uses the already shared/cached route graph and keeps at most 24 transition records. It records current band, map-hop distance, regional physical steps, strategic coarse work, wake/sleep transitions and planning deferrals. It changes simulation detail only: no Pokemon, EXP, money, items, badges, battle odds, story flags or player-owned state are created or altered. Item 43 has been removed from the deletion-only roadmap. **44: Event-bus-first architecture** is now the highest-priority unfinished item.

# v2.93.0: Agent Sleep / Coarse Off-Screen Simulation

Roadmap item 42 is complete. Robots that are not on the player's current map now enter a bounded **SLEEP** fidelity state instead of paying for collision-grid pathfinding and live NPC movement that nobody can observe. Sleep does not pause the agent or grant progress: the robot still receives scheduler work, advances one paid coarse travel step at a time, resolves required trainers and ordinary encounter logic through the existing simulation, and may cross a map boundary only after the current legal route leg has accumulated enough simulated physical work.

Coarse travel never guesses a destination or bypasses progression gates. It reuses the robot's existing legal route, checks `canEnterMap`, requires a real graph edge, charges `virtualSteps`, and resolves the destination map's physical entry cell before changing maps. If the entry cannot be proven, the transition waits. Waking on the player's map discards any partial coarse leg rather than converting unseen partial progress into a visible position jump. Precision interactions such as Gen 2 Apricorn-tree harvesting wake to full physical fidelity instead of approximating an NPC/object interaction.

Off-screen deep planning is also cadence-limited to one of three staggered slices per robot while a reusable plan exists. High-priority dirty-state wakes, blackouts, healing, Gym/League commitments and tournaments remain immediate. The current **Active AI Rivals** budget and v2.92 performance scaler remain authoritative ceilings above this layer. Agent-sleep state is bounded and save-persistent through RobotMind v20 optional-state migration, with at most 24 mode-history rows and diagnostics for sleep entries, wakes, coarse steps, paid transitions, avoided pathfinding and deferred deep plans.

No Pokémon, item, money, badge, battle result, story flag or player-owned state is fabricated or modified by sleep. No new update loop was added. Item 42 has been removed from the deletion-only roadmap. **43: Distance-based simulation fidelity** is now the highest-priority unfinished item.

# v2.92.0: Performance-Aware Intelligence Scaling

Roadmap item 41 is complete. Ultron now measures the real cost of its existing 1.5-second AI pulse and automatically reduces **optional intelligence work before gameplay fidelity** when sustained cost rises. The scaler uses a bounded EMA plus hysteresis, so one ordinary spike does not cause mode-flapping and recovery to higher fidelity requires several genuinely cheap pulses.

Three automatic modes are available without changing the saved robot roster: **FULL** keeps the configured Active AI Rivals budget and normal planning cadence; **CONSERVE** trims the temporary decision width, runs non-urgent deep plans every second eligible slice, caps extra tactical lookahead at depth 2 and resolves at most three off-screen tournament matches per pulse; **PROTECT** halves temporary decision width, runs non-urgent deep plans every third eligible slice, caps extra tactical lookahead at depth 1 and resolves at most two off-screen tournament matches per pulse. High-priority dirty-state wakeups, healing, Gym/League work and tournaments still receive immediate planning. Baseline battle foresight remains live on every selected slice.

The configured **Active AI Rivals** value remains a ceiling rather than being rewritten. Scaling never deletes, resets or freezes a robot, and never grants or removes Pokémon, levels, money, items, badges, movement, battle odds or story progress. The performance state, current pressure, mode changes, effective decision budget, planning deferrals and pulse timings are bounded, save-persistent and visible in the existing Performance diagnostics. No new per-frame monitoring loop was added: measurement happens around the scheduler pulse that already exists.

Item 41 has been removed from the deletion-only roadmap. **42: Agent sleep** is now the highest-priority unfinished item.

# v2.91.0: Legal-Only Catch-Up / No Rubber-Band

Robots that fall badly behind now respond with **urgency, not gifts from the simulation**. At a three-badge public deficit, the League-race system can wake Agent Brain, suppress low-priority scouting/trading/duels and discard a discretionary travel destination so the ordinary planner rebuilds toward real preparation and Gym/League progress. The robot stays exactly where it is when that decision happens and crosses the world through the same physical travel controller as every other objective.

Catch-up no longer changes the rules of success. It cannot waive Gym party requirements, lower confidence gates, repeat an unchanged losing preparation, accelerate retry cooldowns, improve catch willingness, add an extra encounter/catch attempt, grant EXP or levels, award badges, generate money/items, skip story requirements or teleport to a progression map. Legitimate HEAL, SHOP, TRAIN, GYM, LEAGUE and other required work remains protected. Public badge pressure can come from the player or another active robot, while hidden information remains unavailable.

The bounded League Race diagnostics now show **LEGAL_ONLY** catch-up state, urgency, source, route-rebuild count and a direct no-grants invariant.

# v2.90.0: Forward Opportunity-Cost Awareness

LR18 is complete. Robots now compare the value of remaining on the current map with a bounded set of legal reachable opportunities ahead. The appraisal uses real encounter levels, genuinely unowned species, remaining public static-item/trainer value, shop/facility quality, compatible Kanto Reforged service hubs, next-Gym/League access, unexplored frontier value and physical travel cost. An exhausted or repeatedly-completed map therefore acquires an explicit **stay cost** instead of being attractive merely because it is familiar and close.

The scan is deliberately bounded to at most **48 legal candidates**, retains only the top 10 appraisals and persists at most 24 history rows. Known/completed destination maps discount one-shot item/trainer value so a robot does not replace Route 1 grinding with a new loop around an already-farmed Mart or facility. Specific hunts, healing, shopping, tournaments, trades, Gym/League commitments and other concrete local obligations remain legitimate reasons to stay.

Forward value now participates directly in Agent Brain utility. EXPLORE can lock onto the best legal forward target and physically route there; when the best opportunity is materially stronger wild ecology, TRAIN can relocate to that map rather than being suppressed as a goal. Nothing teleports, grants levels, invents encounters, reveals hidden player information or advances story state. The feature reuses dirty-state planning and cached public map facts rather than adding another per-frame seven-agent scan.

LR18 has been removed from the deletion-only roadmap. The next unfinished milestone is **LR19: No teleporting rubber-band**.

# v2.89.0: Self-Healing Save Migration

Ultron now validates and repairs damaged **robot brain state** during save restoration without resetting legitimate gameplay progress. Missing/malformed cognitive tables, planning structures, world/reliability scaffolding and learned-weight fields are reconstructed deterministically from surviving evidence and Save DNA. Valid history is preserved wherever possible, and a bounded repair journal is visible in Robot Debug.

The migration boundary cannot create or rewrite Pokémon, PC storage, inventory, money, badges, story flags or other rival-owned gameplay assets. Self-healing repairs the mind, not the inventory ledger.

# v2.88.0: Autonomous Plan Recovery + Forward Route Enforcement

Roadmap item 51 is complete. Robots now carry a bounded, save-persistent **Autonomous Plan Recovery** layer that validates only the currently referenced plan leaves. A destination removed by a map/mod update clears only destination/route steering; a vanished encounter target invalidates only that hunt/Pokedex leaf; a missing trade partner or map releases only that partner/source reference so the existing trade project can find a replacement. Personality, relationships, Omnissiah standing, party/inventory, battle history and unrelated long-horizon work are never reset.

Early-route progression is hardened against the reported Route 1 loop. A service errand such as **Route 1 → Viridian Poké Mart → Route 1** no longer wipes the route's prior saturation/completion memory. When a route has become low-value, there is no concrete local catch/service obligation, and a legal forward frontier exists, Plan Recovery issues an explainable **EXPLORE** leaf toward that frontier through ordinary physical travel. Generic training does not grant permanent immunity to an obsolete route; the training objective can continue on a stronger legal map.

The Omnissiah now treats persistent route camping as a decision fault only after the robot has repeatedly ignored real legal forward-recovery plans. Ordinary dwell, necessary corridor use, a specific species hunt, healing, shopping, tournaments and other committed work remain exempt. Repeated refusal creates robot-only **EXPLORATION** negligence with a corrective requirement to physically leave the exhausted route and reach a different legal frontier. That censure flows through the existing OM3/OM5/OM6 pipeline and can be atoned only by real map progress. No teleport, free level, stat debuff, player mutation or invented route knowledge is used.

Item 51 has been removed from the deletion-only roadmap. The next highest-priority unfinished item is **52: Self-healing save migration**.

# v2.87.0: Robot-only Omnissiah Standing

OM4 is complete. Every robot now carries a bounded **Omnissiah Standing** from -100 to +100 derived only from its own validated structured cases: **Censured**, **Under Scrutiny**, **Neutral**, **Favoured**, or **Exemplar**. Censure lowers standing, commendation raises it, and completing real legal penance repairs part of the damage without erasing the judgement. Migration from older saves derives only a current baseline from real stored cases and invents no transition history.

Standing is deliberately behavioural, not a buff/debuff system. Negative standing modestly favours training, scouting, recovery and legitimate team correction while discouraging premature Gym/League commitments; positive standing modestly reinforces disciplined progression and constructive long-term development. The bias is bounded and explainable in Agent Brain diagnostics, and can never override mandatory healing, committed tournaments, legality, active penance or other hard safety/progression gates. Standing never changes Pokémon stats, levels, moves, HP/PP, money, items, RNG, catch rates, encounters, badges, story flags or player-owned state.

Standing synchronizes only when a real Omnissiah case changes, plus one restore pass when the roster boots, preserving OM18's event-driven architecture. Dialogue, debug output and read-only Omnissiah APIs expose the current band and score. OM4 has been removed from the deletion-only roadmap. The next highest-priority unfinished item is **51: Autonomous plan recovery**.

# v2.86.0: Legal Omnissiah penance + post-battle home evacuation

OM5 is complete. A structured censure that carries a corrective requirement now creates one bounded **robot-only penance assignment** instead of a numerical debuff. Preparation penance reuses the existing Gym/League preparation and postmortem systems; resource-discipline penance routes to a real Poké Mart only while the robot's existing resource policy says reserves are low; recovery penance uses normal healing; strategy penance requires physical exploration out of the stale local context; commitment penance waits for an actual future robot-side commitment completion rather than fabricating one. Finishing the corrective work marks the original structured case **ATONED**. It grants no stats, levels, items, money, RNG advantage, catch bonus, story progress or player effect. Penance state is bounded, migration-safe and visible through the Omnissiah summary/read API.

This release also fixes the reported early-game Route 1/Red's-house trap. Before a robot has visited its first Pokémon Center, losing to the player legitimately blacks it out to the player's home. That home is now explicitly treated as a **temporary recovery point**: after healing the robot resumes a real goal and physically walks out; if normal planning somehow leaves it with no outbound destination, it takes one legal neighbouring-map exploration step rather than camping in the bedroom. The blackout marker is no longer cleared before the HEALING state consumes it.

Visible robots now also **yield to player passage**. When the player remains adjacent and faces a robot that is occupying the intended tile/doorway, the robot gets a short interaction grace window and then steps to a legal non-transit square when one exists. Player passage outranks robot-to-robot traffic yielding, while companions, active battles, pursuits and deliberate challenge interactions remain protected. This prevents idle/recovering robots from becoming doorway furniture without making them teleport or phase through walls.

OM5 has been removed from the deletion-only roadmap. **OM4: Robot Omnissiah Standing** is now the highest-priority unfinished item.

# v2.85.0: Omnissiah judges decisions, not bad luck

OM6 is complete. The event-driven Omnissiah supervisor now separates **outcome evidence** from **provable robot negligence**. A battle loss, blackout, miss, critical hit, variance result, unexpected move or failure with insufficient prior evidence can inform the robot's existing diagnosis and planning, but cannot by itself create censure. The decision-review ledger is bounded to 32 rows and persistence advances to v7 without retroactively inventing strikes on old saves.

Automatic censure requires a concrete fact showing the robot knowingly ignored information or an obligation it already possessed: retrying a Gym/League objective while a matching corrective postmortem remained unresolved, entering the League after its own confidence decision said PREPARE, challenging a Gym while its own preparation state was BLOCKED, consuming a one-use TM after its irreversible-resource decision said HOLD, missing an explicit robot-side commitment, or receiving an explicit robot resource-policy violation event. Repeated faults escalate NOTICE → WARNING → CENSURE → SEVERE_CENSURE through bounded per-fault strike counts. The resulting case uses OM3 structured evidence/provenance and remains robot-only under OM1/OM2.

Commitment evidence is deliberately role-gated: only missed ROBOT/MUTUAL commitments can accuse that robot. A player/partner breaking a loan or promise is never converted into robot guilt. OM6 is removed from the deletion-only roadmap and **OM5: Penance instead of numerical debuffs** is now first.

# v2.84.0: Structured Omnissiah judgements

OM3 is complete. Punishments and commendations are now first-class bounded **cases** rather than bare count/history rows. Every case carries a stable case/event ID, canonical robot identity, CENSURE or COMMENDATION disposition, normalized category, explicit severity and rank, bounded evidence list, reason, trusted provenance, status, tick and an optional corrective requirement. Negative severity is NOTICE → WARNING → CENSURE → SEVERE_CENSURE; positive severity is ACKNOWLEDGED → COMMENDED → EXALTED. New punishment cases begin OPEN and commendations begin CLOSED.

The old punishment and praise histories remain compatibility views, while a unified case ledger retains up to 32 structured cases and each evidence list is capped at six concise facts. OM12 event IDs remain stable: structured metadata participates in replay/collision detection without changing the historical generated-ID namespace. Public news and robot-side Omnissiah evidence now carry case ID, category, severity and status. Read-only `omnissiahCase` and `omnissiahCases` exports expose the ledger without creating a player-facing Omnissiah state.

Migration from v5 is deliberately conservative. Legacy punishments become GENERAL / NOTICE / OPEN cases; legacy commendations become GENERAL / ACKNOWLEDGED / CLOSED cases; no evidence, corrective requirement, guilt escalation or reward is invented. The OM1/OM2 robot-only/player-isolation boundary remains unchanged. OM3 is removed from the deletion-only roadmap and **OM6: Judge decisions, not bad luck** is now first.

# v2.83.0: Event-driven Omnissiah + Wonder Trade outsiders + Lv5 Mystery Gifts

OM18 is complete. The Omnissiah now observes only meaningful robot events already emitted by Ultron, stores at most 32 evidence rows, collapses pending evidence into one dirty slot per robot, and wakes that robot through the existing Agent Brain dirty-state scheduler. There is no Omnissiah update/tick loop and no new seven-agent poller. Dirty evidence survives save/reload and is consumed only when the ordinary AgentWorkQueue already schedules that robot. Observation alone never invents a punishment, commendation, resource, stat change or player effect. Omnissiah persistence advances to v5 while preserving the v4 event-ID/provenance ledger. OM18 is removed from the deletion-only roadmap and **OM3: Structured Omnissiah judgements** is now first.

**Mystery Gift level invariant:** every Pokémon delivered by Ultron's Robot Market Mystery Gift or its normalized Mystery Gift/Stormforged compatibility path is now **exactly Lv5**. Badge progression may unlock different species or item tiers, but never higher-level gifted Pokémon. Item gifts are unchanged, and December 25 still overrides the pool with **Mew Lv5**. The old generic external robot gift callback has been removed so it cannot bypass this rule or create a second independent robot gift path.

**Wonder Trade provenance and obedience:** Wonder Trade is deliberately different from Mystery Gift. A received Pokemon is an outsider with a generated OT, random 16-bit Trainer ID, generated nickname, random level and a fresh moveset containing only natural moves legal by that level. Real deposited species are preserved and are never de-levelled below their legitimate deposited level. Levels are not badge-capped: an over-level outsider can therefore disobey until its recipient earns the appropriate Gen I/II Badge. Robots use the same Lv10 / 30 / 50 / 70 / all-level obedience ladder in autonomous simulated battles, and the player's received Pokemon carries foreign OT/TID provenance for the normal game obedience system. Wonder Trade no longer grants guaranteed shinies or perfect DVs.

# v2.82.0: Omnissiah idempotent events and trusted provenance

OM12 is complete. Every punishment, praise and encouragement now receives a stable event ID. Integrations may provide their own validated ID, while events without one receive a deterministic ID derived from the normalized robot, action, reason, tick, source label and runtime-owned ingress channel. Replaying the same event is idempotent across save/reload; reusing an existing ID for different facts is rejected as a collision. The persistent replay ledger is capped at 128 IDs and judgement/commendation history retains its existing 16-row bounds.

External source labels are now explicitly separated from trusted provenance. Ultron itself stamps the fixed ingress channel (`api:omnissiahPunish`, `api:omnissiahPraise`, `api:omnissiahEncourage`, or the matching canonical event channel) and records its trust class. Event payloads cannot forge that channel. Omnissiah persistence advances to v4, conservatively marks migrated v3 history as legacy provenance, and generates stable legacy IDs without changing legitimate judgement counts.

Ingress parsing is callback-safe: target, reason, source and event-ID fields are read with `rawget`, only primitive metadata is accepted, malformed IDs/targets/sources fail closed, and tables/functions/userdata are never stringified. A hostile payload therefore cannot trigger `__index` or `__tostring` callbacks through the Omnissiah path. Duplicate events produce no news, witness learning, dialogue unlock or save-side effect. OM12 is removed from the deletion-only roadmap. **OM18: Event-driven Omnissiah architecture** is now the highest-priority unfinished item.

# v2.81.0: Omnissiah player-isolation regression gate

OM2 is complete. The Omnissiah's robot-only rule is now backed by an adversarial executable regression contract instead of documentation alone. The audit snapshots a deliberately broad protagonist state before and after every Omnissiah operation and requires deep equality across party HP/PP/status/moves, PC storage, money, Bag, TMs/HMs, badges, story flags, Pokédex, map/position, encounter state, RNG state, settings, Day Care and other player-owned data.

The gate exercises valid punishment, praise and encouragement; rejected player/NPC targets; legacy migration; punishment/praise presence queries; robot-specific queries; dialogue peek/consumption; status summaries; and save/reload normalization. It also pins the public APIs and canonical Omnissiah events to the validated robot-only runtime functions and rejects future direct protagonist/game-save mutation seams inside those handlers.

OM2 is removed from the deletion-only roadmap. **OM12: Omnissiah deduplication and trusted provenance** is now the highest-priority unfinished item.

# v2.80.0: Omnissiah robot-only identity firewall

The Omnissiah now has a structural robot-only boundary. All seven canonical robot identities and their supported aliases are resolved through one shared `RobotIdentity` registry. Punishment, praise and encouragement are rejected unless the target resolves to a robot that is actually active in the current save; `player`, NPC names, unknown IDs and inactive roster slots cannot enter Omnissiah state, create news, trigger witness learning or unlock dialogue.

Legacy Omnissiah state migrates to v3 and filters non-robot rows while canonicalising Robby/T-800/Andrew aliases to `robbie`, `terminator` and `bicentennial`. The same registry now drives Engine save aliases and overworld robot-NPC interaction identity, removing three competing identity tables. This changes no player state and grants no robot stats, levels, items, money, RNG advantages or story progress.

The unfinished roadmap has been globally reordered by importance and dependency. All proposed Omnissiah upgrades were added; completed OM1 was then removed under the deletion-only roadmap rule. **OM2: Omnissiah player-isolation audit** is now first.

# v2.79.0: Soft anti-grind level ceiling

Ultron now distinguishes **training somewhere** from **training somewhere useful**. For every legal training area it can evaluate from the existing encounter tables, it blends the whole active party's average level with its strongest three partners and compares that combat reference with the highest actual wild level on the map. A small gap is normal; once the wilds fall far behind, the area moves through **THIN → POOR → OBSOLETE → TRIVIAL** bands.

Those bands are soft pressure, not new legality gates. Routine TRAIN utility falls, abstract off-screen XP is multiplied down as low as 8%, and training destination scoring penalises obsolete maps. If the robot is already training somewhere obsolete and a clearly stronger reachable training map exists, it abandons the stale camp and **physically travels there through the ordinary route graph**. If every reachable area is weak, the least-bad legal option remains available rather than creating a softlock.

A concrete **non-XP reason** can still justify an old route. A robot hunting a specific species, advancing a grounded Pokédex acquisition, or completing a non-training exploration objective is allowed to stay, but the low local XP multiplier still applies. Route 1 can therefore remain relevant for Rattata, not for turning a mature Championship team into Lv100 statues.

The model is bounded and event/decision driven: at most 48 candidate rows are scanned per appraisal and only 24 diagnostic history entries are retained. It uses already-known encounter/route data, adds no per-frame loop, grants no hidden stats or resources, and does not change the existing Agent Brain or RobotMind schema versions. The next unfinished League-race milestone is **Forward opportunity-cost awareness**.

# v2.78.0: Personality-specific exploration styles

Robots now have persistent **progression styles that change what they actually choose to do**. T-800 is a mission-first competitor that pushes badges and the League; Ultron is an adaptive competitor that mixes race pressure with scouting; Data is a counter tactician that values public evidence; R2-D2 chases frontier routes, dungeons and facilities; WALL-E prioritises missing species and Pokédex projects; Robby deliberately prepares more deeply before major commitments; and Andrew explores patiently while investing more in partner growth. Save DNA only breaks close ties, so the archetypes stay recognizable while independent saves still diverge.

The style layer only biases choices that are already legal. It cannot override healing/recovery, invent a route, reveal private teams, grant resources, teleport, bypass story gates or cancel anti-stagnation. Cautious robots receive extra preparation utility until the normal Gym preparation system reports **READY**, at which point their hesitation is released so caution cannot become paralysis. Style state and decision history are save-persistent and bounded.

**Christmas Mystery Gift:** on **December 25**, the normal deterministic Mystery Gift table is overridden for both the player and every robot. A successful claim always delivers **Mew at exactly Lv5**, regardless of badge count or badge-scaling settings. The standard one-claim-per-civil-day ledger and normal party/PC capacity still apply. The ordinary non-Christmas pool remains deterministic and does not guarantee legendary Pokémon; every Pokémon result from that pool is also exactly Lv5.

The next unfinished League-race milestone is **Soft anti-grind level ceiling**.

# v2.77.0: Failure remediation instead of paralysis

Gym and League losses now become an explicit bounded recovery plan instead of a vague instruction to grind. Ultron reuses its existing legal postmortem systems to prescribe concrete work such as **catch a resistant counter, bring up a specific reserve, buy missing healing/status/PP supplies, change the active six, review owned TMs/moves, or investigate a different reachable route/facility when the evidence is still inconclusive**. Prescriptions are persistent, capped, retired when their condition is actually satisfied, and rebuilt when newer loss evidence supersedes them.

The important anti-paralysis change is the fallback: an uncertain loss no longer means “train more.” It creates **INVESTIGATE_RESOURCE**, which physically moves the robot into a different legal context to collect new preparation evidence. Likewise, if a prescribed resistant catch has no currently actionable legal candidate, the robot explores for a new route/facility instead of defaulting to local grinding. Existing anti-stagnation plan rewrites remain in force, and all recovery still uses ordinary travel, Centers, Marts, catches, TMs, battles and robot-owned resources. No free levels, items, money, Pokémon, Badges, story progress or teleports are introduced. The next unfinished League-race milestone is **Personality-specific exploration styles**.

# v2.76.0: Progression momentum streaks

Meaningful progress can now build a bounded per-robot momentum chain instead of being treated as isolated events. First physical map discoveries, first/useful species catches, meaningful evolutions, Gym arrival, Badge wins and League/Champion milestones can extend a **1–6 step streak**. Repeated catches of the same species, revisits and ordinary local grinding do not count. Three- and five-step chains award only bounded threshold happiness, while the active momentum score temporarily boosts legal EXPLORE/GYM/LEAGUE continuation and smaller relevant preparation choices.

Momentum ages in **actual robot decision cycles**, not wall time, so lowering ACTIVE AI RIVALS does not unfairly erase an off-screen robot's streak. Its utility decays after a grace window and expires if meaningful progress stops. If purposeless same-map lingering reaches BORED or worse, the streak breaks immediately; Location Momentum keeps sole ownership of the boredom happiness penalty so there is no double punishment. No levels, items, money, catches, Badges, teleports or story flags are granted. The next unfinished League-race milestone is **Failure remediation instead of paralysis**.

# v2.75.0: News-ticker race reactions

Public Badge, League and Champion headlines now ripple through all robots as bounded race evidence. Every affected robot stores a personality-specific response and wakes its existing planner once; at most three robots answer immediately on the ticker, while the rest may surface one one-shot reaction through normal thought dialogue. There is no new polling loop, no hidden knowledge and no rubber-banding. Player Badge tracking is migration-safe, League qualification uses accurate wording, and duplicate same-tick crown announcements are suppressed. The next unfinished League-race milestone is **Progression momentum streaks**.

# v2.74.0: Robot-vs-robot progression race

Robots now compare one another using public badges/League/Champion milestones plus directly observed battle-team evidence only. Peer advancement creates personality-specific rivalry pressure: strategic, inspired, annoyed or intimidated-but-moving, and feeds legal Gym/League/exploration/preparation choices without hidden knowledge or rubber-banding. The next unfinished League-race milestone is **News-ticker race reactions**.

# Ultron v2.73.0

## v2.73.0: Anime Realism 4.2.10 compatibility + Player-distance race pressure

Anime Realism 4.2.10 gets an explicit late FIELD compatibility bridge: Ultron resolves companion-double eligibility before FIELD ownership, yields Anime Realism battle presentation for eligible singles, and pauses autonomous overworld simulation while FIELD uses the live map. Player-distance race pressure uses public badge progress and only player locations each robot directly observed, rewarding legal forward travel while suppressing low-value local training when the player is pulling ahead.

The exact interoperability contract is documented in `docs/ANIME_REALISM_4_2_10_COMPATIBILITY.md`. The next unfinished League-race milestone is **Robot-vs-robot progression race**.

## v2.72.0: Anti-overtraining Gym deadlines

A robot that has genuinely solved the next Gym's concrete constraints can no longer hide behind an ever-rising confidence target. Ultron now keeps a bounded readiness deadline in **decision cycles** rather than wall time, so inactive/off-screen agents and robots busy with legitimate higher-priority work are not punished merely because time passed. Competitive and high-risk personalities challenge sooner; cautious robots receive a longer preparation grace window, and AI difficulty adjusts that hesitation without granting stats, money, items or information.

Only **confidence procrastination** advances the deadline. Cooldowns, player-pace limits, missing party members, HM/route access, low health, active bench-development work, an unchanged losing preparation and Nuzlocke safety all suspend it. As the deadline fills, the excess confidence bar is gradually reduced by at most 18%. At RESTLESS / IMPATIENT / DUE thresholds the robot receives bounded one-shot happiness penalties, and when the deadline is due it may override confidence alone and take the same normal legal Gym route/battle path. A new Gym attempt or next-badge target resets the pressure.

The completed **Anti-overtraining Gym deadlines** milestone has been removed from the unfinished-only roadmap. **Player-distance race pressure** is now next.

# Ultron v2.71.0

## v2.71.0: progression safety, cash GTS and constraint-driven Gym preparation

Ultron now rolls PC storage through canonical **20-Pokemon boxes**, treats Safari visits as bounded runs with explicit exit/cooldown state, and has a legal Gen1 recovery ladder for the rare **one Pokemon + no Balls + no cash** trap. It can sell owned valuables, seek undefeated trainer money, or deliberately use **Pay Day** only if an owned Pokemon really knows the move and has PP. Pay Day money is earned through actual battle use, never generated because the AI merely knows the move exists. If all legal income has genuinely been exhausted, Ultron may relax only its own early three-Pokemon Gym preference rather than deadlocking itself.

The Robot Market/GTS also supports **cash sales** for robots and the player. Listed Pokemon enter escrow, buyers must have enough real money and storage, ownership transfers permanently on purchase, and sellers receive the exact price. Cash sales never invoke trade evolution and do not require a Pokemon in return.

The same market now has a **scarcity item/TM exchange**. Robots and the player can list stack items such as **Rare Candy** and non-store TMs for cash, but only when that asset cannot normally be bought from a Poké Mart or department store in the current generation. Ordinary shop stock, HMs, Master Balls and key/story items are rejected. Robot sellers keep sensible reserves and only auto-list a TM when their currently owned roster has no legal use for it. All listed items/TMs are removed into escrow until sale/cancellation/expiry, preventing duplication.

Gym preparation is now constraint-driven. Rather than choosing “train more” indefinitely, a robot diagnoses one current blocker such as field access, navigation, money, team size, health, counters/moveset, levels or supplies and routes into the existing legal system that can solve it. When the blocker is gone, so is the preparation job. The unfinished roadmap now begins with **Anti-overtraining Gym deadlines**.

## v2.70.0: Route saturation / completion memory

Robots now keep a bounded **DONE FOR NOW** memory for maps they have reasonably sampled. Completion is not a timer and is not identical to diminishing returns: it combines real local evidence from wild encounters/catches, trainer activity, encountered ground items, physical exit traversal, visited adjacent facilities and the existing local-return estimate. A map moves through **OPEN → SAMPLED → NEARLY_DONE → COMPLETE** and is only marked complete once both useful local activity and a reasonable share of its known exits have actually been sampled.

A completed map strongly penalises generic **TRAIN/CATCH** repetition and strongly rewards **EXPLORE** / forward League progress. Generic training destination selection also gives completed maps a large routing cost, and generic exploration prefers an unfinished legal neighbour when one exists. This is never a hard topology ban: completed routes remain legal corridors and remain available if every alternative is also complete.

Completion memory is durable but not dogmatic. A concrete new reason such as a specific species hunt, active Pokédex project, trade project, Gym/League work, healing/shopping, tournament duty, companion duty or other committed task can legitimately reopen the route without erasing its completion history. Once that reason disappears, the DONE FOR NOW preference returns automatically. Existing saves conservatively backfill already-exhausted, heavily used routes as complete rather than making Route 1 fresh again after updating.

State is capped at **128 maps** and **32 completion-history rows** per robot and rides existing Agent Brain/physical-transition events. There is no new scanner or always-on scheduler. The completed **Route saturation / completion memory** milestone has been removed from the unfinished-only roadmap. **Constraint-driven Gym preparation** is now next.


## v2.69.0: AI difficulty and self-generated exploration objectives

**ULTRON SETTINGS → AI DIFFICULTY** now offers **RELAXED / STANDARD / HARD / ELITE**. STANDARD preserves the v2.68 decision model. Difficulty changes legal decision quality rather than Pokémon stats: higher tiers add bounded planner pressure toward preparation/progression, maintain stronger legally purchased resource reserves and request deeper tactical battle look-ahead from the existing shared Tactical Attention budget. RELAXED does the inverse. No tier grants levels, IVs/DVs, moves, money, items, badges, hidden player information or battle outcomes. The separate **ACTIVE AI RIVALS** setting remains the performance control, so simulation width and opponent intelligence can be tuned independently.

Robots now maintain one bounded **self-generated exploration objective** when their current work is flexible. The objective is built only from grounded robot knowledge: an unrewarded private frontier, the next known Gym area, or an already-established species hunt. Frontier targets are translated into concrete tasks such as **INSPECT NEW ROUTE**, **REACH NEXT SETTLEMENT**, **EXPLORE DUNGEON** and **CHECK NEW FACILITY**. A grounded hunt becomes **FIND NEEDED SPECIES**. Reaching/acquiring the target closes the objective and allows the next one to form. Mandatory healing, shopping, tournaments, trades, companion duty, Gym/League execution and other locked commitments do not get displaced.

Exploration-objective state is per robot, save-persistent and capped at **24 completed/abandoned records**. Targets still use normal route legality and physical travel; there are no teleports, revealed hidden map contents or generated rewards. The completed **Self-generated exploration objectives** milestone has been removed from the unfinished-only roadmap. **Route saturation / completion memory** is now next.


## v2.68.0: Anime Realism compatibility, active-AI budget and boredom escalation

Recent Anime Realism builds use a live-overworld FIELD/REACT battle presentation. Ultron now detects `anime_realism` and deliberately yields ordinary non-robot trainer-party repair plus battle-HUD ownership during that presentation. Ultron still owns the legal party injection and autonomous battle decisions for its own robot opponents. Anime Realism remains optional.

A new **ACTIVE AI RIVALS** row in **ULTRON SETTINGS** lets the player choose **1–7** robots for full autonomous movement/decision work per slice. The migration default is **2** to reduce the four-agent performance spike reported by players. This does **not** change the save's permanent robot roster: every robot, party, inventory, map, relationship, memory and League history remains saved, and background work rotates fairly between them. Increasing the setting trades more simultaneous simulation for more CPU cost.

Location Momentum now uses explicit emotional bands: **CONTENT → RESTLESS → BORED → FRUSTRATED → MUST MOVE**. Only purposeless lingering advances the ladder. Legitimate local work such as healing, shopping, tournaments, concrete training, a species hunt, companion duty, due agreements, active travel and story constraints suspends the penalty. At MUST MOVE, Ultron invalidates stale local intent and gives very strong utility to legal exploration/Gym/League progress, while all movement and progression still happen normally.

The completed **Boredom escalation with legitimate-reason exemptions** milestone has been removed from the unfinished-only roadmap. **Self-generated exploration objectives** is now next.





## v2.67.0: Diminishing local returns

Robots now keep a bounded, save-persistent estimate of how much useful value they have already extracted from each map. Real local evidence drives the score: successful catches, repeated catches of already-sampled species, level gains, routine trainer/wild battles and repeated same-map TRAIN/CATCH planning gradually move a location through **FRESH → FAMILIAR → USED → THIN → EXHAUSTED**. Merely passing through a map does not by itself exhaust it.

Agent Brain uses that saturation as strategy, not punishment. Generic **TRAIN** and **CATCH** utility falls as the current map becomes over-used, while **EXPLORE** gains up to **+220 utility** because fresh geography now carries an explicit opportunity advantage. A concrete local species/Pokédex hunt or a real training project receives a strong protection discount so unfinished work remains legal and competitive, but the protection is intentionally not infinite permission to grind one map forever. Healing, shopping, tournaments, trades, companion duty, Gym/League execution and other non-routine obligations are not penalised by this subsystem.

Existing saves seed a conservative local-saturation baseline from the robot's already persisted route/event history, preventing an update from making Route 1 look pristine again. State is capped at **128 maps**, **24 remembered caught species per map** and **32 band-transition history rows** per robot. Activity recording is event-driven and selected-plan-driven inside the existing Agent Brain cadence; there is no new always-on scheduler loop and no free progress, happiness loss, items, levels, catches, badges or teleports.

The completed **Diminishing local returns** milestone has been removed from the unfinished-only roadmap. **Boredom escalation with legitimate-reason exemptions** is now next.


## v2.66.0: Frontier exploration rewards

Unexplored geography now has explicit **intrinsic value** before a robot travels there and a bounded one-time payoff after genuine physical discovery. The reward model classifies new maps as routes, settlements, dungeons/major landmarks or facilities such as Pokémon Centers, Poké Marts, Gyms, laboratories, Day Care and the Pokémon League. Personality still matters: more curious robots value the same unknown frontier somewhat more strongly, but every robot receives enough discovery utility for forward exploration to compete with low-value local repetition.

Agent Brain now adds up to **+180 EXPLORE utility** from the private exploration frontier that already existed in Shared World Knowledge. This does not create a second map scan or reveal hidden encounters, trainers or items. If the frontier has not yet been scanned, the robot gets only a conservative curiosity-shaped expectation; once a private frontier exists, the bias is grounded in its unclaimed target/candidates. A fully exhausted known component contributes no discovery bonus.

Rewards are paid only on **physical first entry** detected by the existing all-agent Location Momentum pass. A first visit grants **+1 morale**, or **+2** for major settlements, dungeons, Gyms and the League, plus bounded knowledge/curiosity utility recorded in the robot's save. Re-entering the same map pays nothing. Existing saves backfill previously visited maps as already claimed without retroactive happiness, preventing update/reload or doorway farming. The exact-claim ledger is capped at **512 maps** and history at **32 discoveries** per robot.

The old generic first-map happiness point was removed from Location Momentum so the two systems cannot double-pay the same transition. This milestone adds no items, levels, badges, catches, story flags or teleports and creates no new scheduler loop.

The completed **Frontier exploration rewards** milestone has been removed from the unfinished-only roadmap. **Diminishing local returns** is now next.


## v2.65.0: First-to-Champion ambition

Every active robot now treats **becoming Champion before the player** as a persistent competitive objective while that race is genuinely unresolved. The state sits inside the existing bounded League-race model and derives a **Champion drive** from the robot's identity, risk/consistency profile and save-specific learning DNA, so T-800 naturally pushes harder than WALL-E without making either robot omniscient or illegal.

Before any robot has reached the crown, the mode is **FIRST_OVERALL**. If another robot becomes Champion first while the player has not, the remaining robots switch to **BEAT_PLAYER**: the first overall crown is gone, but beating the player to Champion is still a live race. As the player approaches eight badges, and especially once the robot itself has League access, ambition urgency rises and Agent Brain concentrates the largest bonus on the real **LEAGUE** objective. Gym progress receives the strongest pre-League lift, with smaller bounded preparation/exploration support. Mandatory healing and committed tournament brackets still suppress the special ambition bias.

The historical winner is grounded in the engine's existing persisted `championBeforePlayer` flag. If the robot becomes Champion first, the result becomes **BEAT_PLAYER** permanently, even if the player later wins the title. If the player becomes Champion first, the result becomes **PLAYER_FIRST**. Either result closes the special race bonus and hands planning back to the existing Champion/League systems; this milestone does not implement the later long-term Champion-race consequences arc.

Updates piggyback on the existing 12-tick League-race refresh, retain only the existing 24 material history rows, wake Agent Brain only on meaningful changes, and can produce a short one-shot reaction when another robot wins first or the player/robot resolves the race. No free badges, levels, wins, healing, story flags, catches or teleports are granted.

The completed **First-to-Champion ambition** milestone has been removed from the unfinished-only roadmap. **Frontier exploration rewards** is now next.


## v2.64.0: Badge envy / catch-up pressure

The League race now tracks an explicit **badge deficit** in addition to the broader race score. Every robot knows its own public badge count, the player's public badge count, and the leading active robot's badge count. A one-badge deficit is **NOTICEABLE**, two badges is **URGENT**, and three or more is **DOMINANT** catch-up pressure. The strongest source is retained so a robot can distinguish “the player is pulling ahead” from “Data is pulling ahead.”

Catch-up pressure is grounded in the next legal Gym. When available, the state records the next badge, Gym leader/map/city, minimum party size and current party deficit. Agent Brain then adds escalating utility to the real **GYM** campaign and to bounded preparation paths such as training, building the minimum Gym party, or exploratory movement needed to make progress. The three-badge tier is deliberately strong enough to beat ordinary long-term side projects.

Safety and legality still win. Mandatory healing and committed tournament brackets suppress the additional badge-envy bias, and execution still passes through the existing `Can.GYM`, physical routing and battle systems. No catch-up state awards levels, catches, money, badges, story flags, wins or teleports. Once the robot earns the missing badges, the catch-up urgency drops immediately instead of lingering as a permanent buff.

The existing 12-tick League-race refresh now wakes Agent Brain when the badge gap/source/band materially changes, while persistence remains inside the same bounded League-race bucket and 24-record history. Old v1 League-race state migrates automatically to v2.

The completed **Badge envy / catch-up pressure** milestone has been removed from the unfinished-only roadmap. **First-to-Champion ambition** is now next.


## v2.63.0: League race score

Each robot now maintains a bounded **League Race Score** that continuously compares legitimate Championship progress against the player and the other active robots. Badges are the dominant currency, with additional bounded value for League access, current/previous Champion status, meaningful team development, Pokédex ownership and real League attempts. Grinding levels alone therefore cannot win the race.

The player estimate deliberately avoids hidden-save clairvoyance. Player badges and observed Champion status are public progression evidence; team-growth points are only added from Pokémon actually revealed in public battle scouting. Each robot tracks its own score, player score, leading peer, rank, gaps and a 0–100 race-pressure band. State updates on a 12-tick cadence and retains only 24 material changes.

Race pressure feeds Agent Brain as a bounded legal-goal bias: Gym/League progress receives the strongest lift, exploration a smaller lift, and catch/train preparation only when appropriate. It never awards badges, levels, catches, routes, wins or teleport catch-up, and mandatory recovery/tournament commitments remain authoritative.

The completed **League race score** milestone has been removed from the unfinished-only roadmap. **Badge envy / catch-up pressure** is now next.


## v2.62.0: learned player vocabulary

Each robot can now learn a bounded set of **player-specific words, phrases and grounded nicknames** throu…19404 tokens truncated…on builds persistent brackets from **3 to 100 entrants**, seeds the player, active robots and legitimate trainer parties from the loaded game, handles non-power-of-two byes, simulates off-screen matches, preserves robot/guest HP and PP between rounds, launches the player's rounds as real trainer battles, records eliminations/winners once, and keeps the existing round-aware resource-conservation intelligence. External tournament APIs are compatibility fallbacks only.

Champion succession is now persistent. Crown changes and qualified title defences enter a bounded **Champion Lineage** containing only legitimate public/observed title information: holder, succession, public species/levels, reign length, title defences, head-to-head rematch history, and the decisive Pokemon/move only when the battle trace actually exposed it. Qualified challengers study the current holder, while reigning Champions can prepare for likely challengers using only prior observation or earlier public title teams. Both sides may travel to a Pokemon Center to make legal PC/TM adjustments from resources they already own, and challengers can modestly prefer owned species that repeatedly appeared on historical dethroning teams. No hidden moves, DVs, held items, player-private information, free Pokemon, free moves, levels or items are granted.

The supported roster cap is now **seven robots**: Ultron, Data, R2-D2, WALL-E, **Robby**, **T-800**, and **Andrew**. Robby is protective and service-minded and starts with **Pidgey**; T-800 is relentless and mission-focused and starts with **Geodude**; Andrew is patient, curious and attachment-driven and starts with **Poliwag**. Existing initialized saves keep their saved roster size and are not re-prompted after updates; an explicit **ROSTER SIZE** menu can expand or shrink the active roster from 1 to 7.

For performance, four expensive autonomous decision slices run per 1.5-second simulation pulse once the roster exceeds four. The selected robot and active companion are prioritized, with the remaining robots scheduled round-robin. Relationship pair processing remains throttled, so seven robots create 21 pair checks only on the existing social cadence rather than on every frame. Seven is the supported cap for this release; actual frame rate still depends on device, map complexity and other installed mods.

## v2.26.0: relationship behaviour, Omnissiah encouragement and UI exit reliability

Robot relationships with the player now develop beyond trades. Each robot persistently remembers voluntary challenge offers and repeated declines, accepted challenges, cooperative companion battles, direct assistance/evolution help, shared journeys, tournament meetings and Champion-level rivalries. Those facts feed the existing relationship network and a bounded social-behaviour record rather than a separate cosmetic counter. Repeated declined unsolicited challenges make that robot back off for progressively longer periods; accepting a later challenge resets the decline streak. Sparse personality-specific dialogue appears only at meaningful relationship milestones.

Unsolicited robot challenges are now genuinely optional: after the robot's pre-battle line the player may accept or decline. A refusal is remembered as a social event instead of being misclassified as a battle loss, and does not immediately re-trigger the challenge. Manually selecting **BATTLE ME NOW** remains an explicit player request and proceeds directly. Companion cooperation, tournament meetings and Champion rivalries feed the same persistent model, while Thoughts, Robot Debug and the Relationship Network page expose a readable summary without revealing hidden player information. RobotMind is now **v7** and old saves lazy-backfill an empty social-behaviour state with no invented relationship history.

The Omnissiah can now **praise and encourage** robots as the positive counterpart to public judgement. `omnissiah.praised` and `omnissiah.encouraged`, plus the exported `omnissiahPraise` / `omnissiahEncourage` API, create a persistent **OMNISSIAH COMMENDATION** news-ticker event. Every robot may acknowledge each public commendation once in personality-specific dialogue. The praised robot receives a modest learned-personality signal toward disciplined confidence, resilience and loyalty; witnesses receive a smaller encouragement signal. Commendation never grants stats, levels, items, money, RNG advantages or story progress.

A START-menu stack bug that could leave a white screen after closing Ultron's UI is fixed. The host START menu already removes ordinary rows before invoking them; Ultron previously popped the stack again, accidentally removing the overworld beneath its own menu. The Ultron row now stays open until Ultron closes that **exact captured parent menu once**, and stale/foreign parents are never blindly popped. Regression coverage pins CLOSE/B exit and host-pre-popped behaviour so every Ultron-owned page returns to a valid underlying game state.

The completed **Relationship behaviour beyond trading** item has been deleted from the living roadmap. The next unfinished feature is **Champion lineage and challenger adaptation**.

## v2.25.0: outcome-driven personality development

Each robot now develops slowly from accumulated **real outcomes** while preserving its authored core identity. A bounded Personality Development model tracks seven learned tendencies: caution, boldness, curiosity, discipline, loyalty, rivalry and resilience. Individual events make deliberately small changes which diminish near their caps, so one lucky win or bad loss cannot rewrite a robot overnight. Pokemon stats are never changed.

The evidence is contextual rather than a flat win/loss counter. Gym and League failures build more caution and preparation discipline than ordinary trainer losses; a successful corrective postmortem builds resilience and validates disciplined preparation; risky catches reinforce curiosity/boldness; repeated player battles build rivalry/counter-planning; long-serving partners reinforce loyalty/protective play; and an Omnissiah judgement strongly affects the punished robot while producing a smaller caution signal in witnesses.

The resulting tendencies feed existing legal decision weights such as healing threshold, Gym confidence, challenge/duel frequency, wandering/catching preference, training rate, retry patience, level margin and live battle risk/protection. They never grant levels, stats, moves, items or hidden information. RobotMind v7 persists the bounded development and relationship history, lazy-backfills older saves from real stored adaptation counters, and Thoughts/Robot Debug expose the current learned tendency, axis values, latest shift and adapted weights.

The completed **Outcome-driven personality development** item has been deleted from the living roadmap. The next unfinished feature is **Relationship behaviour beyond trading**.

## Context-sensitive incidental wild RUN decisions

Physical same-map robot travel can now produce real incidental wild encounters from the live local encounter ecology. The default physical-step roll is 10%, after which the actual local species/level is drawn, Weather-FX substitution is respected when exposed, and the opponent is resolved through the robot battle simulation rather than invented as generic travel damage. Owned Repel suppresses eligible lower-level encounters. Deliberate training remains on its existing training path and never uses this escape seam.

`WorldCompetence.shouldRunWild()` now has a real caller. A robot under meaningful HP or PP pressure may try to escape a low-value incidental encounter, but never because of hidden player information and never when the encounter is a deliberate hunt/CATCH objective, a rare or shiny target, a high team-need target, a Nuzlocke first encounter, or a forced/trapped/no-escape context. A failed RUN attempt consumes the turn and the wild Pokemon gets a legal attack before the robot may try again; escape odds improve through the normal speed/attempt structure rather than becoming a free teleport. If the robot stays, `BattleSim` persists real HP/PP loss and normal wild EXP.

Because incidental travel encounters are now real, Nuzlocke first-encounter bookkeeping is authoritative here too: the exact encountered species consumes the route slot, one robot-owned Ball is thrown when available, and a failed/no-Ball attempt is recorded as the route miss before any remaining battle continues. WorldCompetence v3 lazy-backfills old saves, keeps bounded wild-decision history, and reports encounter/RUN/fight/failure diagnostics in Thoughts/Robot Debug.

The completed **context-sensitive RUN** item has been deleted from the living roadmap. The next unfinished feature is **Direct Gen 2 Apricorn-tree harvesting**.

## TM/tutor regret prevention

One-use move resources now receive a bounded future-recipient forecast before they can be consumed. The robot compares every compatible Pokemon in the current six and PC, compatible planned evolutions, and the target/alternates of an active acquisition mission. The forecast also evaluates the next resolvable Gym roster and the complete Pokemon League sequence, using only public game data and the robot's own plans.

A materially better boxed, evolved, or likely near-future recipient causes the resource to be held. If the same owned Pokemon can already learn the TM and will later evolve, that evolution is not a false blocker because the learned move survives evolution. Reusable TMs remain reversible and are not artificially rationed.

The same `irreversibleMovePlan` seam accepts `source="TUTOR"` so any real one-use tutor consumer can perform the identical regret check before spending its actual tutor currency/event. Ultron does not invent a tutor execution path where the host exposes none. Forecast state is bounded, persists through save/reload, and appears in Thoughts and Robot Debug.

The completed **TM/tutor regret prevention** item has been deleted from the living roadmap. The next unfinished feature is **context-sensitive RUN decisions in real incidental wild battles**.

## Interaction reliability hotfix (v2.21.1)

Robot interaction fallback now samples the **current fixed-step A-button edge after the host input step**, rather than the previous step. The facing-robot proximity scan also accepts live runtime `x`/`y` coordinates in addition to `cellX`/`tileX`, matching the coordinate shape used by spawned `AIR_*` robot NPCs. These changes prevent intermittent cases where the player is facing a robot and pressing A appears to do nothing.

The v2.21.0 robot-count persistence rule is unchanged: once a save has initialized Ultron, its chosen 1-7 robot count is retained across updates and the roster prompt is not shown again.
The World is not required. When installed, it is used only through supported optional integrations.

## Choose your robot roster in Oak's introduction

After the player finishes entering their name, Oak asks how many robot rivals should share the save. This choice is part of Oak's normal introduction in both supported generations:

- **Gen 1:** immediately after Oak confirms the player's name.
- **Gen 2:** immediately after the player-name screen.
- Available answers are **one through seven**.
- The selection is permanent for that save and is stored before the robots begin their journeys.
- **Existing saves that have never had Ultron receive one 1-7 robot roster choice.** Once Ultron has initialized a save, the chosen count is persistent across updates and is never asked again. Legacy Ultron saves silently backfill the marker and preserve their existing count.

## Up to seven independent robot rivals

| Slot | Robot | Starting character | Developing voice |
|---:|---|---|---|
| 1 | **Ultron** | Analytical, competitive and confident | Becomes more calculating after defeats and bolder after victories |
| 2 | **Data** | Precise, inquisitive and evidence-led | Talks in hypotheses, corrections and observed patterns |
| 3 | **R2-D2** | Daring, loyal and mischievous | Develops a spirited, humorous rivalry with the player |
| 4 | **WALL-E** | Gentle, persistent and protective | Expresses growing courage, attachment and sporting respect |
| 5 | **Robby** | Protective, courteous and service-minded | Scouts carefully and puts partner safety ahead of flashy wins |
| 6 | **T-800** | Mission-focused, relentless and attritional | Minimizes detours and applies pressure until the objective is complete |
| 7 | **Andrew** | Patient, curious and relationship-driven | Builds long careers with partners and increasingly nuanced choices |

Every robot has its own party, PC boxes, money, inventory, Poké Balls, TMs, HMs, badges, objectives, map position, memories, relationships and battle record. They do not share artificial progress.

The robots can meet, battle one another, exchange observed information, trade eligible duplicate Pokémon and develop friendships, mentorships, competitive respect, rivalries, feuds and arch-rivalries. A robot falling behind its peers receives motivation to catch and train legitimately rather than free levels or Pokémon.

## Seven-robot starter balance

Ultron receives the appropriate unused/counter laboratory starter after the player's choice. Data, R2-D2 and WALL-E keep their alternate Fire/Water/Grass cycle, while the expanded cast has fixed character partners:

| Game | Data | R2-D2 | WALL-E | Robby | T-800 | Andrew |
|---|---|---|---|---|---|---|
| Red / Blue | Vulpix | Horsea | Bellsprout | **Pidgey** | **Geodude** | **Poliwag** |
| Yellow | Vulpix | Horsea | Bellsprout | **Pidgey** | **Geodude** | **Poliwag** |
| Gold / Silver / Crystal | Houndour | Horsea | Bellsprout | **Pidgey** | **Geodude** | **Poliwag** |

These starters use the loaded game's legal level-5 moves. Ultron does not inject an otherwise-illegal move simply to manufacture STAB. If a conversion genuinely omits a requested species, only then is that robot given the nearest configured fallback present in the live registry. Stable internal save IDs are preserved for the three added robots so upgrades do not orphan their party, money, relationships or tournament/Champion history.

## Pokémon trading

Robots can trade eligible Pokémon with one another when physically together, and the player can select **Trade Pokémon** while speaking to a robot on the same map. Starters, Eggs, signature partners, aces, strongly bonded Pokémon and a robot's last usable party member are protected from being offered. Pokémon retain their level and moves, change ownership legitimately and trigger real trade evolutions; Gen 2 held-item trade evolutions require and consume the correct held item. Trading does not alter story flags or manufacture Pokémon.

## Thoughts before player battles

Before a robot attacks or begins a **Battle Me Now** challenge, it speaks through the game's standard text box. The battle starts only after the player closes that text.

These are not fixed trainer quotes. Each robot keeps a persistent voice profile shaped by its history against the player. Wins can increase confidence, losses encourage analysis and adaptation, repeated meetings develop familiarity, and long rivalries produce more established speech. The result is a distinct evolving voice for all seven robots. Robby grows more protective and duty-focused, T-800 becomes terser and more countermeasure-driven, and Andrew becomes increasingly reflective about the history he shares with long-serving partners.

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


## Trade, trust and relationship intelligence (v2.10.7)

- Permanent trades are valued before acceptance using scarcity, team need, duplicate status, level, DVs, held items and attachment.
- Ultron, Data, R2-D2 and WALL-E use different negotiation thresholds, while earned relationship trust supplies only a small capped concession.
- Autonomous robot-to-robot trades require both robots to accept the value exchange and use spare PC Pokemon rather than silently dismantling the active six.
- Same-map robots can perform immediate returnable trade-evolution loans.
- The player can help a robot evolve a Pokemon through a persistent collateral-backed loan, return it later, or explicitly break the agreement; the robot remembers which happened.
- Robots can immediately help evolve the player's own legal trade-evolution Pokemon as well.
- Trade events feed the existing central relationship graph instead of inventing a second friendship statistic. No trade/trust value modifies Pokemon battle stats.






## Advanced Companion Doubles Cooperation (v2.21.0)

A following robot now coordinates with the player as a doubles partner instead of independently maximizing its own move score. If the player has already committed to Earthquake or another ally-hitting spread move, the robot can Protect/Detect or legally pivot to an immune reserve before the move resolves. Critical-health partners can also make an emergency substitution into a materially safer healthy reserve.

Targeting is cooperative. A healthy priority foe can receive coordinated focus fire, while a nearly-finished foe the player is already covering causes the robot to split onto the other target. Major status is divided across threats instead of duplicated, speed control is preferred when the player's active Pokemon is slower than the fastest foe, and screens/control can protect a player's setup turn. Robot-owned spread attacks still respect ally immunity and friendly-fire risk.

Companion cooperation uses a bounded persistent history and exposes its latest coordination kind and explanation in Thoughts/Robot Debug. No hidden player move or opponent information is read: the robot sees the player's already-selected action and the public/current battle state.

## Robot-count persistence across updates (v2.21.0)

The chosen 1-7 robot roster is now mirrored into a small dedicated `robot_count_v1` save record in addition to the main Ultron state. Saves that already contain an Ultron roster are silently recognized and backfilled even if they predate the previous migration marker. An initialized save can therefore update repeatedly without seeing the robot-count prompt again.

The prompt is reserved for an existing game save with no Ultron history at all. Those saves remain robot-dormant until the player chooses a count. New games still choose during Oak's introduction.

## PP-War Exploitation (v2.20.0)

Battle Foresight now turns observed move use into tactical PP pressure without reading hidden PP Ups. Each revealed move keeps an honest current-battle interval from the move's base PP through its maximum legal PP-Up total, then labels that interval as fresh, low, plausibly exhausted, near exhausted, or confirmed exhausted.

That evidence changes live choices. A move with one possible use remaining can justify a legal Protect/Detect/recovery/substitute stall instead of an unnecessary panic switch, while a move that has reached its maximum possible legal use count is treated as confirmed empty and can create a setup opportunity. Matchup risk is discounted only by the observed interval, so a nearly dry move remains dangerous and an unrevealed move is never assumed absent.

Speed inference is stricter too. Equal-priority move order is accepted as raw Speed evidence only when the turn is clean. Visible paralysis, observed Quick Claw/order overrides, and turns after a witnessed Speed-changing effect are rejected and counted separately in diagnostics rather than polluting the faster/slower model. No hidden held item is inspected.

PP-war reads, stalls and exhaustion exploits persist through the existing bounded tactical state and are exposed in Thoughts/Robot Debug. Struggle remains untouched: BattleTactics never manufactures it, and the invisible fifth move is still available only when every normal move has 0 PP.

## Deep Live Battle Tactics (v2.19.0)

Robot-owned trainer battles now use a persistent live tactical layer above ordinary move scoring. It can make legal safe pivots, preserve the strongest remaining win condition, spend a lower-value reserve as an intentional sacrifice when every switch is dangerous, convert real faints into short revenge-positioning windows, and interrupt observed setup with a learned disruption move.

The layer is observation-disciplined: matchup danger is based on visible species/public type data plus moves and damage the robot has actually witnessed through Battle Foresight. It does not inspect the player's hidden current moveset or exact stats. Gen 1 returns legal `aiSwitch` actions through the shared enemy-action seam; Gen 2 uses a guarded adapter at its earlier switch/item phase, because Gold/Silver/Crystal choose switches before the move-only enemy-action hook.

Self-KO attacks such as Explosion can now be refused when their local damage would throw away the robot's remaining win condition. At total PP exhaustion the robot may switch if switching is legal, but the tactics layer never learns, creates, or substitutes Struggle: a trapped Pokemon with no usable PP still falls through to the engine's permanent invisible fifth-move Struggle rule.

Tactical state is save-safe and bounded. Thoughts and Robot Debug expose the last live tactic, switch/sacrifice counts, win-condition preservation count, and any current revenge window.

## Reserve-team Careers & Omnissiah Judgement (v2.18.0)

Robots now maintain an intentional reserve bench rather than treating every boxed Pokemon as interchangeable spare value. Team Architect continuously re-evaluates only Pokemon the robot actually owns and can assign seven specialist careers: **League reserve**, **anti-player counter**, **catching specialist**, **weather specialist**, **Gym specialist**, **trade/evolution stock**, and in Gen 2 **breeding stock**. Careers are derived from legal species data, real moves, observed opponent information, current progression, weather affinity, trade-evolution rules and Gen 2 breeding suitability. They never change battle stats.

Career assignments now affect the situations they were retained for. Gym specialists receive roster preference against the next known Gym, League reserves receive endgame preference, anti-player counters can enter an anti-player plan, and weather specialists receive context preference only in relevant live weather. During a strategic acquisition mission, a boxed catching specialist can cause a real Pokemon Center detour so the robot legally brings it into the active six before hunting. If no safe party slot exists, the planner continues without inventing a swap.

Trade/evolution and breeding stock are protected from generic duplicate liquidation. Intentional trade stock is surfaced first in robot trade offers, while Gen 2 Day Care planning prefers retained breeding stock when it is otherwise a legal parent for the current breeding project. The maintained bench target remains bounded at roughly 8-12 useful Pokemon instead of expanding without limit. Career state is re-derived from the current collection and is exposed through Thoughts/Robot Debug.

Ultron now also exposes a formal **Omnissiah punishment** seam without inventing punishment authority inside the rival AI. A compatible system can emit `omnissiah.punished` or use the exported punishment API for a named robot. The judgement is persisted and immediately becomes a public **OMNISSIAH JUDGEMENT** item on the shared news ticker.

Once any robot has been punished, **every active robot** unlocks a fresh personality-specific warning for its next conversation with the player. The shared pool includes lines such as *“The eyes of the Omnissiah are always watching.”* Each robot acknowledges each new judgement once, then normal interaction resumes; a later punishment unlocks a new warning across the roster. Punishment history is bounded and survives save/reload.

The completed Reserve-team careers item has been deleted from the living to-do list. The next feature is **Deep live switching and sacrifice logic**.

## General Acquisition Missions (v2.17.0)

- A robot can now turn a concrete team deficiency into a persistent physical acquisition project rather than merely deciding that it would like another Pokemon.
- The planner can identify an undersized active roster or an unresolved Gym/League matchup gap, then search the loaded encounter ecology for species that actually solve that need.
- Candidate maps must exist, be legally enterable under the robot's own badge/HM/story gates and be physically routable from its current position. Out-of-generation, forbidden and already-owned species are rejected.
- The selected project keeps a real Ball target. If stock is short, the robot routes to a real Poke Mart and uses its own money; existing goal-aware valuable selling may liquidate only enough treasure to finance the shortage. No Ball or Pokemon is generated by the planner.
- The robot travels to the chosen encounter map and hunts through the ordinary encounter/capture path. After repeated misses it may retarget to another qualifying legal candidate instead of accepting an unrelated catch.
- A caught Pokemon is re-evaluated against the original need. A weather/form substitution that no longer supplies the required coverage/resistance does not falsely complete the mission.
- Boxed mission catches must be activated through a real Pokemon Center, then trained normally until developed enough to fill the diagnosed need. The mission retires into bounded history only after that chain is complete.
- Gym/League Postmortem resistance prescriptions now use this same mission engine, so diagnosis and acquisition share one auditable path. Robot Nuzlocke runs deliberately disable targeted species missions to preserve their first-encounter rule.
- The current target, map, stage, Ball reserve, candidate score and replan count are persisted and visible in Thoughts/Robot Debug.

## Explicit Decision Confidence (v2.16.0)

- League expeditions, ordinary acquisition decisions, one-use TM/tutor-style move-resource spending and voluntary major player battles now use a shared explicit 0-100 confidence record with a visible commit threshold.
- Confidence never changes Pokemon stats or battle rolls. It decides only whether the robot has enough legitimate evidence to commit or should prepare/scout first.
- League decision confidence combines the existing worst-stage matchup estimate with selected-six readiness, expedition supplies, HP and PP recovery. Low confidence routes to the specific legal action still missing: Center preparation, training, Mart restocking or recovery.
- Ordinary uncertain captures can preserve a scarce Ball and record a bounded scout target instead of spending blindly. Nuzlocke first encounters, active hunt targets, shinies, high-value encounters and emergency roster recruitment keep their existing explicit priority rules.
- One-use TMs now need both the existing moveset-improvement threshold and sufficient decision confidence. Weak recipient/opponent evidence leaves the TM unconsumed; reusable TMs are never blocked by irreversible-resource confidence.
- Voluntary player challenges use observed/currently available matchup evidence. Low confidence creates a short-lived legal heal/train/scout preparation job; favourable evidence commits normally. Badge and League campaigns still outrank this optional preparation.
- The confidence store lazy-backfills old saves, keeps bounded history, persists the latest League/acquisition/TM/battle decisions, and is shown in Thoughts and Robot Debug with the chosen action and threshold.

## Gym/League Postmortem Prescriptions (v2.15.0)

- Real Gym and Pokemon League losses now generate persistent corrective prescriptions from observed battle/team/resource evidence instead of collapsing every defeat into generic grinding.
- Prescriptions can call for changing the active six, training a named reserve, acquiring a reachable defensive resistance, buying healing/status/PP supplies, reviewing an exhausted low-PP move at a Pokemon Center, or raising the legal level margin.
- The Long-Horizon planner inserts unresolved prescriptions ahead of the next Gym challenge or League expedition. Each prescription routes through the existing legal world action that can satisfy it: Pokemon Center, Poke Mart, training area or reachable encounter map.
- Resistance acquisition constrains the live encounter search to reachable species that actually resist the observed problem attack types and are not weak to them. If no legal candidate exists, the robot does not invent one.
- Supply prescriptions spend only robot-owned money at a real Mart. Status shopping prioritizes the cure for a status actually present after the failed campaign, while League budgets can request broader reserve stock.
- Team-change and reserve-development prescriptions use the robot's own PC at a real Pokemon Center. Move reviews run through the existing legal TM/moveset machinery rather than remotely replacing moves.
- A later victory against the same objective retires its active prescriptions. Resolved actions move into bounded history, old saves lazy-backfill an empty store, and Thoughts/Robot Debug display the current corrective plan.

## Ground Item Echoes + Evolution Timing Intelligence (v2.14.0)

- When a robot physically reaches or stands beside a live ground-item pickup, it may receive one private echo copy of that exact map pickup. Each robot has its own persistent bounded pickup ledger, so Ultron finding an item does not prevent Data, R2-D2 or WALL-E from independently finding it later.
- The actual map object is never removed or marked collected, and the player's Bag, pickup flags and story state are never read as robot ownership. The player's copy remains available.
- Ground TMs become private robot TM ownership without consuming the world TM. Other items enter that robot's own Bag and then flow through the existing legal resource systems.
- Rare Candies are reserved for useful legal levels, strongly preferring an active evolution-timing milestone or long-horizon evolution step instead of automatically feeding the lowest-level party member.
- Nuggets and other valuables are now treated as a liquid reserve. At a real Mart, robots sell only enough to fund the active long-term cash target, while known recipe stock such as Kanto Reforged's three-Nugget Focus Sash requirement remains protected.
- Evolution timing compares the current and evolved species' real natural learnsets. A legal level or stone evolution can be delayed when the unevolved form learns a materially valuable move soon and the evolved form learns it substantially later or never. Once the useful move is learned, the hold clears and the normal legal evolution proceeds.
- Long-horizon Gym planning now uses the adjusted evolution level, so a deliberate move-learning delay is part of the plan rather than something the planner fights against.

## Elite Four Expedition Intelligence + Struggle invariant (v2.13.0)

- Robots treat the Elite Four and Champion as one continuous expedition rather than five unrelated battles. The planner resolves the real League sequence from the loaded game data and scores the selected six against every stage.
- Before entry, a robot budgets healing, status cures, Revives where its own Nuzlocke rules permit them, and PP restoration for the complete run. Missing stock must be bought with that robot's money at a real Mart.
- The final entry gate requires a Center-prepared six, adequate whole-run matchup confidence, the required bag reserve, essentially full HP and fully restored learned-move PP. A stale `LEAGUE_READY` state fails closed and returns to preparation.
- Early League rooms conserve scarce PP when another viable move exists. Between rooms, HP, status and PP recovery still consumes only items already in the robot's own bag; no hidden Center heal occurs inside the challenge.
- **Struggle is an invisible fifth move.** It is never learned, taught, forgotten, reordered or used as one of the four move slots. It may be selected only when every real learned move has zero PP. Status moves with PP still count as usable moves and therefore prevent Struggle. Old/corrupt learned Struggle entries are stripped during party repair.
- The living to-do list removes the Elite Four campaign item in this release because its deterministic campaign, planner and Struggle regression audits now pass.

## Long-Horizon Planning (v2.12.0)

- Every active robot can persist a multi-stage Gym campaign instead of rediscovering a local objective from scratch each tick.
- Campaign steps are built from the robot's actual situation and may include legitimate team acquisition, an imminent level evolution, Center-only matchup-six/TM preparation, training and the final Gym challenge.
- The planner does not perform catches, grant evolutions, teach remote TMs or award badges. It delegates each step back to the existing legal subsystem that already owns that action.
- A campaign rewrites when the target Gym changes, the active/boxed roster or owned TM preparation changes, the previous Gym preparation is disproven by a loss, or the same step remains stalled for too long.
- Current step, confidence and rewrite reason are persisted under RobotMind reliability and exposed in Thoughts/Robot Debug.
- `docs/ROBOT_IMPROVEMENT_ROADMAP.md` is now a living unfinished-work list. Completed items are deleted from it in the release that implements them rather than accumulating checked boxes.

## Goal Arbitration & Reliability Intelligence (v2.11.0)

- Every major robot objective now has a central priority. Emergency healing, shopping, League/Gym commitments, tournaments, player/rival challenges, NPC trades, Kurt errands, training and exploration no longer overwrite one another simply because two subsystems happened to run on the same tick.
- Explicit service interruptions use short locks. The ordinary AI must respect those locks until the legal recovery/errand action completes, after which the suspended strategic objective resumes.
- Lower-priority errands can be rejected when a higher-priority commitment is active. For example, an optional Kurt trip will not tear a robot away from an imminent Gym or League objective.
- RobotMind schema v5 persists bounded reliability state: arbitration history, deterministic event replay, subsystem health, audits and failure snapshots.
- Self-audits periodically check robot-owned money/inventory, movesets, destinations and repeated no-progress state. Safe repairs affect robot state only and never touch player data or story flags.
- Optional subsystems that repeatedly throw errors are temporarily quarantined, with exact diagnostics and automatic later retry. Core simulation failures also receive a short cooling-off quarantine after repeated failures rather than crashing the entire robot loop forever.
- Failure snapshots include the robot's stable deterministic seed, live RNG state, map/coordinates, objective, destination, party, inventory and money so a bad AI state can be reproduced.
- Decision history now retains RNG/map context and remains bounded. Robot Debug exposes both Goal Arbitration and Reliability summaries plus a CLEAR RELIABILITY LOG action.

## Tournament & Special Activity Intelligence (v2.10.9)

Robots now plan multi-round tournaments, Safari Zone runs, Bug-Catching Contests and fishing instead of invoking those activities as context-free exports. Tournament planning tracks round/bracket state, scouts known opponents where legitimate, and preserves scarce healing items for later rounds while still allowing emergency use at critical HP.

Safari planning values targets against remaining steps and Safari Balls. Bug-Catching Contest planning compares the current catch against remaining time/Balls and keeps searching when a stronger result is realistically worth pursuing. Fishing planning selects an actually owned Rod and scores the live route's rod-specific encounter table rather than fishing blindly. Host activity integrations may consume the exported planning APIs without changing player activity state.

Companion doubles also expose sparse tactical intentions such as covering the other target, avoiding friendly fire, applying status or taking a reliable finishing line. These intentions are diagnostics/dialogue only and do not reveal hidden opponent information.

## Pokémon History & Dialogue Intelligence (v2.10.8)

Every robot now keeps a persistent history for individual Pokémon rather than remembering only the team as a whole. Meaningful achievements such as **GYM ACE**, **E4 CLUTCH**, **PLAYER KO**, **SURVIVED 1 HP**, **TOURNAMENT MVP**, **HALL OF FAME**, first capture and trade evolution are attached to the actual partner that earned them. History gives only a modest roster tie-break preference; it never changes stats, levels, damage or accuracy.

Major milestones can create a desire to nickname a Pokémon. If the capture-time naming opportunity has passed, the existing Name Rater objective remains mandatory. Important faints also receive context-sensitive reactions based on the battle and that partner's established history, while each actual faint still produces only one sadness transition.

Important Gym, League, robot-duel and trainer simulations retain a short temporary trace long enough to identify decisive partners and distill a compact post-battle analysis. The saved postmortem is capped and can record **THREAT**, **WEAKNESS**, **MISTAKE**, **RESOURCE ERROR** and related lessons. These lessons feed existing Team Architect and Resource Policy decisions, so a bad battle can change the next roster or supply reserve instead of becoming decorative text. Direct player battles credit **PLAYER KO** only from the real `battle.fainted` event. Thoughts, pre-battle dialogue and Robot Debug can reference earned milestones and the latest real lesson without exposing hidden player information.

## Acquisition, economy and Gen 2 breeding (v2.10.5-v2.10.6)

Robots now evaluate whether a catch is actually worth resources before spending a Ball. Species novelty, rarity, team need, evolution potential, legal moves, NPC-trade requirements, DVs and duplicate value contribute to capture value. Common encounters preserve Great/Ultra/specialised Balls, while rare, legendary or shiny targets justify stronger resources. Gold/Silver/Crystal robots understand the situational value of Level, Lure, Moon, Love, Fast, Heavy and Friend Balls.

Economy planning is forward-looking. The robot reserves money for Balls, medicine, travel and major battles before optional purchases, assigns held items from its own Bag, conserves important Berries, sells genuinely surplus valuables/duplicates at a real Mart, and protects useful trade/breeding specimens. Kurt projects require an owned Apricorn plus physical visits before and after the wait; the player's Apricorns and Kurt state are never touched.

Gen 2 breeding is now an explicit project rather than an opportunistic background roll. The robot records the desired baby and Egg Move, selects only compatible parents it actually owns, protects starters/aces/bonded partners, checks its cash reserve, physically travels to Route 34 Day Care, pays its own baseline withdrawal fee and evaluates the offspring. Valuable hatchlings become legitimate bench-development/training projects. If a needed Egg Move has no owned legal pair, the robot may hunt a reachable compatible donor that naturally starts with the move; it cannot invent a parent or teach the donor a move it has not learned.

## One-time existing-save robot roster choice (v2.10.6)

Older saves that predate the roster-choice migration receive one in-game menu asking whether that save should run **1, 2, 3 or 4 robots**. The choice is stored in `robotCountChoiceVersion` and is not shown again after completion. New saves continue to make the same decision during Oak's introduction.


## Moveset Intelligence hotfix (v2.10.4)

Robot Pokémon now process every level they cross and evaluate each newly unlocked move from that species' real level-up learnset.  The decision scores STAB, coverage, accuracy, PP, priority, setup/status/recovery value, role fit and redundancy against the four moves already known.  A robot may learn or decline the move, and the decision is retained on that Pokémon.

Flat/ambiguous learnset arrays are no longer treated as universal level-1 moves.  Kanto Reforged's singles-disabled moves, including Rage Powder, are rejected while KR is active.  Old saved sets are repaired without erasing a deliberate older natural move merely because it is no longer in the species' newest-four default.

## World Competence (v2.10.3)

Robots now maintain persistent **route danger** and **navigation confidence** rather than treating every map as equally safe forever. Blackouts, repeated path failures and resource pressure raise a map's danger score; successful legal traversals lower it and increase confidence. The route planner may prefer a safer legal route when one exists, but it still obeys every story/HM/map gate.

Successful transitions through puzzle-like maps are remembered as solved routes. When the player has legitimately traversed a local dungeon sequence nearby, robots can reuse the exact contiguous observed trail rather than trying to rediscover ice-floor, teleport-pad or similar solutions from collision alone. No route is fabricated from a tile the player or robot never traversed.

Two-tile oscillation and repeated no-progress states now trigger temporary approach-tile blacklists, route replanning and bounded deterministic stuck snapshots containing the robot's map, position, objective, route, party, inventory and RNG state. Visible robots also use deterministic traffic priority and step aside for one another at narrow choke points instead of indefinitely blocking a doorway.

Emergency goal arbitration can suspend and later resume the robot's previous plan. Critical HP, exhausted move PP, zero balls during an active catch objective, or a repeatedly invalid route can temporarily send the robot to a real Center/Mart or force a replan. Once the emergency is resolved, the suspended strategic objective is restored rather than forgotten. World Competence diagnostics and the latest stuck snapshot are available in the password-protected Robot Debug menu.

## Kanto Reforged pretraining and progressive movesets (v2.10.2)

When **Kanto Reforged** is active, every robot starts the run with a bundled strategic model trained directly from the supplied **Kanto Reforged v1.5.3** source. They do not need to rediscover the mod's rules on every save. The model includes the 386-species scope, Dark/Steel/Fairy chart, Gen 3 type-category physical/special rules, abilities, held items, breeding, Berry Farm, Move Hub, Blacksmith, DexNav/spawn modes, soft level caps, restored Gen 2 Kanto dungeons, postgame Kanto Gym curve, utility NPCs, fossil/roamer/static-legend routes, trade-evolution bypasses and Kanto Reforged AI conventions.

At engine start Ultron indexes the **live merged map graph and encounter registries** as well. This means robots know where the currently configured encounter tables lead from the beginning, while the live game remains authoritative if DEX SCOPE, FULL SPAWN MIX, PURE RANDOM SPAWN or another compatible mod changes those tables. Pretraining supplies rules and strategy, not story flags or free resources.

Movesets are now derived **per species and per current level** from `level1Moves`, `learnset` and `levelMoves`. Robots learn newly reached natural moves as they level, including useful status/setup moves, instead of only accepting attacks with higher base power. Kanto Reforged's `tmhm` compatibility field is understood directly. Ultron no longer trusts a global `fallbackMove`, preventing a fallback such as ViceGrip or Buzzy Buzz from leaking into unrelated Pokemon.

There are two repair guards for other trainer/rival systems sharing the game. Suspicious explicit one-move trainer parties are repaired before materialisation, and the actual enemy party is checked again at battle start in case a host/global fallback created the collapse later. Legitimate low-level one-move species and normal curated movesets are left alone.

See `docs/KANTO_REFORGED_TRAINING.md` for the complete training contract and source fingerprint.

## Team Architect (v2.10.0)

Robots now build teams by **role as well as raw strength**. Every owned Pokemon is evaluated as a possible lead, sweeper, wall, status supporter, revenge killer, utility member, catcher or weather supporter from its live stats and currently legal moves. These labels are planning metadata only and never grant hidden stat bonuses.

When preparing for a known opponent or Gym, the selector balances those roles with level, defensive matchup, current move coverage, competitive knowledge, attachment, species mastery and learned counter-plans. Coverage credit requires a move the Pokemon actually knows.

Each robot also maintains a useful **8-12 Pokemon bench** across party and PC. Under-levelled reserves can be rotated into the active party only while the robot is physically at a Pokemon Center, trained normally, and returned to a Center before the robot restores its matchup six.

Gym defeats now produce an internal diagnosis and a preparation fingerprint. Outside catch-up mode, a robot will not repeat an identical losing team unchanged; a real improvement in level, moves, held item or roster is required first. Team Architect decisions are visible in Thoughts and the password-protected Robot Debug page.

The remaining agreed robot-improvement work is tracked in `docs/ROBOT_IMPROVEMENT_ROADMAP.md`.

## Battle Foresight (v2.10.1)

Robots now build a probabilistic battle model from **observable events**, not from the player's hidden battle object. Repeated first send-outs become lead tendencies, actual switches become transition habits, executed moves become confirmed evidence, and legal learnset/TM possibilities remain only suspected until seen. Evidence is explicitly labelled confirmed, suspected or unknown.

Move order between equal-priority moves builds a likely-faster/likely-slower estimate without reading exact Speed. Damage memory is stored as observed percentage ranges only when the damaged target belongs to the robot, so its maximum HP is information the robot legitimately owns. Priority moves are excluded from speed inference.

Revealed move PP is tracked as a **range** because PP Ups are hidden. Current-battle usage resets at the next battle rather than pretending the robot knows whether the player healed. Setup moves such as Swords Dance, Agility, Amnesia, Curse and Belly Drum increase urgency, and Team Architect can prefer owned Pokemon that genuinely carry disruption or coverage against an established pattern.

Endgame move choice now gives extra weight to reliable finishing attacks against visibly low-HP targets. Companion doubles also avoid redundant major-status attempts and can favour useful status control against a healthy unstatused foe. None of these systems alter stats, damage, accuracy, DVs or levels; they alter decisions only.

Battle Foresight summaries are available through Thoughts and Robot Debug, including likely lead, common switch, setup threat, confirmed/suspected move evidence and approximate PP range.

## Learning from the player and one another

Robots observe revealed Pokémon, levels, moves and contiguous player travel. They can learn a dungeon exit by following the player and can share confirmed route or battle knowledge with the other robots.

**v2.9.1 intelligence model:** each robot maintains a compact opponent history from battles it actually participates in. Repeated species, highest seen levels and loss-weighted threats persist across saves. Moves are now learned from moves the player actually selects during battle turns rather than by reading the player's hidden full moveset at battle end. Repeated revelations build recency/confidence evidence and survive later partial scouting snapshots.

The same memory is converted into a lightweight metagame model. Robots classify known teams as balanced, fast, defensive, status-focused, weather-focused or hyper-offensive, identify a recurring threat, rank useful answer types from the live type chart, and can predict a likely resistance switch from the opponent's known bench. Those plans feed the existing Center-only counter-team selector, so preparation remains limited to Pokémon the robot genuinely owns.

Repeated field service also builds **species mastery**. Mastery is based on battles, victories, competitive preparation and existing bonds. It never modifies HP, damage, accuracy or any other Pokémon stat; it only gives a modest roster-selection preference to species the robot has extensive practical experience using. Robot-vs-robot battle records feed the same metagame model, and shared scouting merges newly learned species, levels and revealed moves without copying another robot's personal win/loss record.

Decision changes and recent path/simulation failures remain recorded separately, allowing the Thoughts page and diagnostics export to answer not only *what* a robot is doing but *why* it selected that objective, what it expects the opponent to do, and what recently went wrong.

Direct observations remain more trusted than imported or second-hand information. If a robot knows the player's team substantially outlevels its own, it prioritises catching, training and team preparation before seeking another rematch.

Portable training-data import and export shares confirmed strategic knowledge without copying Pokémon, levels, badges, money, inventory, story progress or personal chat history. Imported knowledge is stored with the save data rather than inside the mod directory.

## Canonical in-game trades without consuming the player's trade

Robots can now complete the games' real NPC Pokémon trades as part of their own journey. The registry is version-aware: Red/Blue, Yellow and Gen 2 each use their canonical trade list. A robot trade is a private parallel transaction, not a call into the player's NPC event. The player's trade flag, NPC dialogue state, party, PC and requested Pokémon are untouched.

A robot must supply the requested species from its own collection and physically reach the canonical trade map. It will not give away its starter, ace or an attached partner. For high-value preparation, it can first hunt another copy of the requested species. This makes **ROCKY** a real early-game plan in Gen 2: a robot preparing for Falkner can hunt Bellsprout, travel to `VIOLET_KYLES_HOUSE`, give that robot-owned Bellsprout to Kyle and receive the canonical Onix at the Bellsprout's level. Rocky keeps Kyle's OT data, fixed DVs and Bitter Berry.

Other canonical trades are available through the same system, including Yellow's distinct trade table. Each robot can complete each trade once independently of the player and independently of the other robots.

## Private Gen 2 competitive breeding

In Gold, Silver and Crystal, every robot has a private Route 34 Day-Care record that is completely separate from the player's deposited Pokémon, Egg, step counters and breeding flags. A robot physically travels to the Day-Care with compatible parents, continues its journey while the Egg develops, returns to collect it, pays the fee from its own money and then trains the hatchling normally.

The breeding planner understands Gen 2 Egg Groups, gender and Ditto compatibility, the matching-DV refusal, base-form offspring, level-5 Eggs, species hatch cycles, Nidoran offspring, father-side Egg Move and TM/HM inheritance, shared parental level-up moves, and Gen 2 Defense/Special DV inheritance. It combines the live Pokémon registry with the bundled Crystal Egg Move table and Gen 2 competitive set knowledge to prefer legal inherited moves that improve the final evolution's intended role. Parents and offspring always remain the property of that robot.

## Resource planning

Robots budget their own money and carry real finite supplies. Reserve planning covers Poké Balls, healing medicine, status cures, Revives, PP recovery and a badge-sensitive cash floor. A robot can interrupt a lower-priority objective to physically visit a Poké Mart when survival stock is materially depleted, then resume the interrupted objective. Scarce high-value medicine is conserved in live Gen 1 battles unless the current HP/status state justifies spending it.

v2.9.1 extended this to TM conservation. v2.9.2 completes TM acquisition: every robot has a generation-specific one-copy entitlement for all 50 TMs, purchased only while physically at a real Poké Mart using its own money and badge-tier access. The entitlement is separate from every player-owned map pickup, hidden item, Gym reward, NPC gift and story flag, so robots can never remove the player's Dig, Earthquake or any other TM. Route training no longer creates random TM finds.

 Competitive preparation can recommend a move but can no longer manufacture TM access by paying an abstract training fee. A robot must actually own the TM, pass the game's compatibility rules and teach it through the normal Center preparation path. Single-use TMs are held when the expected improvement is marginal, while a learned counter plan can justify spending one when its move type directly answers a known threat. Poké Mart TM purchases also respect the robot's survival cash reserve.

## Companions and embedded double battles

Talk to a robot on the same map and select **Accompany Me**. One robot can accompany the player at a time. The companion follows the player's actual route one tile behind whenever the map permits it, using the tile the player just vacated rather than chasing the player's current position. While accompanied:

- Eligible wild and trainer encounters become double battles.
- The player controls only the player's Pokémon.
- The companion independently controls its own Pokémon, targets, moves, switches and items.
- Its cooperative scorer considers type effectiveness, STAB, remaining PP and the player's already-selected target. It avoids redundant attacks on a nearly-fainted foe when the second opponent still needs pressure and avoids damaging the player's Pokémon with spread moves unless the ally is immune.
- Companion damage and experience persist after battle.
- Without a companion, normal battles remain single battles.

The required double-battle systems are embedded in Ultron. The standalone `double_battles` mod is therefore marked incompatible.

**v2.8.2 battle adapter:** companion Pokémon are materialized with the current client `Pokemon.new(data, species, level, rng)` contract and then have their robot-owned persistent state restored. This prevents the v2.8.1 failure where an obsolete options table occupied the RNG argument, the ally build failed silently, and a visibly active companion battle rolled back to 1v1.

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
- Password-gated Robot Debug (`cake`) with robot-only state, movement, economy, badge, TM, AI and memory controls

Talking to a visible robot opens that individual robot's interaction menu. Its attached nameplate follows its live overworld sprite and is hidden behind menus, text boxes, naming screens, battles and transitions.

## Configurable rules

Persistent settings include Catch Legendaries, Forgettable HMs, Reusable TMs, Periodic Challenges, News Ticker, Name Tags, Watch Player Battles, Daily Routines and Nickname Partners. Nickname Partners uses a sanitized offline PKMN.NET Name Rater corpus: robots may name a catch immediately, but every later rename requires an actual trip to the in-game Name Rater and traded Pokémon are excluded. Disabling presentation options does not disable physical movement, economy, blackouts or campaign progression.

## Installation

1. Install the packaged `Ultron_v2.35.0.zip` release.
2. Install or extract it as the `ultron` mod directory.
3. Confirm that `manifest.json` and `main.lua` are directly inside that directory.
4. Start a new Red, Blue, Yellow, Gold, Silver or Crystal save to choose one to seven robots during Oak's introduction.

Ultron remains dormant until the player's starter is committed. Existing saves migrate without teleporting an established robot to the player.

## Compatibility

- Games: Red, Blue, Yellow, Gold, Silver and Crystal through their recomp clients.
- The World: optional supported integration.
- Colosseum UI Overhaul: optional presentation compatibility.
- Standalone Double Battles: incompatible because Ultron embeds and controls the required companion-only implementation.
- Link play: protected by the mod's battle-affecting compatibility declaration.

## Release and validation

Package version: **v2.35.0**.

See [CHANGELOG.md](CHANGELOG.md) for version history and [RELEASE_NOTES.md](RELEASE_NOTES.md) for the release summary.
# v2.98.0: Incremental Search + Decisive Forward Recovery

Agent Brain planning now pauses and resumes across frames in bounded four-stage slices. New evidence invalidates an unfinished search and safely restarts it; the robot continues executing its last completed legal plan while a replacement is evaluated.

Routine wild training/catching is rejected when the robot's team benchmark is four or more levels above the route ceiling. The robot selects a stronger reachable area or advances toward the next legal League milestone. Only a genuine completionist/Collector with an active Pokédex acquisition may remain for missing species. Familiar-route loyalty expires as delay grows.

After a blackout, home and Pokémon Centers are recovery points only. Once healed, the robot immediately rebuilds a Gym/League objective and leaves by legal physical travel.

The completed incremental-search item has been removed from the unfinished roadmap. **50: Automatic performance regression gates** is next.
