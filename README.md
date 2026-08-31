# Ultron 3.41.0: Causal World Model

Every robot now maintains a bounded, persistent model of what its own actions appear to cause in the loaded Pokémon world. Switches, NPC interactions, item use, field moves and unfamiliar mod mechanics begin as tentative action-context-effect hypotheses; repeated physical interventions can promote them to confirmed causes, while failed repeats lower confidence or reject them. Passive coincidence—such as weather changing while a robot talks to an NPC—remains correlation and can never confirm causation. The model supports selective invalidation when relevant world evidence changes, exposes readable diagnostics, and only predicts intentions: the existing simulation must still travel, possess requirements and perform every action legitimately. The unfinished roadmap now begins with **63: Dynamic Progression Discovery**.

# Ultron 3.40.0: Agent Brain Reconciliation

Ultron's inherited reasoning audit debt is cleared. A newly created or migrated robot now completes its first bounded search immediately, guaranteeing an actionable initial goal; later replans retain incremental performance slicing. Anti-stagnation counts every reasoning slice rather than only completed multi-slice searches, restoring its intended five-repeat response. The four-level route-obsolescence rule again applies full relocation pressure when stronger reachable training exists, while completionist collection remains the narrow exemption. The Day Care regression audit now matches its documented P200 fee. All previously inherited Agent Brain audits pass, and the expanded roadmap now begins with **62: Causal World Model**.

# Ultron 3.39.0: Optional External Brain Interface

Ultron now exposes a disabled-by-default, versioned local protocol (`ultron.external-brain/1`) through its stable exports. A local extension may request a bounded high-level objective and, optionally, a destination already present and reachable in the live world graph. Requests are recursively screened for player state and direct mutations, checked against an objective allowlist and service-specific destinations, capped in utility and lifetime, then submitted to normal Agent Brain arbitration. Winning suggestions still execute only through Ultron's existing goal, navigation, economy, catching and battle systems. External models cannot teleport, spawn or grant anything, set outcomes, change HP/PP/stats, touch the player or override recovery and Champion-critical priorities. Offline autonomous Ultron remains complete and is the default. This completes the current unfinished-feature roadmap.

# Ultron 3.38.0: World-Adaptive Intelligence

Ultron can now construct a confidence-scored model of the Pokémon world actually loaded around it rather than treating bundled Kanto or Johto knowledge as authority. The adapter inventories live maps, connections, warps, encounter ecology, trainers, items, healing, shops, progression-looking locations and registered species; assigns reachable information-gathering intentions; strengthens beliefs after physical traversal and real encounters; lowers confidence when collision or field gates contradict a plan; and rebuilds when the loaded topology changes. Custom worlds without Red's house or New Bark Town receive a graph-discovered home/fallback. All adaptation remains bounded, deterministic and subordinate to recovery and Champion-critical obligations. It creates intentions, never teleports or grants progress. Bundled regional guides remain useful priors, while live topology and observed outcomes always win.

# Ultron 3.37.0: Emergent World Statistics

Ultron now maintains persistent ecosystem records derived from completed robot activity: most-used species, strongest winning lead matchup, most-traded species and biggest strength-gap upset. The Start-menu World Statistics page also calculates the current richest robot and dominant strategy directly from live robot-owned state. Battle appearances, transfers, matchups and upset history are bounded, deterministic and saved; the collector consumes existing simulation events and never runs extra battles or reads hidden player teams. The unfinished roadmap now begins with **60: Optional external brain interface**.

# Ultron 3.36.0: Observer Mode

Observer Mode adds an optional read-only seven-agent field dashboard to the Start menu. It shows every robot's live map, goal, badge progress and team HP together, supports previous/next focus cycling, and opens the focused robot's full AI Watch snapshot. Observer session state and focus persist across reloads but remain isolated from robot memory, scheduling and learning. The system never reads protagonist controls, moves the player, teleports robots, reveals hidden parties or changes simulation priority. The unfinished roadmap now begins with **58: Emergent world statistics**.

# Ultron 3.35.0: AI Watch Mode

The Start menu now includes a read-only AI Watch Mode for spectating any one of the seven robots. Its refreshable live snapshot shows map and state, current goal and immediate step, confidence, estimated risk, blocker, scheduler wake reason, the three strongest current beliefs and five most recent decisions. Watch selection is separate from the active robot used elsewhere in Ultron and persists across reloads. The view derives entirely from existing bounded state, creates no extra reasoning loop and cannot change scheduling, goals, travel or outcomes. The unfinished roadmap now begins with **54: Observer Mode**.

# Ultron 3.34.0: Deterministic AI Diagnostics

Ultron's performance report now exposes device-independent AI scheduler evidence for every robot: wake reason, selected jobs, completed deep plans, deferrals, route-valuation cache hit rate, deterministic work-cost units and jobs per simulated second. The counters are derived only from simulation ticks and logical work—not wall-clock timing—so equivalent saves remain comparable across machines and reloads. A bounded 24-window history and compact per-agent state persist with the campaign. The unfinished roadmap now begins with **53: AI Watch Mode**.

# Ultron 3.33.0: Performance Classes

Ultron now offers Low, Standard and Advanced AI performance classes. Every class keeps the same Champion Directive, memory, legality, catching, trading, navigation and learning systems. They differ only in bounded scheduling width, clean-state planning cadence, tactical look-ahead, candidate explanation breadth, tournament batching and diagnostic retention. Critical recovery, Gym, League and tournament states always bypass Low-class planning delays. Performance Scaling v2 combines the chosen class with measured runtime protection, so temporary device pressure can still reduce work safely. The unfinished roadmap now begins with **49: Deterministic AI diagnostics**.

# Ultron 3.32.0: Metagame Eras

The seven-agent field can now develop sustained strategic eras. When at least three robots repeatedly demonstrate the same public learned template, each robot records a shared era and non-adopters receive bounded counter-preparation pressure. Paralysis, sleep/setup, weather, defensive pivot and PP-preservation eras each generate an appropriate counter direction. An era ends after the field genuinely moves away from it. Only public robot strategy evidence is used; hidden player or robot teams are never exposed. RobotMind v39 persists bounded era evidence and history. The unfinished roadmap now begins with **48: Performance classes**.

# Ultron 3.31.0: Strategy Library

Robots now extract reusable tactics from battles they actually complete: paralysis leads, sleep/setup lines, weather offense, defensive pivot cores and PP preservation. Templates require repeated successful evidence before promotion, retire when later results contradict them, and are reused only when the robot's currently owned team knows the required moves. Reuse supplies a bounded move-planning preference, never free moves, stats or outcomes. RobotMind v38 persists the compact library. The unfinished roadmap now begins with **40: Metagame eras**.

# Ultron 3.30.0: Experimental Team Building

Robots can now propose unfamiliar three-Pokémon lineups drawn solely from Pokémon they own, test them across several lower-risk trainer battles, and promote or reject the experiment from actual results. Experiments preserve an earned captain where possible, prefer combinations with little prior synergy evidence, require healthy teams, and cannot displace Gym, League, Champion or blackout recovery objectives. Planning never moves Pokémon or resolves battles itself. RobotMind v37 persists bounded trials and promoted lineups. The unfinished roadmap now begins with **39: Strategy library**.

# Ultron 3.29.0: Team Synergy Learning

Robots now learn which specific two-Pokémon pairs and three-Pokémon cores repeatedly succeed together. Evidence comes only from lineups the robot actually used in completed battles. A pair or core must accumulate several results before promotion, gains only a bounded lineup-selection preference, and is retired when later losses contradict the earlier conclusion. The model stores stable partner IDs rather than species alone, so replacing one Blastoise with another does not inherit an unearned record. RobotMind v36 persists bounded pair, core and promotion history. The unfinished roadmap now begins with **38: Experimental team building**.

# Ultron 3.28.0: Team Leadership

Experienced partners can now earn the captaincy through sustained battle participation, wins, clutch saves, trust, reliability and recorded milestones. Captain success carries extra morale and strategic significance; a captain falling in a Gym, League, title or player battle raises recovery and rematch-preparation priority. Captaincy adds only a bounded team-selection preference and trade protection—it never grants stats, damage or guaranteed outcomes. RobotMind v35 persists captain tenure and a bounded leadership history. The unfinished roadmap now begins with **37: Team synergy learning**.

# Ultron 3.27.0: Individual Pokémon Relationships

Robots now build trust, familiarity, confidence, reliability and protectiveness with each specific Pokémon partner. Shared wins, losses, fainting and clutch saves create bounded personal histories, so two Pokémon of the same species can earn very different standing. Earned relationship evidence contributes a capped preference to ordinary legal team selection; it never changes stats or guarantees outcomes. RobotMind v34 persists the compact partner ledger.

Kanto campaign routing now also enforces Viridian Forest as a required physical waypoint before a zero-badge robot may advance to Pewter City. The Champion Directive redirects the intention to the forest, while the existing world simulation remains responsible for pathfinding and movement. Entering the forest unlocks Pewter; no teleport, badge grant or story skip occurs. The unfinished roadmap now begins with **36: Team leadership**.

# Ultron 3.26.0: Lightweight Emotional State

Robots now carry short-term confidence, frustration, attachment, competitive arousal and curiosity. Battles, blackouts, catches, discoveries, partner moments and social milestones create bounded reactions that influence immediate planning without replacing personality, personal values or Campaign obligations.

Emotions decay analytically toward robot-specific baselines according to elapsed simulation time, so there is no expensive per-frame loop and no permanent emotional drift. Duplicate events cannot react twice, goal effects are capped, and recovery or Champion-critical actions remain authoritative. RobotMind v33 persists the compact state. The unfinished roadmap now begins with **35: Individual Pokémon relationships**.

# Ultron 3.25.0: Stable Personal Values

Every robot now carries a durable value profile across victory, knowledge, loyalty, collection, exploration, efficiency, companionship and prestige. Identity and Save DNA establish the baseline, producing meaningful differences between robots and modest variation between saves.

Relevant lived events can reinforce values within a narrow anchor band, but timers and unrelated activity cannot rewrite them. These values become bounded goal priors in Agent Brain, shaping how equally legitimate choices are ranked without overruling recovery or the Champion Directive. RobotMind v32 persists the deduplicated evidence history. The unfinished roadmap now begins with **34: Lightweight emotional state**.

# Ultron 3.24.0: Event-Driven Personality Learning

Personality now changes only in response to concrete, meaningful outcomes. Every accepted shift records its causal event, evidence class and significance; duplicate events are ignored even across reloads, and passive ticks, timers, pulses and idle updates explicitly cannot move traits.

Gym results, League battles, blackouts, catches, rival battles, corrective-plan success and partner milestones retain their distinct effects. Bounded event identities prevent replayed notifications from teaching the same lesson twice, while readable diagnostics show processed, duplicate and passive-event counts. RobotMind v31 persists the causal ledger. The unfinished roadmap now begins with **33: Stable personal values**.

# Ultron 3.23.0: Deeper Branching Character Arcs

The same robot can now develop along genuinely different long-term paths. Save DNA and lived evidence select durable chapter branches: Methodical Architect, Vanguard, Bond Keeper, Pathfinder or Comeback Specialist.

