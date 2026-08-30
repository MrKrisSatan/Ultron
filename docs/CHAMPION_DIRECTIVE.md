# Ultron 3.0 Champion Directive

The Champion Directive is the single campaign layer above Ultron's existing autonomous systems. It asks what blocks the robot's current Championship milestone, builds a bounded sequence of legitimate intentions, and reuses existing subsystems to execute them.

## Campaign hierarchy

Every live plan exposes five nodes:

1. **Ultimate** — become Champion, reclaim the Championship, or defend/develop the reign.
2. **Strategic** — next Gym Badge, Pokémon League, or post-Champion program.
3. **Tactical** — the active generated mission.
4. **Immediate** — the next physical/legal action.
5. **Blocker** — the observed reason the strategic target is not yet complete.

The tree is capped at 12 nodes, though the standard view uses five. Reassessment occurs on selected planning slices and meaningful dirty-state changes, never in a new per-frame loop.

## Progress Pressure

Pressure is bounded from 0–100 and rises across planning cycles without meaningful progress. Badge wins, useful catches, evolutions, League/Champion progress and completed missions reduce it. Bands are CALM, WATCHFUL, RESTLESS, ADVANCE and DIRECTIVE.

Personality affects growth and detour tolerance, not the ultimate destination. T-800 escalates fastest; WALL-E escalates slowest. At DIRECTIVE pressure, optional or stale work is replaced by a reachable forward campaign step. Familiarity pressure visibly decays as advancement pressure rises.

## Obligation classes

- **CAMPAIGN-CRITICAL:** required recovery, provisioning, next-Gym/League travel or a diagnosed correction.
- **USEFUL:** preparation or acquisition that materially supports the campaign.
- **OPTIONAL:** tournaments, social activity or scouting that may be worthwhile while pressure permits.
- **STALE:** healed Centers/homes, obsolete training areas or resolved collection work.

## Generated missions

The generator can create Campaign Recovery, Dynamic Training Relocation, route Expeditions, Gym Preparation, Evolution Projects, TM Acquisition, Counter Hunts, Cash Recovery and League Provisioning. Champions generate persistent endgame missions for defence preparation, collection, competitive breeding, trusted-partner development or reserve readiness.

Missions are private robot intentions. They cannot grant resources, alter player state, set story flags, resolve encounters or move a robot. They select only objectives/destinations already supported by the legal AI executor.

## Failure and recovery

Gym, League, Champion and blackout failures record a bounded postmortem: failure target, diagnosed cause, evidence count, prescription and strategic resume target. Blackout creates a temporary recovery mission. When the team is healthy, the recovery leaf is discarded and the preserved strategic campaign resumes immediately.

## Dynamic training geography

The directive consumes the shared anti-grind ecology. A route with wild Pokémon four or more levels below the relevant team becomes stale for ordinary training/catching. The mission redirects to stronger reachable ecology or the next campaign route. A live completionist acquisition may temporarily override the training penalty; resolving that local target removes the exemption.

## Debug and persistence

Robot Debug shows all five hierarchy levels, ADVANCE/EXPLORE/COLLECT/FAMILIARITY pressures, activity class, postmortem, campaign statistics and latest reasoning trace. Campaign history is capped at 32, trace at 24, mission history at 24 and tree at 12.