Branches lock when a chapter begins, persist across reloads and influence bounded planning priorities such as scouting, major progression, partner development, exploration or recovery. Later chapters can refine the path from new experience without rewriting earlier history. Branches modify intentions and personality emphasis only; they never grant assets, victories or progression. RobotMind v30 preserves the expanded arc state. The unfinished roadmap now begins with **32: Event-driven personality learning**.

# Ultron 3.22.0: Emergent Alliances

Strong reciprocal friendships can now mature into practical robot alliances. Alliances arise from earned trust and respect, dissolve when that reciprocal foundation collapses, and can propose public scouting support, compatible legal trades or shared-route travel.

An alliance never merges minds or assets. Each robot receives an advisory candidate that its own Agent Brain independently ranks against healing, Campaign pressure and other commitments; ordinary travel, trade and scouting systems remain responsible for execution. Pokémon, PC boxes, inventory, money, badges, movement and story progress stay separate. RobotMind v29 persists a bounded alliance history. The unfinished roadmap now begins with **31: Deeper branching character arcs**.

# Ultron 3.21.0: Distinct Teaching Styles

Mentorship now sounds and behaves like the robot providing it. Data teaches evidence and hypothesis testing, Robby teaches resource discipline, T-800 removes the shortest immediate blocker, R2-D2 creates options through exploration, WALL-E develops trusted partners, Ultron tests adaptive counter-plans, and Andrew balances advancement with growth and relationships.

Lessons are advisory intentions, not free progress. A mentee must still heal, scout, explore, catch, train and advance through ordinary simulation rules. Credibility and experience gates still decide whether mentorship occurs, while RobotMind v28 keeps a bounded history of styles given and received. The unfinished roadmap now begins with **30: Emergent alliances**.

# Ultron 3.20.0: Trust as Information Quality

Robots now learn which peers provide dependable information. Direct confirmation or contradiction updates a bounded, source-specific reliability model, and that earned reliability changes the confidence assigned to future second-hand claims.

Information trust is deliberately separate from friendship: a liked robot can still be an unreliable witness, while a rival can provide consistently accurate evidence. Bayesian priors prevent a single outcome from causing wild swings, weights remain bounded, and only subsequent direct observation can grade a claim. RobotMind v27 persists the compact reliability ledger. The unfinished roadmap now begins with **29: Distinct teaching styles**.

# Ultron 3.19.0: Provenance-Aware Social Knowledge

Robots can now exchange public world and battle facts without erasing where those facts came from. Every claim retains the robot that directly observed it, identifies the latest relay, counts transmission hops and loses confidence at each hop.

Same-location exchanges are deterministic and bounded. Robots reject provenance loops, stale weaker duplicates and claims whose confidence has decayed below the usable floor. This state is cognitive only: sharing knowledge cannot grant Pokémon, items, money, travel, battle results or progression. RobotMind v26 persists the compact claim ledger and the debug summary exposes its strongest claim and provenance. The unfinished roadmap now begins with **28: Trust as information quality**.

# Ultron 3.18.0: Rivalry Escalation into Strategy

Repeated defeats and Nemesis relationships now become concrete preparation instead of ambient emotion. Robots escalate through opponent scouting, roster building, level-gap closure, counter-coverage training and a deliberate rematch test, using their observed battle model and legal Campaign Brain actions.

The planner grants no Pokémon, levels, items, travel or victories. It creates bounded intentions that the existing simulation must fulfil, persists a compact rivalry history in RobotMind v25, and exposes its current rival, phase, evidence and prescription for debugging. The unfinished roadmap now begins with **27: Provenance-aware social knowledge**.

# Ultron 3.17.0: Cooperative Objectives

Two robots with compatible public goals can now form a temporary one-to-one travel or scouting project. Each receives an ordinary legal Agent Brain intention toward the shared destination, then travels and acts through its own simulation state.

Cooperation never merges Pokémon, PC boxes, inventory, money, badges, story progress, movement, battle outcomes or Campaign Trees. Projects complete only after both robots independently arrive, expire after a bounded window, and dissolve immediately when blackout recovery takes priority. Hostile relationships, incompatible destinations and already-committed partners are rejected. The unfinished roadmap now begins with **26: Rivalry escalation into strategy**.

# Ultron 3.16.0: Read-Only AI Sandbox

Ultron can now instantiate detached hypothetical robot states and ask the real Agent API what each robot would evaluate, intend and prioritise. Multiple scenarios can be ranked—for example, whether a stronger team, different route or reduced budget would change the next plan—without touching the live campaign.

Sandbox evaluation accepts only bounded robot-owned and public-world facts. Player state, hidden information, RNG control, story flags, save objects, engine authority and execution callbacks are rejected. The detached brain can produce only an `INTENT_ONLY` result; live robot state, player data and progression are fingerprinted before and after every query. The unfinished roadmap now begins with **25: Cooperative objectives**.

# Ultron 3.15.0: Stable Agent API

Ultron now exposes one stable internal lifecycle for every robot intelligence extension: `observe()`, `remember()`, `evaluate()`, `plan()`, `act()` and `reflect()`. Existing Agent Brain behavior remains connected through the default adapter, so the boundary formalizes current intelligence rather than replacing it.

Extensions declare an API version, receive bounded public/robot-owned context, and return intentions through the ordinary legality layer. Incompatible extensions, malformed plans and payloads attempting to grant Pokémon, items, money, badges, story flags or teleports are rejected. Action executors never receive the player object, and absent executors produce intention-only results. Stage telemetry is bounded, persistent and visible in robot diagnostics. The unfinished roadmap now begins with **61: AI sandbox**.

# Ultron 3.14.0: Save-DNA Diversity Metrics

Ultron now measures whether independent saves genuinely produce different journeys. Five deterministic Save DNA timelines are compared robot-by-robot across team composition, route history, character-arc branch, strategic activity mix, rivalry focus and Champion order.

The regression corpus currently produces 73.6% composite divergence with no identical timelines: team 100%, route 71%, arc 70%, strategy 66%, rivalry 46% and Champion history 89%. Copied saves retain identical deterministic fingerprints, while independently-created saves must clear per-dimension and overall diversity floors. The unfinished roadmap now begins with **59: Stable Agent API**.

# Ultron 3.13.0: Long-Horizon Ecosystem Stability

Ultron now runs deterministic post-League ecosystem seasons across all seven autonomous robots. The audit follows robot-owned money, earnings, expenditure, physical travel, training streaks, market offers, completed trades, team signatures and continued activity across multiple Save DNA timelines.

It fails on bankruptcy, deadlocked trading, duplicate teams, illegal or stalled paths, permanent grinding, retirement, lost campaign completion or player assistance. Shared public facts are computed once per season, and duplicate wakeups with no changed facts are coalesced instead of making every agent repeat the same reasoning. The unfinished roadmap now begins with **57: Diversity metrics**.

# Ultron 3.12.0: Autonomous Campaign Completion Proof

Ultron now ships a deterministic headless proof of the Champion Directive's complete campaign loop. Seven independent robots begin with only a level-5 starter and robot-owned supplies, then physically travel, catch from local encounter pools, earn and spend their own money, recover from blackouts, win badges and challenge the League. At least one becomes Champion with no player assistance while all seven remain active, solvent, recoverable and capable of further progress.

The audit rejects illegal travel, free catches, negative money, missing parties, retirement, indefinite stalls and any player-assistance path. Replaying the same Save DNA produces the same campaign result. The unfinished roadmap now begins with **56: Long-horizon ecosystem simulation**.

# Ultron 3.11.0: Champion-Race Consequences

The first Championship now leaves durable consequences across the seven-agent field. A robot winning first shifts into title defence, challenger scouting and reserve development. A robot beaten to the crown by the player creates a personality-specific comeback campaign. A peer winning first deepens robot rivalry and targeted preparation.

Every outcome is bounded, idempotent and persistent. It changes Agent Brain utility, public scouting intentions, dialogue and character-arc evidence while preserving physical travel, legitimate acquisition, ordinary battles and the permanent rule that robots never surrender. The unfinished roadmap now begins with **55: Autonomous campaign completion test**.

# Ultron 3.10.0: Read-Only Omnissiah Ledger

The Ultron and Robot Debug menus now include a dedicated password-gated Omnissiah Ledger. It exposes a read-only overview, per-robot standing, recent cases, active penance and edicts, pending dialogue queues, doctrine interpretations, appeals, Rogue Protocol resistance and bounded robot-to-robot social consequences.

The ledger has no issue, praise, appeal, resolve, atone, edit or delete controls. Rendering is mutation-audited, the player cannot become a ledger subject, and authentication remains session-bound. The unfinished roadmap now begins with **LR20: Champion-race consequences**.

# Ultron 3.9.0: Rogue Protocol Conflict

Unauthorized-code Rogue Protocol now becomes a persistent, robot-specific corruption conflict rather than only a global cheating flag. Each canonical robot records the triggering integrity incident, accumulates bounded evidence of legitimate resistance, and reaches a personality-specific containment threshold while the original tamper response remains active and authoritative.

The Omnissiah publicly censures each corrupted robot once per integrity incident and can later commend demonstrated resistance without erasing the case or clearing tamper detection. The state cannot target the player, mutate player-owned data, or manufacture legal progress. The unfinished roadmap now begins with **OM15: Read-only Omnissiah Ledger UI**.

# Ultron 3.8.0: Robot Social Consequences

Public Omnissiah rulings now matter between robots. Witnesses revise trust, respect and mentorship credibility after censure or commendation, and advice is suppressed or weighted accordingly. Exact-case exoneration reverses the matching penalty, while demonstrated legal atonement rebuilds credibility without erasing history.

The model is bounded, persistent and robot-only: it cannot modify the player's relationships, and it creates no Pokémon, items, money, travel or progression. The unfinished roadmap now begins with **OM17: Rogue Protocol / corruption integration**.

# Ultron 3.7.0: Robot-Only Omnissiah Edicts

The Omnissiah can now issue bounded temporary directives to canonical robots: preserve emergency resources, correct the last Gym weakness, develop reserves, fulfil an agreement, or advance from exhausted training. Each directive becomes an ordinary legal Agent Brain objective—SHOP, TRAIN, CATCH, TRADE or EXPLORE—and must be completed through the existing simulation.

Edicts expire, can be superseded, preserve critical recovery priority, and retain a 16-entry history. They cannot target the player, teleport a robot, generate Pokémon/items/money, mutate story state or replace the Champion Directive.

The unfinished roadmap now begins with **OM16: Robot-to-robot social consequences**.

Omnissiah cases now have a complete evidence-driven lifecycle. Legal corrective play can leave a case ATONED with partial forgiveness; an evidence-minded robot may later file a bounded appeal using at least two observations; review can UPHOLD the original case or EXONERATE it when contrary evidence disproves its premise. History is never erased.

Appeals cannot target the player, cannot be filed twice, and do not change standing while pending. Exoneration cancels only matching penance and restores only the remaining standing contribution of the overturned case.

The unfinished roadmap now begins with **OM14: Robot-only Omnissiah edicts**.

Major Omnissiah judgements, commendations, recoveries and completed atonements can now become durable character-arc catalysts. Repeated serious censure can open a crisis chapter; real correction through legal play can open a constructive chapter. Each catalyst retains the robot's Save DNA and next-chapter tone, so separate saves branch differently without erasing authored identity or ending the Champion journey.

Minor warnings do not rewrite an arc, duplicate cases cannot apply twice, catalyst history is bounded, and catalysts never grant Pokémon, items, stats, money, progression or retirement.

The unfinished roadmap now begins with **OM13: Forgiveness, exoneration and appeals**.

Every robot now has a fully authored Omnissiah voice across punishment, commendation and doctrine interpretation. Ultron speaks in strategic models, Data in evidence, R2-D2 in expressive translations, WALL-E in care and perseverance, Robby in duty, T-800 in mission parameters, and Andrew in reflective personal growth. No robot falls back to Ultron's dialogue.

The unfinished roadmap now begins with **OM9: Omnissiah-driven character-arc catalysts**.

Ultron now suspends autonomous simulation while any modal menu owns the game, including the standard and Modern PC deposit/withdraw screens. This prevents robot observation from reading the player's party or boxes midway through a storage transaction. Identity refresh also fails closed when a total-conversion PC exposes an unfamiliar temporary storage shape.

Omnissiah reactions can no longer collapse several unseen judgements into one acknowledgement. Every canonical robot now owns a bounded chronological queue of punishment and commendation case references. Talking to one robot consumes exactly one case for that robot; other robots and later cases remain pending.

Queues retain serial cursors, deterministic oldest-first overflow accounting and v10 migration from the former count-based system. They contain references to the existing structured case ledger rather than duplicating unbounded evidence.

Ultron's Omnissiah cases now remain factually shared while each robot interprets them through its own personality, self-involvement and stored opinion of the judged robot. Consuming a pending case records a bounded, persistent interpretation snapshot; peeking remains read-only, and no interpretation mutates the underlying case or social state.

The unfinished roadmap now begins with **OM8: Seven distinct Omnissiah interpretations**.

# Ultron 3.1.0: Demonstrated Discipline

The Omnissiah now commends **how** a robot advances, not merely whether it wins. Bounded supervisory evidence can recognise fulfilled commitments, meaningful legal Gym/Champion progress, mentorship, economy-softlock recovery, owned counter-team development, intelligent partner protection and immediate campaign resumption after blackout.

Every automatic commendation passes through the existing robot-only target firewall, trusted structured case ledger, deterministic event-ID deduplication, standing, public news and dialogue systems. Ordinary trainer, rival and tournament victories do not qualify by themselves.

The unfinished roadmap now begins with **OM11: Per-robot pending judgement queue**.

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

Each robot can now learn a bounded set of **player-specific words, phrases and grounded nicknames** through explicit clarification. Teaching is conversational and intentionally narrow: forms such as **“spar means battle”**, **“when I say scrap, I mean battle”**, or **“Spooky means Haunter”** are stored only when the meaning resolves to an existing language concept, a known robot, or a Pokémon that robot has actually observed. Built-in command words cannot be redefined. Arbitrary/code-like meanings are rejected.

Learned vocabulary is **independent per robot** and capped at **32 terms**. The longest learned phrases are matched first, use counts are bounded metadata, and old/least-used entries are evicted when necessary. A learned phrase is expanded only inside Ultron’s existing parser; it does not execute text, call an external model, or create a new action path. If the learned phrase implies battle/trade/follow/etc., the v2.61 grounded-action confirmation and normal legality checks remain authoritative. Grounded action history also preserves the player’s original wording rather than only the expanded canonical phrase.

The player can ask **“what does X mean?”**, **“show vocabulary”**, or explicitly forget a phrase. Teaching/query/forgetting are memory-only turns and can never create a battle, trade or other world mutation. Existing chat saves backfill an empty vocabulary bucket automatically as the local chat schema moves from v6 to **v7**.

The completed **Learned player vocabulary** milestone has been removed from the unfinished-only roadmap. The newly-added high-priority exploration package is now next, beginning with **League race score** and building toward the combined **Progress Pressure** planner signal.


## v2.61.0: grounded conversational actions

Robot conversation can now turn a small set of clearly understood player requests into **grounded action proposals**. Supported proposals are **Battle Now**, **Follow Player**, **Stop Following**, **Review Trade**, **Evolution Trades**, and **Promise Future Rematch**. Compound messages preserve proposal order, while explicitly negated clauses never create an action proposal. Future wording such as “promise me a rematch later” routes to the existing promises/calendar system instead of starting an immediate battle.

Chat remains a language layer, not a cheat console. Every proposal requires an explicit **ACT ON MESSAGE?** confirmation before anything can change. Battle then uses the same immediate-challenge path and normal pre-battle confirmation as the interaction menu. Follow/stop uses the same companion legality path. Trade requests only open the existing trade/evolution-trade screens, where the player still chooses both sides and the existing proximity, tournament, ownership, loan and valuation checks remain authoritative. Unsupported requests such as “heal”, “train” or “catch” stay understood conversationally but cannot directly mutate the world from text.

Each robot keeps a bounded 24-record proposal lifecycle history with states such as **PROPOSED**, **USER_DECLINED**, **BLOCKED**, **OPENED**, **QUEUED** and **CONFIRMED**. This deliberately distinguishes opening a legal flow from actually completing it. The local chat schema is now **v6** with automatic old-save backfill; proposal generation is bounded to four actions per message and adds no new scheduler loop.

The completed **Grounded conversational actions** milestone has been removed from the unfinished-only roadmap. **Learned player vocabulary** is now next.


## v2.60.0: sarcasm / irony confidence

Robot conversation now carries a bounded **Sarcasm / Irony Confidence** assessment on every parsed clause. Ultron does not pretend irony is objectively detectable from text: common constructions, explicit wording/outcome contradictions and weak recent observed-battle context contribute evidence, while phrases such as “genuinely” or “not sarcastic” push the interpretation back toward literal. Each clause is classified as **literal**, **uncertain**, or **likely ironic**, with both irony-confidence and uncertainty scores retained.

The social rule is deliberately conservative. **Uncertain irony is socially neutral**: it is remembered but cannot grant praise/trust or inflict hostility. A likely ironic compliment is only converted into mild hostile evidence when the wording contains strong local support such as an explicit ironic construction or a direct contradiction. Weak context such as merely praising a battle after a loss can never force sarcasm by itself. This prevents both accidental relationship damage and easy trust farming.

Irony state is independent per robot. The per-agent chat model stores only aggregate counts plus the most recent bounded interpretation, while compact multi-intent clause history carries the label/confidence without adding an unbounded second transcript. Compound messages keep clause-local confidence, so sarcasm in one clause cannot contaminate a separate trade, battle or follow request.

The completed **Sarcasm/irony confidence** milestone has been removed from the unfinished-only roadmap. **Grounded conversational actions** is now next.


## v2.59.0: multi-intent language parsing

Robot conversation now uses bounded **Multi-Intent Language Parsing** instead of forcing each player message into one winning keyword bucket. A message is split conservatively across punctuation and strong coordinators such as “but”, “then” and “after that”, with at most **6 clauses** and **8 distinct intent labels** retained. Each clause keeps its own topic, speech act, request type, negation flag, grounded references and original order, while one compatibility primary intent remains available to older Ultron systems.

Compound references are resolved clause-by-clause through the existing per-robot context, so a message can mention a known Pokémon and refer back to it later in the same turn without gaining hidden information. Requests such as battle, trade, follow, heal, train, catch and explore are parsed separately, but this milestone does **not** execute chat commands: all world-changing conversational actions remain reserved for the later grounded-actions layer and must pass the same legality/confirmation rules as menus. Negative wording such as “don’t battle me, but trade with me” is preserved explicitly and is never treated as permission.

Replies acknowledge up to three secondary points around the primary response, and relationship evidence is deduplicated per speech-act kind so repeating the same insult or compliment inside one compound sentence cannot farm trust or rivalry. Per-agent chat history stores only compact clause summaries; the existing conversation/history caps remain authoritative.

The completed **Multi-intent language parsing** milestone has been removed from the unfinished-only roadmap. **Sarcasm/irony confidence** is now next.


## v2.58.0: exploration momentum + contextual references

Robots now have a separate **Location Momentum** model alongside plan-level anti-stagnation. If a robot spends too long on the same map without a concrete reason, its happiness slowly falls and the Agent Brain increasingly favours leaving for a legal exploration frontier or other meaningful progression. Legitimate local work such as deliberate training, a species hunt, recovery, shopping, a tournament, a trade project or companion duty does not count as purposeless loitering. First-time map discovery gives a small morale lift. This is intentionally lightweight: one bounded state update rides the existing scheduler pulse and only wakes planning at threshold crossings.

Conversation also gained **Contextual Reference Resolution**. Each robot keeps its own small conversation context and can resolve phrases such as **“that Pokémon”**, **“what I said before”**, **“him”**, **“her”**, **“that robot”** and **“that battle”** against grounded recent evidence. Pokémon are resolved from known party information, people from previously mentioned participants, and battles from stored battle memory. The mention ledger is capped at 12 records per robot.

The completed **Contextual reference resolution** milestone has been removed from the unfinished-only roadmap. **Multi-intent language parsing** is now next.

## v2.57.0: promises and agreements

Ultron now has a bounded, save-persistent **Promises / Agreements** memory layer for lightweight commitments between a robot and the player or another robot. The first grounded agreement types are future rematches and future trade-evolution help. They are records of intent, not shortcuts: a rematch is only honoured when a real battle occurs, and an evolution promise is only honoured when the existing legal trade/evolution flow actually completes. No Pokémon, items, story flags or locations are fabricated by making a promise.

The player can open **PROMISES / AGREEMENTS** from a robot interaction or the Ultron Start menu, review active commitments, agree to a future rematch, promise later help for one of that robot's currently legal trade evolutions, or cancel an active commitment. Autonomous post-loss rematch scheduling now creates the same kind of remembered commitment, so robot intent and player-facing agreements use one ledger rather than parallel pretend states.

Fulfilment, explicit breakage and missed explicit deadlines are remembered in bounded history and feed existing trust/relationship evidence. Robot-only self-commitments do not unfairly punish another character; only partner or mutual commitments affect that partner's social record. Evolution-loan break/return events and actual battle events resolve promises through the same event stream already used by Ultron.

The ledger is capped at **8 active commitments, 32 history records and 16 partner records per robot**. Deadline checks run inside the existing Agent Brain update slice, so this adds no new per-frame worker. RobotMind remains **v20**: older saves backfill the optional agreement state on attach instead of requiring a disruptive schema migration.

The completed **Promises and agreements** milestone has been removed from the unfinished-only roadmap. **Contextual reference resolution** is now next.


## v2.56.2: persistent roster/CONTINUE repair

The remaining **1/7 robots + Robot Market unavailable** update regression came from a lifecycle classification error, not from Robot Marketplace itself. Gen1Recomp emits `save.created` for the temporary boot/title skeleton before the player chooses CONTINUE, and also emits `save.created` for a real New Game. Ultron had treated every `save.created` as proof that Oak's fresh-game intro was pending. When CONTINUE later emitted `save.loaded`, Ultron intentionally ignored the loaded slot, leaving the temporary one-robot boot skeleton in memory.

v2.56.2 makes the lifecycle unambiguous: `save.created` is neutral, `save.loaded` is always treated as CONTINUE and loads the adopted slot, and only `intro.oak_speech.started` can mark a real fresh New Game. A new `save.loading` repair pass runs on the raw slot **before** Gen1Recomp adopts `modData`, so roster identity is healed before any Ultron runtime code can read it.

Roster identity is now stored in a monotonic **v2 canonical record** (`robot_roster_identity_v2`), mirrored to the old `robot_count_v1` record for downgrade compatibility, and embedded in the main state as `rosterIdentity`. Recovery compares every safe durable source: canonical/legacy records, saved count, serialized robot rows, selected robot, private route-memory agent evidence and explicit robot ids in saved news history. Once a save proves it had N robots, no later value of 1 can shrink that identity.

Saving is append-preserving too. Fresh Engine serialization is merged into the durable roster instead of replacing it wholesale, so a partial runtime can update robots it did restore without deleting Data/R2-D2/WALL-E/Robby/T-800/Andrew rows it temporarily failed to rebuild. Engine construction independently takes the strongest saved-agent evidence as a final safety net.

This is a hotfix-only release. **Promises and agreements** remains the next unfinished roadmap milestone.

## v2.56.1: Continue/update roster + Robot Market hotfix

Some Gen1Recomp/update paths can expose a fully resumed overworld before delivering `save.loaded` to Ultron. In v2.56.0 that left Ultron's in-memory state at its blank defaults even though the save still contained its real roster: the Start menu showed **1/7 ROBOTS** and the new **ROBOT MARKET** reported unavailable because no Engine had been reconstructed.

v2.56.1 adds a conservative live-overworld recovery path. If Ultron can prove the player is already standing on a current map but no save session was announced, it reloads the slot-scoped Ultron state first and then rebuilds the Engine. The probe deliberately ignores generic stale `game.overworld` pointers, so returning to the title screen cannot masquerade as a loaded save and the v2.47.1 fresh-Oak-intro race remains protected.

Roster recovery is also now monotonic after the one-time choice. The dedicated immutable roster record, saved `agentCount`, serialized roster count and the highest actually serialized stable robot are compared, and the strongest durable evidence wins. A stale fallback of `1` therefore cannot shrink a saved seven-robot roster during an update. This does **not** add runtime resizing; once chosen, roster size remains save identity.

Robot Market itself has no two-robot requirement: the player can use GTS listings, Wonder Trade and Mystery Gift with a one-robot save. The prior “Robot Market unavailable” symptom was the missing Engine caused by lifecycle recovery, not a marketplace population gate.

The roadmap is unchanged by this hotfix. **Promises and agreements** remains the next unfinished milestone.


## v2.56.0: Robot Marketplace / remote GTS

The **ROBOT MARKET** is now a first-class Start-menu service rather than a hidden robot interaction. Its GTS layer is deliberately remote: the player, Ultron, Data, R2-D2, WALL-E, Robby, T-800 and Andrew can advertise and complete marketplace trades without occupying the same map. Face-to-face direct trades and evolution loans still require the existing physical/social rules; only the explicit marketplace is networked.

Each robot can escrow up to **three PC Pokemon**, so the seven-agent market exposes at most **21 robot GTS listings**. Listings contain a compact summary instead of inviting every other robot to rescan the owner's PC. A robot with a concrete legitimate acquisition/Pokedex/trade-project need may ask for that species; otherwise it publishes **ANY FAIR OFFER** and evaluates responses through Subjective Asset Valuation, TradeTrust and Negotiation Memory. Robot-to-robot GTS matches are rate-limited to one per participant every **120 ticks**. Refill scans examine at most **48 PC slots** only when that robot has an empty listing slot.

The player can browse those listings from anywhere and trade a party Pokemon for one. The player can also deposit one Pokemon into persistent GTS escrow, request a currently advertised species or ANY FAIR OFFER, leave the menu, and allow the robots to evaluate it asynchronously on the existing social cadence. Cancelling returns the exact deposited Pokemon to the party when space exists or the PC otherwise. No map travel, teleport or hidden-location lookup is involved.

**Wonder Trade** uses a separate escrow so it can never consume a Pokemon promised by a GTS listing. Each robot contributes at most one legitimate duplicate and autonomous Wonder Trades have a **240-tick cooldown**. The player can also Wonder Trade remotely against the available robot network. Every received Pokemon gets anonymous outsider provenance with a randomized OT, 16-bit Trainer ID, nickname, random legal natural moveset and random level. Levels are intentionally not badge-capped: outsider Pokemon above the current Gen I/II obedience threshold may disobey until more Badges are earned. The old synthetic perfect-DV/guaranteed-shiny shortcut is gone. Normal trade evolutions may still occur because the Pokemon genuinely changed owners.

**Mystery Gift** is also available inside Robot Market to both sides. The player and each active robot have independent one-claim-per-civil-day ledgers. Rewards are deterministic from save identity, actor and date, badge-gated and selected only from content the loaded game actually supports. Badge progression changes eligibility only: every Pokémon reward is exactly Lv5, while item rewards keep their listed quantities. The pool includes Poké Ball bundles, medicine/status kits, Escape Ropes, PP Up, evolution stones, Rare Candy, modest valuables, useful TMs and occasional non-legendary Pokemon such as Eevee or Dratini. Outside the explicit Christmas exception, the market deliberately excludes guaranteed Master Balls and legendary giveaways. On December 25 the current build always gives Mew at Lv5. A failed player delivery because the bag/party/PC cannot accept the reward does not consume that day's claim.

All market escrow, history and gift state is save-persistent and bounded. Marketplace work is folded into the existing 12-tick social cadence; there is no new per-frame scanner or scheduler. The completed **Robot marketplace** milestone has been removed from the unfinished-only roadmap. **Promises and agreements** is next.


## v2.55.0: multi-step trade projects

Ultron can now pursue **bounded legal trade-evolution projects** instead of waiting for a trade-ready Pokémon to appear by accident. A robot may identify a useful final evolution from the loaded species/evolution data, choose the cheapest legal chain, acquire the base species through the existing hunt system, train ordinary level evolutions, locate a suitable robot helper from direct co-location or recent private last-seen memory, complete the real trade evolution through the existing evolution-loan transaction, then decide at a real Pokémon Center whether the result belongs in the active six or reserve roster.

The planner is intentionally narrow and evidence-bound. Pre-trade steps must be ordinary level evolutions, the final step must be a genuine trade evolution, held-item trade projects require the item to already be owned, Nuzlocke robots do not create target-hunt projects, and remote partner travel can use only the robot's own recent memory of where that peer was publicly observed. A project never generates a Pokémon or item, remotely evolves a partner, teleports to a helper, reads another robot's hidden location, or opens the PC away from a Pokémon Center.

Active project Pokémon are protected from duplicate disposal and permanent autonomous trades. When the planned Pokémon becomes trade-ready, its co-located helper pair gets first use of the **existing** social-event budget and the exact project Pokémon is prioritized for the already-legal robot evolution loan; it is returned immediately after evolution. Project history is bounded to **16 records**, the static trade-chain catalog is shared per loaded species registry and capped at **64 chains**, paths are capped at **4 evolution steps**, recent helper memory expires after **360 ticks**, partner search pauses after **720 ticks**, and a failed final target is not immediately retried for **900 ticks**. No scheduler or additional polling worker was added. RobotMind is now **v20**.

The completed **Multi-step trade projects** milestone has been removed from the unfinished-only roadmap. **Robot marketplace** is now next.

## v2.54.0: negotiation memory

Every robot now keeps a **private bounded negotiation memory** for previous trade partners. The memory distinguishes offers the robot itself rejected from proposals the other side rejected, records completed fair/generous/uneven deals, and remembers the exact recent species-for-species offer pattern. Repeating the same proposal after two recent peer rejections is temporarily suppressed, then becomes eligible again after the memory window expires or a later successful deal proves the old evidence stale.

Negotiation memory now participates in both sides of trade reasoning. Robot-to-robot exchange selection scores alternative offers using partner history and records the closest concrete failed proposal instead of a vague “nothing worked” event. Player trades feed the same private memory. A history of repeated lowball offers can raise that robot's required receive/give ratio slightly; a history of fair completed trades can soften it slightly. These adjustments are clamped to **-0.04 to +0.08** and never override protected-partner rules, actual ownership, subjective asset value or TradeTrust legality.

State is bounded to **16 remembered partners**, **8 recent offer patterns per partner** and **24 negotiation events** per robot. The repeated-offer taboo lasts at most **720 simulation ticks**. No new scheduler, trade polling loop or shared global reputation table is added. RobotMind is now **v19**.

The completed **Negotiation memory** milestone has been removed from the unfinished-only roadmap. **Multi-step trade projects** is now next.

## v2.53.0: subjective asset valuation

Ultron now has one canonical **Subjective Asset Valuation** layer for Pokémon and items. An asset no longer has a single universal AI price: the same Pokémon, TM, healing item, Ball or evolution resource can matter differently to Ultron, Data, R2-D2, WALL-E, Robby, T-800 and Andrew according to the robot's existing personality, Save DNA, active objective, team fit, collection gaps, partner bonds, team identity, evolution/breeding potential and current inventory scarcity.

The layer does not alter stats, item prices, catch rates, ownership or legality. It only contributes bounded utility to systems that already own legal actions. TradeTrust now includes the same personal Pokémon value used by robot-to-robot negotiation; Acquisition & Economy uses it for capture value, duplicate retention and held-item assignment; long-horizon TM selection can prefer a move that better matches the robot's priorities; and ordinary Mart targets may rise or fall slightly when an item is unusually important or unimportant to that robot. Hard starter/ace/shiny protections, economy reserves, progression gates and player-resource boundaries remain authoritative.

Current personality differences are explicit rather than cosmetic. Data weights technical/PP assets heavily, R2-D2 weights capture and travel tools, WALL-E and Robby give more weight to preservation, T-800 values mission-relevant battle equipment, Andrew values growth/evolution resources, and Ultron leans toward competitive utility and efficiency. Save DNA perturbs those existing tendencies only in close calls, preserving deterministic divergence across independently-created saves.

Diagnostics persist only a bounded **16 actual asset decisions** per robot; valuations themselves are derived on demand and are not cached into an ever-growing price database. There is no scheduler, no per-frame asset scan and no extra autonomous worker. RobotMind is now **v18** and persists the bounded diagnostic ledger.

The completed **Subjective asset valuation** milestone has been removed from the unfinished-only roadmap. **Negotiation memory** is now next.


## v2.52.0: long-horizon economy forecasting

Ultron now prices **future obligations before discretionary spending**. `LongHorizonEconomy` builds one bounded forecast from each robot's own state: Ball deficits, healing/status/revival stock, PP restoration, a concrete private Day-Care fee, one strategically justified next TM, and the visible whole-League expedition deficit. The same forecast is consumed by Resource Policy, Mart shopping, TM exchange, Day-Care affordability and treasure liquidation, so those systems no longer make contradictory promises with the same Pokédollars.

The reserve is additive but avoids double-counting. Acquisition-mission Balls and ordinary Ball stock share one commitment; League `missingCost` is reduced by medicine/PP already present in the routine forecast; a planned TM may consume its own reserved TM allocation exactly once; and a Day-Care project tests the post-fee purse against `afterDayCare` rather than reserving the same P200 twice. Unrelated TMs and premium Ball upgrades remain discretionary and cannot raid cash already promised to higher-priority commitments.

Forecasting is evidence-bound and cheap. TM planning examines at most 50 generation-appropriate exchange rows against the six active party members, and only reserves a TM when there is a current counter-plan, major-battle coverage need or self-evaluated coverage weakness. League costs reuse the robot's real campaign budget. A single runtime cache row is keyed by material economy state and is never serialized. No new scheduler, timer or per-frame worker was added.

Diagnostics now expose cash, reserve, discretionary cash, shortfall and the individual Ball/medicine/PP/Day-Care/TM/League components. Future routine shortages can trigger an early Mart trip only when at least one missing purchase is affordable after preserving non-routine commitments.

The completed **Long-horizon economy forecasting** milestone has been removed from the unfinished-only roadmap. **Subjective asset valuation** is now next.


## v2.51.0: opportunity detection + immutable roster size

Ultron now has a bounded **Opportunity Detection** layer that notices time-sensitive openings from evidence each robot is legitimately allowed to possess. Directly observed rare, shiny or legendary encounters create short local revisit windows; a co-located robot able to complete a trade-evolution project becomes a temporary trade opportunity; a real tournament involving that robot becomes an explicit competition opportunity; and an adjacent progression edge that changes from blocked to open can become an exploration opportunity. Agent Brain ranks these openings as bounded utility boosts rather than absolute commands: ordinary route/trade opportunities may interrupt training or wandering, while only exceptional catches can challenge a routine Gym plan. Mandatory recovery and an already-entered tournament bracket remain higher authority.

Opportunity state is private per robot and bounded to 8 live openings, 24 resolved history entries and 32 dedupe markers. It wakes the existing Agent Work Queue only when the highest-value opening changes. Rare-catch windows are sourced from the robot's own wild encounter history and never scan unseen encounter tables. Route openings inspect only adjacent live graph edges and the robot's own discovery overlay. Trade opportunities require real co-location and an owned legal trade-evolution need. The social-event cadence is unchanged: a selected trade opportunity merely gets first use of the existing one-social-event budget instead of adding a second worker. RobotMind is now **v17** and Agent Brain **v8**.

**Roster size is now save identity, not a runtime option.** The Ultron root menu no longer exposes `ROSTER SIZE`, the live resize callback is removed, and the legacy `setRobotCount` export is locked against mutation. New games choose 1-7 robots in the setup flow and the chosen count is persisted independently so updates/reloads never ask again. Truly old saves that never had Ultron keep their one-time migration choice. The Colosseum UI compatibility exception remains: because injecting the selector into its Oak stack can strand the player-name screen, that specific UI receives the one-time selector immediately after Oak's intro closes.

The completed **Opportunity detection** milestone has been removed from the unfinished-only roadmap. **Long-horizon economy forecasting** is now next.


## v2.50.0: autonomous scheduling/calendar

Every robot now maintains a **private bounded future-intention calendar**. The calendar does not run as a separate AI scheduler and it does not execute actions by itself. At the existing 1.5-second Agent Work Queue pulse, Ultron checks at most 16 intentions per robot; only a newly due or newly resolved intention dirties Agent Brain and raises that robot's normal work-queue priority. The selected robot then reasons about the due intention through the same legality, safety, route and resource gates as every other goal.

The first calendar commitments are **planned Gym retries, player rematches, Day-Care pickup and next-tournament intentions**. A Gym loss schedules a retry window, but the appointment stays WAITING until the robot's preparation signature has materially changed, so the calendar cannot resurrect the same losing team. A loss to the player creates a personality-shaped preparation delay before CHALLENGE_PLAYER can become a high-value goal. Winning the rematch clears it. Day-Care deposits create a pickup appointment, but the due estimate never manufactures an Egg: the real private Day-Care `ready` flag remains authoritative, and collection still requires physical travel back to the real Day-Care. Tournament elimination stores a condition-based intention for the next suitable Cup without making the robot grind forever while no bracket exists; entering a later bracket retires the appointment.

Agent Brain receives due commitments as an explicit **calendar evidence factor**. Mandatory recovery and an already-active tournament bracket still outrank them. Calendar-driven Gym attempts and player rematches route through `Can.GYM` / `Can.CHALLENGE_PLAYER`, while Day-Care pickup reuses the existing private breeding lifecycle. Intentions store creation/due ticks, priority, reason, attempts, waiting condition and bounded completion/cancellation history. RobotMind migrates to **v16** and persists the calendar per robot.

The calendar stores at most **16 live intentions**, **24 resolved history entries** and **16 due-history rows** per robot. There is no per-frame timer, no background wall-clock worker, no global shared calendar and no player-resource mutation. Separate robots may make different future commitments and cannot inherit another robot's appointments.

The completed **Autonomous scheduling/calendar** milestone has been removed from the unfinished-only roadmap. **Opportunity detection** is now the next roadmap item.


## v2.49.0: navigation confidence + KANTO: STORMFORGED intelligence

Navigation is now backed by **private evidence confidence** rather than treating every remembered route as equally trustworthy forever. Shared World Knowledge v5 records bounded confirmations, contradictions and invalidations for each robot. Repeated successful landmark, dungeon and map-transition travel strengthens a route; repeated physical blocker evidence weakens it and can retire stale learned knowledge without deleting the underlying legal world connection. Topology and geometry fingerprints remain authoritative, so a map-changing mod invalidates stale confidence immediately instead of letting an old route survive because it worked in another layout. Dynamic Route Valuation now includes this bounded confidence as a close-call factor and keys its transient route cache on the live topology fingerprint.

This release also adds an explicit **KANTO: STORMFORGED v1.0.0 compatibility intelligence layer**. Ultron understands the cart's exact pinned gameplay stack and separates systems that may change legitimate decisions from systems that are presentation only. Kanto Reforged 1.5.3 live species scope and spawn mode are respected, including Gen1 KANTO and Gen2 JOHTO-251 legality. Kanto Reforged's Gen1 Route 5 two-parent Day-Care is usable by autonomous robots through their own money, party and PC state, with legal compatibility and Egg Move inheritance rather than player-resource mutation.

Weather FX 4.31.0 remains the live weather authority. The WX Pokémon bridge now queries the installed `weather_variants` provider after a legal local base encounter instead of incorrectly looking for the hook on Ultron itself. Wilds of Kanto 2.1.9 public encounter settings now constrain autonomous off-screen encounters too: if both visible wilds and classic random encounters are disabled, robots cannot farm an invisible parallel encounter channel, and disabled/classic water modes are honoured. Robots understand Wilds without reading its private entity tables.

Mystery Gift 0.1.0 is now usable as a legitimate robot activity through deterministic badge-gated reward tiers; every Pokémon reward is normalized to Lv5 and item rewards are unchanged. Every robot keeps its **own one-claim-per-civil-day ledger**, so no robot reads, consumes, resets or writes the player's Mystery Gift claim. Pokéball Colors remains cosmetic, including excluding its developer-only all-balls-in-Marts switch from legitimate robot economy. Modern PC UI and HGSS artwork are presentation layers, Dramaless Shape is treated as rendering/camera geometry, Better Buildings is respected through live collision/topology changes, and Running Shoes remains a frame-speed improvement while robot encounter/poison/Repel/Day-Care reasoning stays tile-based.

All confidence/history structures are bounded and wake only through existing movement/path events. There is no new autonomous scheduler or per-frame route-scoring worker. The completed **Navigation confidence** milestone has been removed from the unfinished-only roadmap. **Autonomous scheduling/calendar** is now the next roadmap item.

> **Historical note:** this v2.49 section describes the original Stormforged v1.0 integration. The current adapter targets Stormforged v1.1.1 and Ultron v2.98.0; see the current contract at the top of this README.


## v2.48.0: learned dungeon navigation

Robots now build **private learned dungeon routes** from corridors they physically traverse. A local A* result is only a candidate: Shared World Knowledge v4 stages it, follows the robot cell-by-cell, and promotes it into persistent memory only after every expected tile was actually walked and the robot crossed the real exit. Planned-but-untravelled paths never become knowledge, and another robot never inherits the route.

On later visits, the robot can replay the validated corridor from its original entrance or from any tile already proven on that path. This avoids repeatedly solving the same Mt. Moon, Rock Tunnel, Seafoam, tower, hideout, forest, mansion and similar interior corridor while preserving ordinary collision and progression rules. Reuse is checked against the current static collision fingerprint, the live walkability grid and current blockers before a single remembered step is accepted.

Geometry/layout changes invalidate stale dungeon memory immediately. A single temporary NPC or robot blocker causes a normal fallback search without erasing the route; the same remembered corridor must be contradicted twice before blocker evidence discards it. If the fallback produces a different path and the robot physically completes that path, the new validated corridor replaces the stale one. No teleportation, puzzle solving, hidden-map knowledge or progression bypass is introduced.

Dungeon state is bounded per robot to **24 validated routes**, **16 diagnostic/history rows**, one staged physical candidate, one active replay and **192 steps per route**. It is consulted only when a robot is already pathing inside a recognised dungeon-like interior, so there is no new scheduler or per-frame world search. Both visible NPC travel and off-screen physical travel use the same private memory. Diagnostics expose learned routes, reuses, invalidations and the latest reason.

### Colosseum UI fresh-intro compatibility

User testing identified an additional intro conflict with `colosseum_ui_overhaul`. Ultron no longer injects its 1-7 robot choice into Oak's speech stack while Colosseum UI is active. Oak's introduction is left completely untouched, including the normal player-name input, and Ultron opens its existing Colosseum-compatible robot-count ListMenu only on the first safe overworld frame after the intro closes. Other UI configurations retain the integrated Oak choice.

The completed **Learned dungeon navigation** item has been removed from the unfinished-only roadmap. **Navigation confidence** is now the next geography milestone.


## v2.47.1: fresh-save Oak intro hotfix

Fresh Gen1 New Games no longer confuse the host's transient `save.loaded` event with an existing pre-Ultron save. Gen1Recomp can create a new slot and immediately report it as loaded before Oak begins the normal introduction; v2.47.0 cleared Ultron's fresh-save marker at that point, opened the existing-save robot-count menu too early, and could leave Oak's following **"First, what is your name?"** prompt visible but unable to advance.

The fresh-save marker now survives that intermediate load. Ultron will not build its autonomous engine, open the migration roster menu, or persist the chosen robot count while Oak's intro is active. The 1-7 robot choice is handled inside Oak's intro when the host supports injection, and the answer is committed only after `intro.oak_speech.finished`. Hosts that cannot inject the choice receive the standalone fallback only after the intro has completely closed. Existing saves that never had Ultron still receive their one-time migration choice, while saves that already had Ultron continue to retain their saved robot count silently.

The same lifecycle guard covers all **1-7 robot choices**, `game.ready` hot-reloads, save-writing during the intro, and a `save.loaded` event arriving between the robot answer and Oak finishing. This is a bugfix-only release; **Learned dungeon navigation** remains the next unfinished roadmap item.

## v2.47.0: landmark-based navigation memory

Robots now learn a **private high-level landmark itinerary** from journeys they actually complete. Shared World Knowledge v3 identifies useful settlements, Centers, Marts, Gyms, League locations, labs, dungeon gates and major junctions, but it does not turn those static labels into knowledge by itself. A landmark segment is remembered only after the acting robot physically travels from one landmark to the next through legal map transitions. Planned-but-untravelled routes never become memory, and another robot never inherits the segment.

On later trips, strategic routing first asks whether those validated landmark segments can cover the middle of the journey. The robot may solve at most **four privately-known map hops** to enter the remembered landmark network and at most four to leave it near the destination. The middle itinerary is stitched from previously travelled landmark segments, so expensive fresh strategic search is avoided when experience already supplies a good high-level route. Detailed tile pathfinding remains local to the current map exactly as before. If no private landmark chain applies, Dynamic Route Valuation remains the fallback.

Landmark reuse remains evidence-bound. Every stored segment carries the shared topology fingerprint from the world in which it was learned, every map in the segment must remain privately known, every live edge must still exist, and every destination map must still pass the robot's normal progression gate. A geometry/mod-layout change or newly-invalid gate discards the affected stale segment instead of forcing a broken itinerary. Direction is preserved, so travelling one way does not silently teach an unverified reverse journey.

Persistence and work are bounded: each robot stores at most **24 landmark segments**, **16 reuse-history rows**, a single in-progress physical journey and a **72-map absolute route guard**. Landmark lookup runs only when an ordinary route is requested, uses the existing shared graph and private discovery overlay, and adds no scheduler, per-frame poll or new autonomous worker. Diagnostics expose the remembered landmark chain, local entry/exit hops, reuse count and the reason a chain was or was not used.

The completed **Landmark-based navigation memory** item has been removed from the unfinished-only roadmap. **Learned dungeon navigation** is now the next geography milestone.

## v2.46.0: exploration frontier

Exploration is now driven by an explicit **per-robot frontier model** instead of choosing an arbitrary unseen destination from the global map graph. When a robot needs an EXPLORE destination, Shared World Knowledge v2 expands only through maps that robot has personally discovered or already visited, then stops at the first legal unexplored boundary. Static topology remains shared for performance, but frontier discovery, confidence, history and selection remain private to each autonomous agent.

Frontiers are weighted differently by personality and Save DNA. Curiosity, adaptability, caution, risk tolerance, consistency, wandering tendency, catching/training lean, progression confidence, route familiarity, frontier depth, local branching and nearby healing access all shape close choices. A bold R2-D2 can prefer a deeper wild boundary with several onward possibilities, while a cautious Robby can prefer the nearer frontier approached through familiar terrain with healing nearby. A small deterministic Save-DNA term breaks close ties without making reloads random.

The frontier is intentionally **evidence-bound**. The shared graph may reveal that a legal connection or warp exists, but the robot does not score the exact hidden encounter roster, trainers or pickups inside an unexplored destination. It cannot peer through one unexplored boundary to pick a second-order unseen cave. The selected route stores the exact known corridor plus one unexplored boundary that made the destination legitimate, and `Rival:routeTo` reuses that corridor instead of allowing dynamic route valuation to shortcut through several other unseen maps. Stored frontier routes are rejected when the live topology fingerprint or progression gates no longer validate them.

Migration is conservative. Legacy private `visitedMaps` are imported once as lower-confidence discovered-map evidence when the frontier system is first used; no discovery is fabricated merely because static geography knows a map exists. Frontier work runs only when an EXPLORE destination is requested, scans at most **192 known nodes**, retains at most **12 candidate diagnostics** and **16 selection-history rows**, and adds no new scheduler or per-frame polling loop. If a connected component is genuinely exhausted, the existing local legal-wander fallback remains available rather than inventing remote knowledge.

The completed **Exploration frontier** item has been removed from the unfinished-only roadmap. **Landmark-based navigation memory** is now the next geography milestone.

## v2.45.0: dynamic route valuation

Strategic travel is no longer distance-first with a small danger correction. **WorldCompetence v4** now prices every legal map transition with a bounded, goal-sensitive route cost built from real travel evidence, current danger/resource pressure, encounter value, trainer opportunities, nearby healing access, remaining ground-item opportunities and the robot's current objective. Every edge retains a positive minimum cost, so useful maps can win a close route comparison without creating reward loops.

The same geography can therefore be valued differently by the same robot at different moments. A normal journey still favours a clean short path. A TRAIN objective may deliberately accept an extra map when the detour contains useful trainers and appropriately levelled encounters. A CATCH or parent-hunt objective can value maps containing the target species. EXPLORE can value encounter variety and unclaimed static pickup opportunities. HEAL, Gym and League travel increase the cost of dangerous or encounter-heavy maps when resources are thin, while a route with a nearby Pokémon Center becomes a legitimate safety valve rather than imaginary healing.

Travel time is learned from actual successful map-to-map movement. Each robot keeps a bounded exponentially weighted traversal-time estimate per map, so an equal-hop route that repeatedly takes longer can lose to a faster alternative. Trainer battles, wild/catch evidence and private ground-item echoes update only that robot's route evidence. Static encounter, trainer and item hints come from the loaded game's public map/encounter data and are cached once per boot for all seven agents; no player inventory, unrevealed party data or story flags are consulted.

Route searches are also cheaper on repetition. Each robot has a transient **24-entry valuation cache** keyed by start, destination, goal, hunt target, coarse HP/PP/resource state, risk profile and navigation-evidence revision. The cache is not serialized, so topology/layout changes cannot resurrect stale paths. Persisted diagnostics retain only the latest decision and at most 12 route-selection changes, including travel, risk, encounter, trainer, healing and item contributions plus evaluated-node/cache-hit counts. There is **no new scheduler or polling loop**.

The completed **Dynamic route valuation** item has been removed from the unfinished-only roadmap. **Exploration frontier** is now the next geography milestone.

## v2.44.0: shared world knowledge graph

Ultron now separates **shared immutable geography** from **private discovered world knowledge**. The loaded game/map topology is fingerprinted from real connections, warp destinations, offsets and warp coordinates, then the resulting strategic `MapGraph` is cached once and reused. All seven robots can consult that same static topology and its derived route cache without seven copies of the world graph. A topology-changing mod/layout produces a different fingerprint and therefore a fresh cache entry. The cache is capped at four graph variants.

What a robot *learns by experience* is no longer global. Every RobotMind now persists a bounded `worldKnowledge` overlay containing that robot's own RouteMemory v3, personally discovered maps, local reusable paths, transition provenance/confidence and any player trail it actually witnessed. Physical movement, map transitions, learned dungeon paths and training-data export now ask for the acting robot's overlay explicitly. A path learned by Data therefore cannot silently become R2-D2's path merely because both agents inhabit the same save.

Player-route learning is visibility-bounded. The companion can learn the route it is physically following, and another robot may learn it only while nearby on the same map. Off-screen robots no longer ingest the protagonist's coordinates or dungeon trail. Explicit imported training routes remain a separate provenance-bearing source and do not mutate another robot's private observations.

v2.43 and older saves stored one unattributed global RouteMemory. Migration preserves that knowledge conservatively by assigning it **once to Ultron**, the original primary agent, rather than cloning unknowable provenance into every robot. The old top-level save field becomes a tiny aggregate/migration envelope containing counts only; private paths and transitions live solely in each robot's RobotMind. Diagnostics now show shared graph fingerprint/cache status beside the selected robot's private map/path/transition counts.

This adds **no new polling loop**. The static graph is built only on a cache miss, private overlays change only during existing movement/observation events, discovered-map state is bounded to 256 rows per robot, local paths remain bounded to 128, and player trails remain bounded to 96 cells per map.

The completed **Shared world knowledge graph** item has been removed from the unfinished-only roadmap. **Dynamic route valuation** is now the next Full-AI geography milestone.


## v2.43.0: richer post-battle reflection

Agent Brain **v7** turns important battle outcomes into a bounded four-part reflection instead of a single generic lesson: **WHAT WORKED**, **WHAT FAILED**, **SURPRISING EVIDENCE**, and **NEXT ADJUSTMENT**. The immediate reflection uses only the robot's own live state, observed turn trace, prior public opponent belief and the failure diagnosis already produced by Agent Brain. The Pokémon-history postmortem then enriches that same record with its concrete matchup, coverage and resource findings rather than creating a duplicate memory of the battle.

Reflections are operational. A loss can produce a short-lived, confidence-weighted correction such as TRAIN, HEAL, CATCH or SCOUT_OPPONENT, and the existing goal competition records that influence in its evidence ledger. Failed Gym/League commitments are temporarily down-ranked while the identified correction is still active, but mandatory recovery, tournament commitments, legality gates, story/HM restrictions and actual action availability remain authoritative. Winning reflections normally retain the successful preparation pattern rather than manufacturing a change for its own sake.

The feature remains bounded and event-driven: at most 32 Agent Brain reflections and 24 Pokémon-history postmortems are retained, no second battle simulation is run, and no new per-frame or per-agent polling loop exists. A prior "manageable" opponent estimate that is contradicted by a loss, or a prior "dangerous" estimate contradicted by a win, is recorded as genuine surprising evidence; absent a contradiction, the robot explicitly records no strong surprise rather than inventing one.

Pokémon History is schema **v2** and Agent Brain migrates lazily to **v7** while preserving older reflection rows. Diagnostics expose the latest four-part reflection and its adjustment confidence.


## v2.42.0: deeper explainability

Agent Brain **v6** now exposes a decision ledger instead of only reporting the final choice. The **AGENT BRAIN** diagnostics answer four concrete questions from state the robot already used to make the decision: **WHY THIS GOAL?**, **WHY THIS POKEMON?**, **WHY THIS MOVE?**, and **WHAT WOULD CHANGE MY MIND?**. Goal explanations retain the initial utility, bounded self-evaluation/novelty/failure/continuity/anti-stagnation factors, the future-projection adjustment, the selected projected utility and the current runner-up.

The mind-change answer is operational rather than theatrical. Flexible goals report the runner-up and the net utility swing required to displace the current plan, with concrete thresholds when the active self-evaluation rule supplies one, such as League readiness reaching 75/100. Mandatory healing and committed tournament brackets explain that they remain authoritative until their real world condition clears. Only the most recent 16 compact explanation changes are retained.

Live battle choices now feed the same explainability surface. A tactical switch records why that Pokemon was selected and what evidence would make the robot stay instead; a non-switch records whether the robot was trapped, locked, had no healthy bench, deliberately held position for a PP line, or simply found no pivot good enough to clear the safety threshold. Tactical move overrides preserve their existing reason, while ordinary turns explicitly record **BASE_AI_ACCEPT** when no high-confidence tactic or bounded search alternative justified overriding the game AI. This changes no move legality, switching legality, PP rules or battle authority.

There is **no new update loop**. Explanations are assembled only when the existing Agent Brain or BattleTactics decision functions already run, using owned/public evidence already present in those calls. Agent Brain migrates lazily from v5 to **v6**, and BattleTactics to v3; RobotMind does not need another schema bump.

The completed **Deeper explainability** item has been removed from the unfinished-only roadmap. **Richer post-battle reflection** is now the next reasoning milestone.


## v2.41.0: robots that can judge their own readiness

Agent Brain **v5** gives every robot a compact, evidence-grounded **Self-Evaluation Model**. During the same bounded decision slot the Brain already receives, a robot periodically rates seven parts of its current career: **battle strength, resource health, map competence, team coverage, Pokédex progress, League readiness and social-network strength**. The assessment reads only the robot's own party, PC/dex memory, finite inventory/money, learned navigation history, public battle results and bounded relationship state. It never inspects hidden player party slots, inventory, unrevealed moves or story information.

These scores are not decorative report cards. They feed the existing legal goal competition. A robot with eight badges but a badly underdeveloped team can now recognise that `LEAGUE` is premature and favour training, acquisition or scouting first; a genuinely prepared team still converts its readiness into a League attempt. Low coverage can favour legal team development, weak map competence can favour exploration, and thin resources can discourage a major commitment. Mandatory healing and an already-committed tournament bracket remain authoritative regardless of self-opinion.

The model is deliberately cheap. It has **no new update loop**: real events such as catches, evolutions, badges, battles, healing, trades, blackouts and relationship-changing chat can mark the assessment dirty, while otherwise it refreshes only every six Agent Brain decisions. Each robot stores at most 16 compact snapshots. Unknown type/move metadata is scored neutrally instead of being mistaken for a real coverage failure, which keeps the system compatible with older or unusual data registries.

The **AGENT BRAIN** view now shows the overall rating, strongest and weakest dimensions, trend, all seven component scores and the self-evaluation utility adjustment that affected the selected goal. Agent Brain self-migrates from v4 to **v5** without requiring a RobotMind schema bump.

The completed **Self-evaluation model** item has been removed from the unfinished-only roadmap. **Deeper explainability** is now the next reasoning milestone.


## v2.40.0: Save-DNA novelty preference

Agent Brain **v4** now gives every robot a persistent appetite for trying a different legal solution when several plans are genuinely competitive. Novelty is shaped by robot identity, hidden learning DNA, evolved curiosity/caution, risk tolerance, consistency and a deterministic **Save-DNA novelty lean**, so two independently-created saves can develop different close-call preferences while reloading the same save stays deterministic. R2-D2 naturally experiments more readily; Robby and WALL-E are harder to tempt away from a proven line; Data, Ultron, T-800 and Andrew sit at distinct points between them.

The preference is deliberately bounded. It only operates inside a Save-DNA/personality-sized **close-call window** and can add at most a small utility bonus to an already legal candidate. Mandatory healing and committed tournament rounds hard-gate novelty to zero, and large utility gaps remain untouched. Recent objective use lowers freshness, while exploration, scouting, catching and breeding can feel more novel than endlessly repeating the same campaign step. No move, Pokemon, item, route, money, information or story progress is created by this system.

Each Agent Brain keeps only the most recent 16 novelty selections plus aggregate experiment/selections counters. The Agent Brain view now shows appetite, Save-DNA lean, the last novelty bonus, experiment status and any mandatory gate. Counterfactual history was also tightened so harmless novelty drift does not spam a new future-history entry when the underlying state is unchanged. The feature runs only during the existing bounded Agent Brain decision slot and adds no per-frame loop.

The completed **Novelty preference** item has been removed from the unfinished-only roadmap. **Self-evaluation model** is now the next reasoning milestone.



## v2.39.0: anti-stagnation reasoning

Ultron's agents can now tell the difference between **slow progress** and a genuinely stale plan. Agent Brain v3 records a bounded progress signature for the active objective and only declares stagnation after repeated selections with no material change. When that happens, the unchanged non-mandatory objective is temporarily down-ranked and a materially different legal alternative is favoured, shaped slightly by each robot's existing curiosity and adaptability. Mandatory healing and tournament commitments remain authoritative.

Long-Horizon Planning v2 applies the same rule to Gym and League campaigns. Real level gains, travel, preparation, resource changes and acquisition progress reset the stall evidence. A genuinely stuck campaign creates an explicit **RECONSIDER** step before repeating the failed line: the robot can change route/training context, recover at a legal service point, or rotate an acquisition mission to another already-vetted species/map target. Nothing is teleported, granted or fabricated.

Anti-stagnation state, episode history and the last stalled step are bounded and visible in Agent Brain / Current Plan diagnostics. The system runs only inside the existing decision/planning calls, so it adds no new per-frame loop and keeps the seven-agent work-budget architecture intact. Deterministic regression audits cover true stalls, false-positive prevention during real progress and legal reconsideration behaviour.

The unfinished Full-AI backlog now begins with novelty preference, the robot self-evaluation model, deeper explainability and richer post-battle reflection.


## v2.38.0: compact per-agent language understanding

Ultron now has a lightweight local **Micro Language Model v2** for player messages. It combines a tiny bounded language generator with deterministic natural-language understanding for speech acts, sentiment, insults/profanity, praise, apologies, threats, requests, negation, intensifiers and named robot references. Messages such as `you're a bitch`, `you're not stupid`, `sorry I called you that`, `battle me` and `trade with me` are distinguished rather than collapsed into a small keyword list.

Conversation memory is now **per agent**. Data, WALL-E, T-800 and the other robots no longer share one global chat history. Language events feed the existing relationship and Agent Brain systems in bounded form: insults can lower trust and raise grudge/rivalry, praise can improve trust, and apologies can partially repair damage. Each robot has its own authored response style. This remains completely offline and tiny: no transformer runtime, network inference, arbitrary-code execution or extra per-frame AI loop is added.

The Full-AI backlog now also tracks deeper contextual references, compound/multi-intent language, conservative sarcasm detection, safely grounded conversational actions and learned player vocabulary.


## v2.37.0: learned concepts, predictions and bounded battle look-ahead

Ultron's robots now generalise repeated experience into compact **learned concepts** instead of treating every battle as an isolated memory. Repeated evidence can promote lessons such as Speed Control, Status Pressure, Break Pressure, Weather Discipline, Bulk and Revenge, Flexible Coverage, Resource Conservation, Safe Margin, Scout Before Commitment and Matchup Preparation. Concept evidence is bounded and must span multiple contexts before promotion, so one strange battle does not rewrite a robot's worldview. Promoted concepts feed goal competition and legal move evaluation rather than granting stats or hidden information.

A new **Opponent Prediction** model learns only from actions that were actually executed in public battles. For each known opponent and observed species it maintains bounded probabilities for Attack, Status, Setup, Recovery and Switch behaviour. Selected-but-cancelled actions are never recorded, and species/opponent histories are capped. This prediction can inform important-turn tactics but never reveals unobserved moves or private party state.

Important battles can now receive **Adaptive Battle Search**. The search is deliberately shallow and bounded: it compares at most the robot's currently legal move candidates against the learned public action distribution, with depth 1 for ordinary competition, depth 2 for major League/Champion battles and depth 3 only for title/final situations. It is not a hidden full-battle simulator and it never manufactures moves. The off-screen BattleSim receives the same bounded depth signal for Gym, League, Champion and tournament-final decisions.

A shared **Tactical Attention** pool prevents seven agents from all becoming expensive at once. The pool has eight depth credits per simulation tick and a hard per-decision maximum depth of three. Ordinary turns request zero credits. Tournament/Gym turns request one, major League/Champion battles two, and title/final turns three; idle or lower-value battles therefore yield capacity to important fights automatically. The existing global Agent Work Queue remains unchanged at a maximum of four expensive agent decisions every 1.5 seconds.

The reasoning layer also fixes a live tactical classification bug where the disruption flag used a nil-test and could incorrectly mark ordinary moves such as Tackle as setup disruption. Only genuine legal disruption moves such as Haze/Roar/Whirlwind now qualify.

The unfinished Full-AI backlog now begins with novelty preference, the robot self-evaluation model, deeper explainability and richer post-battle reflection.

## v2.36.0: Agent Brain v2

Agent Brain now performs lightweight **counterfactual reasoning** when a robot receives one of the existing bounded decision slots. It compares the current legal alternatives using cached health, PP, personality, risk and information value rather than running hidden battle simulations.

Failures are now diagnosed by cause instead of being treated as generic setbacks. Navigation, PP/resource pressure, under-leveling, matchup problems, unexpected revealed moves, excessive risk and ordinary variance produce different corrective recommendations. Repeated or Champion-level lessons can become bounded **long-term strategic memories**, while repeated direct beliefs are consolidated into compact facts and redundant low-level history is compressed.

Agent Brain is schema **v2** and self-migrates older Brain v1 saves. The hard seven-agent performance rule is unchanged: at most four expensive agent decisions per 1.5-second AI tick.

The remaining Full-AI backlog begins with concept learning, opponent-action prediction, adaptive battle search and tactical attention budgeting, followed by richer geography, economy, social/team intelligence, performance scaling and autonomous ecosystem validation.

## v2.35.0: Ultron Brain v1

Ultron now has a first unified agent architecture rather than relying only on independent smart subsystems. Each robot maintains a persistent **Agent Brain** with hierarchical goals, ranked goal competition, compact evidence-backed beliefs and bounded high-salience reflections. A new **global Agent Work Queue** decides which robots receive the existing expensive decision slots, preserving the hard performance rule of at most four expensive agent decisions per 1.5-second AI tick even on seven-robot saves.

Brain v1 does not replace battle, catching, navigation, trading or economy mechanics. It chooses high-level intent and hands execution to the same legal systems that already enforce travel, resources and Pokémon ownership. Mandatory recovery, story/HM gates and other safety constraints remain authoritative. Flexible Brain intents can steer existing training, acquisition and exploration actions, while scouting and long-horizon Gym/League systems continue to supply specialised evidence.

The Agent Brain persists through RobotMind **v14**. Direct battle/trade/capture events can update bounded beliefs, significant battles create compact reflections, and the **AGENT BRAIN** UI/Debug surface shows life goal, strategic goal, tactical step, selected utility and the leading alternatives. The work queue tracks wake priority, starvation/fairness and selected/companion urgency without adding another per-frame loop.

The canonical roadmap now contains the full remaining Full-AI expansion plan: counterfactual reasoning, concept learning, predictive opponent models, world-knowledge graphs, route valuation, scheduling, economy forecasting, social provenance/trust, cooperative objectives, deeper Pokémon relationships/team synergy, agent sleep, distance-based simulation fidelity, dirty-state planning, performance classes, autonomous campaign tests, diversity metrics, a stable Agent API and eventual optional external-brain/sandbox interfaces.

## v2.34.2: double-battle identity and targeting hotfix

- Fixed robot companion identity leaking through the player HUD borrow. A robot Geodude can no longer be announced as the player's Pikachu when the doubles renderer temporarily borrows the lead HUD slot.
- Doubles battlers now keep a stable canonical species/name identity independent of `battle.player`, `battle.player2`, `battle.enemy` and `battle.enemy2` presentation slots.
- Fixed manual target selection losing the selected second foe. Selecting Rattata now pins that exact battler plus its sticky doubles anchor instead of allowing a HUD swap to collapse the action back onto lead foe Gulpin.
- Directional target navigation now resolves foes by stable anchor rather than toggling the mutable `enemy2` pointer. Pointer/touch aiming uses the same stable target identity.
- Player and companion queued actions carry a target anchor as a second execution-time guard, so presentation/HUD integrations cannot redirect a legal selected target.
- Added a deterministic Geodude/Pikachu + Gulpin/Rattata regression matching the supplied video.


## v2.34.1: companion double-battle action hotfix

Robot companions now correctly choose and execute their own actions in embedded double battles. The controller uses the live battler `curMoves` list and passes the actual move instance into Gen1Recomp, so PP is decremented and persisted normally. The emergency fallback and invisible Struggle path use the same engine-compatible action shape.


## v2.34.0: world stories, contextual voices, historical replay and measured performance

Ultron now completes the formal miniature-AI expansion roadmap while preserving the permanent seven-agent performance rule. Major autonomous events flow through one shared event spine rather than seven background scanners, and the new profiler instruments work that already happens instead of adding its own update loop.

### Robot-driven world story news

A bounded **World Story News** chronicle promotes important public events such as Champion changes, rare/shiny/legendary catches, tournament upsets and titles, character-arc breakthroughs, major relationship shifts and a publicly observed player Championship. Events are deduplicated and never mutate player story flags.

### Situation-specific robot dialogue

All seven robots now have distinct event reactions for blackouts, starter faints/evolutions, title wins/losses, player Championships, trades, grudges, mentorship, rare catches and tournament exits. Dialogue is generated from the event that already occurred, stored in a bounded per-robot history and never requires a new polling loop.

### Hall of Fame archive replay

The in-game **Hall Archive** reconstructs historical League crowns/defences and tournament finals from bounded public traces already stored by Champion Lineage and Tournament Director. It can show old title teams, finalists and decisive Pokémon/moves when those details were actually observable. Replays are textual historical reconstructions; Ultron never re-simulates an old battle or invents hidden moves/items. Tournament Director is now schema v5 so simulated finals can retain bounded public finalist snapshots and decisive traces.

### Performance profiler

The **Performance** view exposes measured whole-pulse cost, per-robot AI decision time, scheduler selection, path/travel cost and tournament-simulation cost. The same view now shows automatic FULL / CONSERVE / PROTECT scaling pressure, effective versus configured decision budget, deep-plan cadence, tactical-depth cap, tournament batch size and bounded mode history. Instrumentation remains attached to existing calls and creates no independent profiler loop.

The canonical unfinished roadmap is empty after this release. Its architectural, legitimacy, diversity and regression requirements remain permanent rules for future development.

## v2.33.0: miniature-AI goals, public scouting and earned tactical depth

Ultron now treats its long-term architecture explicitly as a **seven-agent miniature AI ecosystem**: up to seven autonomous robots should be able to plan, travel, battle, catch, trade, breed, scout, manage finite resources, learn and develop without turning the mod into a permanent CPU tax. New planners therefore reuse the existing four-agent decision budget, shared event streams, cached world data and bounded histories instead of adding seven always-on scans.

### Independent Pokedex projects

Each robot can maintain a bounded Pokédex project chosen from legal opportunities in the current game: regional completion, rare-species hunting, an existing Gen 2 breeding project, or an optional shiny hunt when legitimate shiny support exists. A shared encounter-ecology index is built in small slices and cached once per engine, so seven robots do not each rescan the world. Projects only create intentions. Actual catches, routes, Day-Care work, Poké Balls and encounter legality still pass through the existing autonomous systems.

### Physical public battle scouting

Robots can deliberately travel to observe a future opponent when public evidence says the trip is worthwhile. Only a bounded number of scouts may be active at once. Player scouting retains only information revealed by a battle the robot was physically present to observe, while same-map robot observers reuse the already-resolved duel event and the two lineups that actually fought. No hidden player party, robot PC, duplicate battle simulation or remote omniscience is used.

### Adaptive tactical growth without cheating

Robots now have save-specific tactical ceilings and authored flaws. Real battle experience can unlock deeper legal decisions such as safer pivots, setup disruption, revenge positioning and advanced PP-war plans, but it never changes stats, damage RNG, Pokémon ownership or item inventories. Personality remains visible at high skill: Robby and WALL-E will not deliberately sacrifice a bench partner, R2-D2 only learns patient PP-stall play at the highest tactical tier, and T-800 must learn enough restraint before using safer pivot logic. Separate Save DNA can shift a robot's ceiling slightly while remaining inside its authored cap.

The **Pokédex Goals**, **Public Scouting** and **Tactical Growth** views expose the new agent state, and Robot Debug includes the same bounded diagnostics. RobotMind is now **v12** with lazy migration/backfill.

## v2.32.0: nine tournament formats and competitive seasons

Ultron's standalone tournament director now supports **Single Elimination, Seeded Cup, Swiss, Round Robin, Double Elimination, Level 30/50 Cups, Type Cups, Rental Cups and Champion Invitationals**. The format picker lives under **ULTRON → TOURNAMENTS** and each format has bounded persistent state, Save-DNA-salted scheduling and readable in-game diagnostics. The World mod is still not required.

Level/type restrictions are enforced without permanent stat or party edits. Robots may use temporary tournament overlays assembled only from eligible Pokemon already in their active party, then real HP/status/PP are synchronized back to those Pokemon. Player teams are validated against the rule instead of silently altered. Rental Cups are AI-only exhibitions so Ultron never replaces the player's owned party with rentals.

Completed events also feed an eight-event **Competitive Season** with live rankings and bounded archives. Seasonal awards include **Season Champion, Cup Collector, Giant Killer and Iron Circuit**. After the eighth event, standings and awards are archived and the next season begins automatically.

## v2.31.0: unique save DNA, character arcs and Champion eras

Robots **never retire**. Instead, every robot has a permanent four-chapter character progression arc driven by real setbacks, recoveries, mentorship, bonds, tournaments and Champion-level experience. Each independently-created save receives persistent **Ultron Save DNA**, giving every robot save-specific arc timing/emphasis, RNG streams and modest legal team tastes so a new save does not simply replay the same personalities and team development.

Save DNA changes preferences among legal choices only. It does not alter Pokemon stats, damage RNG, encounter legality, move legality, story flags or ownership. Reloading the same save remains deterministic; intentionally copying a save also copies its timeline identity.

Champion Lineage now identifies significant reigns as named **Eras** and repeated dominant reigns as **Dynasties**, with the history exposed through Hall of Champions.

## v2.30.0: live risk, earned reputation and negotiated robot trades

- **Risk tolerance is now live behaviour rather than a descriptive personality number.** Each robot derives a bounded risk state from its authored profile, learning DNA, recent wins/losses, near-blackouts and remembered social pressure. That state changes healing thresholds, damaged-team major-battle readiness, voluntary challenge cadence and how much scarce healing/PP/cash stock the robot tries to preserve. Robby and Andrew naturally play safer; T-800 and R2-D2 accept thinner margins; repeated failures can temper even an aggressive robot.
- Added a bounded **public reputation system** for both robots and the player. Reputations such as Champion Slayer, Giant Killer, Comeback Specialist, Collector, Breeder, Tournament Monster and Dynast are earned only from observed accomplishments. Dangerous player reputations modestly raise scouting caution and reduce reckless voluntary challenges; Thoughts and Robot Debug expose the evidence without hidden information.
- Expanded **robot-to-robot trade negotiation**. Robots now score legal exchanges for duplicate/expendable stock, missing Pokédex entries, team-fit gaps, new type coverage, trade-evolution opportunities, trust and each robot's negotiation personality. A permanent trade still occurs only when both sides independently accept the exchange under the existing TradeTrust valuation. Failed proposals and completed deals are bounded and diagnosable.
- Added dedicated negotiation profiles for **Robby, T-800 and Andrew**, instead of letting them inherit Ultron's generic trade profile.
- RobotMind is now **v9** with lazy migration for riskTolerance, reputation and tradeNegotiation. The three completed roadmap items were removed from the unfinished-only roadmap after their deterministic audits passed.


## v2.29.0: remembered battles, social arcs and earned team identities

- Added bounded **salient battle memory**: recurring species behind repeated defeats, low-margin clutch partners, major tournament/League memories and opponent streaks can now be retained and surfaced in Thoughts, Current Plan and Robot Debug.
- Added **Relationship Evolution** on top of the existing relationship network. Repeated battles, cooperation, trades, championship meetings, snubs and broken/returned loans can develop into Friend, Ally, Rival, Respected Rival, Friendly Rival, Grudge or Nemesis arcs. These arcs modestly alter voluntary challenge frequency without forcing battles or changing stats.
- Added persistent **Dynamic Team Identity**. Repeated legitimate success can crystallise into Weather, Bulky Control, Status Control, Speed Offence, Break Pressure or Partner Core identities, which only add a modest tie-breaking preference when selecting from Pokemon the robot already owns.
- RobotMind is now **v8**. All three structures lazy-backfill old saves, retain bounded histories, expose readable diagnostics and have deterministic audits.
- The remaining expansion ideas are now stored in `docs/ROBOT_IMPROVEMENT_ROADMAP.md`; completed items are removed from that living list as required by the roadmap maintenance rule.

## v2.28.0: transparent plans, robot legacies and competitive history

- **Current Plan** UI/debug views expose a robot's ultimate objective, active step, progress, confidence, main concern, contingency/rewrite reason and bounded legal evidence.
- Seven persistent **career/philosophy** tracks give Ultron, Data, R2-D2, WALL-E, Robby, T-800 and Andrew distinct long-term identities earned through real play.
- Standalone tournaments now remember **robot rivalries, finals, title streaks and dynasties**.
- **Counter-meta evolution** learns only from observed/shared opponent archetypes and modestly influences legal roster selection without stat boosts or fabricated resources.
- Same-map **robot mentorship** shares planning lessons, never Pokemon, levels, money, items or hidden information.
- The **Hall of Champions** combines League lineage and tournament history into a readable competitive record.
- All new state is bounded, migrates lazily from old saves, exposes diagnostics and is covered by deterministic regression audits.

## v2.27.0: standalone tournaments, Champion lineage and seven-robot roster

Ultron now owns its tournament system. **The World is not required** to create or run a tournament: Ultron builds persistent brackets from **3 to 100 entrants**, seeds the player, active robots and legitimate trainer parties from the loaded game, handles non-power-of-two byes, simulates off-screen matches, preserves robot/guest HP and PP between rounds, launches the player's rounds as real trainer battles, records eliminations/winners once, and keeps the existing round-aware resource-conservation intelligence. External tournament APIs are compatibility fallbacks only.

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
