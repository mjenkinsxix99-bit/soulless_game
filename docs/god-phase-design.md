# Soulless — God Phase & World Phase Design Notes

> Living design doc. **LOCKED** = agreed, don't relitigate without cause.
> **OPEN / PARKED** = still spitballing or deliberately deferred. Nothing here is implemented yet.
> Two-phase build: **Phase 1 = the gods & their fights/powers** (ship first). **Phase 2 = the buildable world** (bigger, later).

---

## LOCKED — The Throughline (artistic direction)

The entity is **soulless because it was destroyed** — the gods took its world, its
worshippers, and its body, leaving only ether in the void. Everything in the game is
**clawing back what was stolen**:

- Souls consumed → grow stronger, develop **form**, take flesh, **mold that flesh into what it wants** (existing ascension/form system).
- Minions → an army of enemies turned to its cause.
- Heroes → defeated to take their power, rungs on the ladder.
- Gods → the *target*. Kill them, take their power, use it to rebuild what was lost.
- ...only to **become the thing it hated**: a destroyer of worlds, on a loop.

**Key reframe:** "Soulless" is ironic — the entity is the game's greatest **soul-hoarder**,
having swallowed every soul it ever killed. The final act is **letting the hoard out**:
creation = disbursing stored souls as living worshippers. *Everything you ate becomes
everyone you make.* Then you raze them — that's the horror, and the whole grind earns it.

**The "shaping" motif (design spine):** the entity *shapes* at two scales — **6 forms**
(molding its own flesh, existing system) mirrored by **6 blended societies** (molding its
people's culture, §Covenants). Same verb, bookending the game.

---

## LOCKED — The Convergence (every currency cashes out in the World)

The World is the sink that finally consumes the **entire** economy. Nothing orphaned:

| Currency | Becomes | Role |
|---|---|---|
| **Souls** | Life itself | Spend the hoard to breathe Claykin into being (Clay + Souls = life). |
| **Tattered Souls** | The substrate | Land, soil, the dead you build *on*. |
| **Burning Souls** | Divine spark **+ the upgrade currency for hero AND god powers** | Fuel for miracles/creation events; also what you spend to level powers on the map. |
| **Minions** | The first servants | Turned army = labor/angels tier; also produce base elements & channel counters. |
| **Elements → Compounds** | God-shield counters (Phase 1) **and** world materials (Phase 2) | See Element Mixing. |
| **God Souls** | The world seed | Pick **3** at world creation to shape terrain/events (boon+bane each). |
| **The Faithful** | The world's output | Claykin converted by the Revenants (sword / piety / education). |
| **Faithful Souls** | The prestige crux (was "Divinity") | **Produced by the Faithful at Transcend**; makes each re-run faster *and* deeper. |

---

## LOCKED — Three-Act Structure

1. **Act I — The Pantheon:** defeat the 13 gods. Challenging but **not a slog**. Each yields a power + its God Soul.
2. **Act II — Genesis:** defeat **NYX** (primordial night) → unlock the power to CREATE → World tab opens.
3. **Act III — The Cycle:** build a world → run it → **raze it** for Faithful Souls → rebuild differently. Replay is the point.

Prestige nesting: existing **Ascension → Reincarnation**, plus new **Transcension** on top (placeholder name — the raze that claims Faithful Souls; also gates mixing depth, one tier per raze).

---

# PHASE 1 — THE GODS

## LOCKED — God fight model (two-phase, stockpile-gated)

- **Two-phase HP bar.** A **gold immortal shield** (made of the god's element) you cannot damage, then a **red mortal HP bar**.
- **The shield is a persistent pool you BURN the counter into (no minions assigned — dropped that).** Each shield = a fixed amount of its counter element/compound (e.g. "requires 500 Research"). You **pour your stocked counter into it**; the pool drops and **the reduction is PERMANENT** — never regenerates, **survives reincarnation**. At 0 the shield is **gone for good** → the mortal HP phase begins.
- **Mortal HP phase is retryable** — once the shield's paid, it stays paid; flee/fail the HP fight and you just retry it (no re-paying). *(Retires the old "shield resets if you flee" rule — that was for the abandoned channel model.)*
- **Two-fold gate:** combat build clears the HP; the right counter stock clears the shield. Miss either → wall.
- **Roster still gates it:** base elements come from Elite minions with fixed elements, so you need producers of the counter element. "Do I have the right element?" stays the strategy; the click-work is gone.
- Sequential (gold to zero, *then* red).

## LOCKED — The Counter Wheel (which element strips which shield)

Closed loop over the 10 elements — a **perfect permutation** (every element counters exactly one and is countered by exactly one):

- **5-cycle (Wu Xing destruction):** Wood breaks Earth · Earth dams Water · Water quenches Fire · Fire melts Metal · Metal chops Wood.
- **3-cycle (works):** Research carves Stone · Stone smothers Plant · Plant reclaims Research.
- **2-cycle (the pair):** Holy ↔ Dark.

Shield element → counter you channel: Earth←Wood · Water←Earth · Fire←Water · Metal←Fire · Wood←Metal · Stone←Research · Plant←Stone · Research←Plant · Holy←Dark · Dark←Holy.

**Shield complexity scales:** single (Stairway) → double → triple (the finale). **No element is rare** (10 minions each, one per realm); counters are deliberately **spread across all 10** so no single element is over-demanded (balance).

## LOCKED — Shields: the Stairway 5 (single base element each)

Single base element, common counter (no Holy/Dark — reserved for the Worlds). Burn amounts anchored to the 5,000 base cap; ramp is a teaching curve. Amounts are tunable placeholders.

| # | God | Shield | Burn (counter) | Amount | Logic |
|---|---|---|---|---|---|
| 1 | Morrigan | Water | Earth | **200** | Washer at the Ford — the blood-river; the earthen bank dams it |
| 2 | Durga | Stone | Research | **500** | Daughter of the mountain, immovable — out-*think* it, don't out-muscle it (the one abstract counter — foreshadows Holy/Dark) |
| 3 | Brahma | Plant | Stone | **800** | Born from the cosmic lotus — barren rock smothers the bloom *(alt: Research/Vedas → Plant)* |
| 4 | Thor | Metal | Fire | **1,200** | Mjölnir, dwarf-forged iron — the forge unmakes it |
| 5 | Isis | Wood | Metal | **1,800** | The Nile's green life — the sickle cuts the sacred green |

Counter sequence the player gathers: Earth → Research → Stone → Fire → Metal (five distinct — teaches farming a spread).

## LOCKED — Shields: the Worlds 8 (compound shields)

Pour **compounds** (permanent, so the pool persists). **Rule:** a compound strips every band whose counter-element it carries — so a dual-element compound cracks a double shield in *one* pour; a triple shield needs two compounds. Amounts TBD (climb from Hades up); compounds are all 2-element (tier-1) — **no triple/transcension-gated compound is ever a god counter** (would soft-lock).

| # | God | Shield | Counter(s) | Pour | Note |
|---|---|---|---|---|---|
| 6 | Hades | Earth | Wood | **Timber** `wood+plant` | gateway — gentlest |
| 7 | Amun-Ra | Fire | Water | **Mud** `water+earth` | drown the sun |
| 8 | Shiva | Fire + Dark | Water, Holy | **Holy Water** `water+holy` | quench flame, banish void — one compound, both bands |
| 9 | Sekhmet | Holy + Metal | Dark, Fire | **Hellfire** `dark+fire` | unmake the Eye's radiance, melt her claws |
| 10 | Athena | Research + Stone | Plant, Research | **Herbcraft** `plant+research` | the wild overruns her wisdom |
| 11 | Odin | Research + Water | Plant, Earth | **Loam** `plant+earth` | soil reclaims runes, dams the seas |
| 12 | Zeus | Metal + Fire + Holy | Fire, Water, Dark | **Steam** `fire+water` + **Hellfire** `fire+dark` | **fire constant**; Dark unmakes the king's divinity |
| 13 | NYX | Dark + Water | **Holy (Light)**, Earth | **Dawn** `holy+fire` + **Clay** `earth+stone` | **Light** floods primordial Night (callback to Amun-Ra's Light); Clay = the stuff of the Claykin to come |

**Finale mirror:** Zeus = a *Holy* shield unmade by *Dark*; Nyx = a *Dark* shield unmade by *Light*. Light and dark cross at the climax.

## LOCKED (pending testing) — Mortal HP, timer & signature twists

**Mechanic:** once the shield's paid, the god drops mortal and a **timed DPS check** starts (the Elite-check pattern, boss-sized). **Show only the god's HP — no DPS hint;** the player works it out. **Fail = HP resets, retry anytime** (the shield stays paid; the gate *is* the DPS threshold).

**Tuning principle:** set so **base DPS fails and spell-burst succeeds** — the god fights are the payoff for the whole spell system (Morrigan's nodes, Isis's rotation). Remember the player has stacked DPS boosts, elite-timer extensions, and spells (Twin Blades ×2, Twin Strikes ×2, Power-of-3 ×3, Flurry, crits, Invoke Power).

**Formula:** `God HP = EliteHP(refFloor) × 10` · **Timer = 3× the player's current elite timer** (inherits timer-minion bonuses). Anchor: the game's curve is ×1.166/floor past 130 with Elite ×10.6 at floor 1000 → **floor-1000 Elite HP ≈ 1.06e76**. The ×10 is the fairness knob (base clears ~3× an Elite over the 3×-long window → fails at ×10; ~10× burst clears it).

| # | God | Ref floor | HP ≈ |
|---|---|---|---|
| 1 | Morrigan | 1000 | 1e77 |
| 2 | Durga | 1010 | 5e77 |
| 3 | Brahma | 1020 | 2e78 |
| 4 | Thor | 1035 | 2e79 |
| 5 | Isis | 1050 | 2e80 |
| 6 | Hades | 1075 | 1e82 (gateway jump) |
| 7 | Amun-Ra | 1100 | 5e83 |
| 8 | Shiva | 1125 | 2e85 |
| 9 | Sekhmet | 1150 | 1e87 |
| 10 | Athena | 1180 | 1e89 |
| 11 | Odin | 1210 | 1e91 |
| 12 | Zeus | 1250 | 5e93 |
| 13 | NYX | 1300 | 1e97 |

**Pacing assumption:** the player climbs ~floor 1000 → 1300 across the god phase (a 10²⁰ spread, but it's the game's own steepness). Compress the ladder if the phase spans fewer floors, stretch if more. **Adjust after playtesting.**

**Signature twists** (bend only the timer or add regen — cheap):
- **Isis** — regenerates a sliver/sec: a soft DPS floor (resurrection).
- **Sekhmet** — shortened timer (bloodlust).
- **Odin** — lower HP, brutally short timer: a pure burst check (sacrifice — everything, *now*).
- **Nyx** — long timer, colossal HP: an endurance test ("the night is long").
- Everyone else standard; **Hades = the honest benchmark** ("welcome to the gods").

## LOCKED — UI placement (Phase 1)

- **Dominion** = new **right-side tab**, the god-power shop. Holds your **Blessings** (the god powers — seized, not bestowed). **Reveals when the god Stairway opens**; cards fill as gods fall (locked silhouettes until then). Cards mirror hero-power cards (BS cost · level · Buy) with sub-UIs where needed: **Hades** Feed-Souls button + running tally + DPS readout · **Isis** 10-slot drag-to-order rotation (spell picker per slot, repeats OK, spell 9 excluded) · **Athena / Thor** on-off toggles · **Nyx** one-time *Unlock Life* → opens the World tab. Header flourish: **the 7 days of creation lighting up** as Worlds gods fall.
- **Map entry stays unified:** Portal → Enter → overlay → forward/back (hero map / Stairway / Worlds). Dominion is the shop, not the door.
- **Mixing = the Theurgy modal** (LEFT side, alongside Sacrifice / Minions / Entity). Reveals at Brahma (#3). Layout + the full compound codex live in **`docs/theurgy-compounds.md`**: two sections — a flask bench on top (**always two input boxes** → `???` until discovered) and one periodic-table codex below, sectioned by tier (1 / 2 / 3 — nothing past 3), with **the 10 base elements as its first 10 pre-discovered cells**; click a cell to fill the first open flask, click again to remove. **Every recipe is a pair; tier = chain depth.** Tier 1 (the 45 elemental pairs) is the entire first run and Phase 1's whole scope; each **Transcension** (the raze) lets one more tier be dropped into a flask. *Kiln is reserved for Phase 2 — a World buildable where Claykin are fired into castes.*
- **The god encounter / pour screen** (not a tab): the gold shield bar, "requires X", a **Pour** button burning stock into the persistent pool, remaining amount; at zero → the mortal HP + timer fight. Slots into the existing hero-encounter flow (pour + timed fight replaces "accept challenge").
- **Resulting bars:** right = Upgrades · Portal · Honors · Stats · **Dominion** (+ World later); left = Sacrifice · Minions · Entity · **Alchemy/Theurgy**.

## LOCKED — Element Mixing (the tie-in that makes it load-bearing)

**Unlocks mid-phase, at the stairway→worlds-zone gate** (after god #6) — because that's exactly when it becomes required. Base elements are minion-produced, **capped at 5,000** (raised from 2400 to give the new sinks room; the Portal still requires 2400 — split `ELEMENT_CAP=5000` from `PORTAL_REQ=2400`), and **wipe every reincarnation**. **Compounds are uncapped and permanent.** Mixing **transmutes ephemeral base elements into PERMANENT compounds** — the machine that makes farming last. Compounds do three jobs:

1. **God-shield ammunition (Phase 1) — hard gate:** the **5 Stairway gods are stripped by base elements; the 8 Worlds gods (Hades + the 7 creation days) ONLY by compounds.** Base elements go inert at the map boundary (Hades = the first, gentlest compound fight), forcing full mixing engagement mid-phase. Compounds counter *two* bands at once when they carry both counter-elements (e.g. **Holy Water** `water+holy` strips both of Shiva's bands). All god-counter compounds are 2-element (tier-1) — triple/transcension-gated compounds are never counters.
2. **Economy engine:** spend a compound to **boost production of the elements/compounds below it on the tree** (the fine-tuning dial).
3. **World material (Phase 2):** the same hoard is what you build the world (and Claykin) from. Destroyer's tools become creator's tools.

**Discovery:** each discovered compound stays **known in the codex forever** (survives all resets); each discovery → a small permanent **base-element production speedup**. (No compound-production bonus — production automation is a god power, see Thor.)

**Recipe tree (LOCKED shape):** **every recipe is a pair — `A + B = ??`**; depth comes from chaining a compound as an ingredient, never from more boxes. **Tier = chain depth** (Tier 1 = element + element, the 45; Tier 2 = Tier-1 + element; …), topping out at **Tier 3** (115 cells, tapered 45/40/30 — nothing deeper; Wonders are Phase-2 World buildables, Life is the Nyx unlock). **Tier 2+ recipes are unhinted — a deliberate puzzle.** **Gated one tier per Transcension** (the raze): the whole first run — god phase and world 1 — is Tier 1 only; each raze lets one more tier be dropped into a flask, so each successive world is built from deeper materials. Full codex in `docs/theurgy-compounds.md`. Optional **Yggdrasil-tree** visual — presentation only, undecided.

**Unlock timing:** **Brahma (#3)** unlocks the mixing system (the Creator's gift; levels grant auto-mixing); it becomes **mandatory at #6** (Hades — the Worlds gateway is the first compound fight). Gods #4–5 (Thor, Isis) are base-element practice with mixing available. (Odin at #11 gives the compound-yield *perk*.)

**Body vs soul split:** the **7 physical elements** build the world's *body* (terrain, materials, Claykin flesh); the **3 abstract elements — Holy, Dark, Research** — define its *soul* (the Covenant axes, below).

**Mixing powers (LOCKED):** Brahma (#3) unlocks mixing + auto-mixing; Odin (#11) gives the compound-yield perk (Spoils scale).

## LOCKED — God Powers (de-duplicated; upgraded with Burning Souls)

Full audit confirmed the **multiplier economy is saturated** (DPS/click/souls/TS/crit/mana/cost all touched by 3–11 sources), so every god power sits on **whitespace** (zero/single-source levers) — automation, meta, or new-system, never a plain multiplier. **God powers upgrade with Burning Souls, same as hero powers** (no new currency layer). **God Souls are reserved for the 3-pick world seed.**

**Power-unlock ORDER** (this reorders the gods; accept two lore bends — Odin early, Athena late):

**FINAL board (LOCKED)** — split across two maps: **Stairway (5, base-element shields)** and **The Worlds (8, compound shields; Death → Creation → Life)**.

| # | God | Power (magnitude) | Map / Beat |
|---|---|---|---|
| 1 | Morrigan | Auto-buy spell nodes — 9 levels (one per spell node) | Stairway |
| 2 | Durga | Flurry rate — +1 slash/sec per level, max 7 | Stairway |
| 3 | Brahma | **Unlock the mixing tree**; levels grant auto-mixing (the Creator's gift) | Stairway |
| 4 | Thor | Auto-buy the sacrifice (tattered) grid — 20 levels, each pass buys affordable nodes in order | Stairway |
| 5 | Isis | Spell auto-cast — **10-slot rotation** (levels unlock slots), accepts repeats (queue Power-of-3), **spell 9 excluded**, drag-to-order UI | Stairway |
| 6 | **Hades** | **Feed-Souls Bank** — 1:1 button; TS fed give **7.77% DPS** each (vs 6.66% unspent) | Worlds — *gateway, no beat* |
| 7 | Amun-Ra | Offline earnings — +2h & +5% eff./level, max 9 → **24h @ 95%** | Worlds — **Light** |
| 8 | Shiva | Retain **10% of souls** through reincarnation | Worlds — **Air** |
| 9 | Sekhmet | **×Minion XP** — Glory-in-Sacrifice scale (+0.25/lvl) | Worlds — **Land** |
| 10 | Athena | Auto-buy hero powers — **Heracles + Soul Catcher** (for now) | Worlds — **Growing things** |
| 11 | Odin | Compound-yield perk — Spoils-of-War scale | Worlds — **Waters** |
| 12 | Zeus | **×1.10/level (unlimited)** on Heracles, Soul Catcher, Spoils of War, Glory in Sacrifice; Spoils cost scale | Worlds — **Animals** |
| 13 | NYX | Unlock **Life** (the World tab) | Worlds — **Breath of Life** |

**Hades as the Worlds gateway:** the lord of the dead guards the threshold — you pass through Death to reach Creation, and the soul-keeper unlocks the Soul Bank as you enter (you're about to spend souls on *life*). No creation beat (none of the 7 days fit death). Unlike every other god (who *teaches* a new power), Hades simply *helps* — he alone knows the entity's grief. Makes Map 2 read as a cosmogony: **Death → the 7 days → Life.**

Placeholder greeting (Hades): *"You are already familiar with death and loss — I have nothing to teach you. But I will help you. Bolster your strength in my soul bank."*

**Deity placement:** deities sit where lore + creation fit best (powers move with them). Amun-Ra → #7 (sun = "Light", "labors in your absence" = offline); Durga → #2 (Flurry, fine early); Brahma → #3 (the Creator unlocks mixing); Hades → #6 (Worlds gateway); Odin → #11 ("Waters" — seas from Ymir's blood). Accepted lore bends: Durga early, Amun-Ra into the hard zone, Brahma early.

Cut for redundancy along the way: crit, click damage, enemy-HP reduction, overkill-chaining, elite-*timer* extension, auto-buy base upgrades, auto-collect urns, auto-mark-for-immolation (all already covered by tattered grid / minions / SMART Clickers / Jason).

### Creation story — final 7 (placeholder post-defeat flavor)
Each of the final 7 enacts a day of creation, culminating in Life at Nyx:
- **Amun-Ra** — "You have caused **Light** to be formed."
- **Shiva** — "You have caused the **Air** to form."
- **Sekhmet** — "You have gathered the **Land**."
- **Athena** — "You have caused the land to sprout **growing things**."
- **Odin** — "You have caused the **Waters** to populate."
- **Zeus** — "The **Animals** have gathered upon the land."
- **NYX** — "The **Breath of Life** has been gained."

---

# PHASE 2 — THE WORLD

## LOCKED — The World board (big, pannable, fogged)

- **A WORLD — big.** The map pans and zooms; tiles sized as needed. (Revises the earlier "fixed, on-screen" call — that was a skill-budget worry; pan/zoom on canvas is a camera transform + drawing only what's in view.) Size TBD. Iso hex sprites, draw back-to-front, hex hit-detection.
- **Procedurally seeded by the 3 chosen God Souls:** each soul carries **terrain weights**, a **guaranteed minimum** of its key tile, and a **bane** (its calamity). Base weights → apply the 3 souls → roll → **guarantee pass** (Origin is Grassland, center ring claimable, every soul's key-tile minimum met, enough food/wood/stone reachable that the world can't be born unwinnable).
- **Fog of war, lit by campfires.** *Explored = campfire-lit* = accessible and buildable. A campfire lights **radius 2**; a new one may be placed on any lit tile **or one tile into the fog**; campfires are **permanent** (no relighting); **cost doubles per campfire (×2).** The **Origin** starts with the first fire.
- **Save-safe:** flat int arrays (terrain / structure / lit) per hex.

**The tile set (11):**
| Tile | Rule |
|---|---|
| Grassland | buildable/farmable; **foragable** |
| Forest | wood — **needs tools**; bootstrap: bundled foraged grass counts as wood |
| Mountain | **mine it for ore** *or* **terraform it away** |
| Coast | fish, water |
| Deep Water | barrier |
| Lava | threat + barrier → **Obsidian ground** once cooled (Firewalkers + water, fetched from Coast or supplicated) |
| Desert | near-nothing; **irrigable only within 2 tiles of water** → Grassland |
| Marsh | herbs; **foragable** |
| Blight | **not impassable, but kills Claykin over time**; **static — never purified, worked around** |
| Hallowed Ground | a tile **consecrated by the Revenants** (see Hallowed Ground below); **required under every Revenant-only building** |
| Origin | the center; starts with a fire |

## LOCKED — Tiles, jobs & the Claykin (the working model)

- **Claykin are never seen** — a count, no walking, no pathfinding, **no distance penalty.**
- **The player designates what a tile *is*** (housing, farming, woodcutting, mining…) by placing buildings on it. Each building has its own **count-per-tile or team cap** (see the Buildings section). A purpose is available by **what the tile is and what it touches** (woodcutting on/adjacent to Forest, mining on/adjacent to Mountain, fishing beside Coast with fish, a Forge beside Lava, farming on Grassland).
- **A resource tile commits to ONE product** as the tech tree branches — rock *or* gold ore, wheat *or* grapes. Never both.
- **Jobs are +/− buttons.** Idle Claykin (born idle into housing) are assigned to any slot on an **explored** tile; reassign at will. **XP is a per-job record on the Claykin** (chopping XP waits while it farms; farming starts at 0). **A level-50 farmer is a level-0 fighter** — only the level in the target job counts.
- **Resources are stockpiled** (food, lumber, stone, iron, gold, algastone, fish, herbs, holy…) in the Barn / Granary / Warehouse (and Docks); a food system to develop.
- **Two ledgers, one name.** What the Claykin dig, chop, farm, fish, or produce is **theirs** (world materials, in their stores). What sits in the Theurgy codex is **the deity's** and does not exist in the world until **gifted**. Iron, gold, holy, axe: the same word can live on both ledgers; **gifting is the only bridge.** Supplication fires only when the Claykin lack something a job needs.
- **Building is a fill, not a purchase.** A placed building's material cost is *placed* over time by Bolders (wood) and Masons (stone) at their placement rate; **build time = cost ÷ rate.** The player can queue any number of buildings; crews build in placement order, and when stock runs dry the queue stalls until the player supplicates or production catches up.
- **Terraforming is Claykin work, never a god action.** Workers do it; materials they lack are asked for via **supplication**.
- **Two channels for materials from the deity, both timed:** **Gifting** (proactive, short cooldown) and **Supplication** (reactive — fires on its own timer when a marked building lacks materials: *"The woodcutter Claykin humbly request X wood to complete their building. Grant or deny."*). Set the gift cooldown a little **longer** than the supplication trigger so supplication is the normal channel. **Supplications ≠ Edicts** (edicts = society-level choices).
- **Penalties:** hazard adjacency (a tile next to Lava/Blight) and **random calamities that kill Claykin — these are the God Souls' banes.** That's the whole penalty layer.

**The jobs (LOCKED). Two material streams:** Claykin jobs produce **mortal goods** (food, wood, stone, ore, fish, herbs) to the stockpile; the deity supplies **divine compounds** (the Theurgy table) by gift or supplication. Buildings consume a mix.

*Greenware jobs (any unfired Claykin) — team cap is set by the workplace (see Buildings):*
| Job | Workplace · cap | Does | Fires into (at level 20) |
|---|---|---|---|
| Chopper | Chopper Camp · 6 | wood (needs an axe) | — |
| Farmer | Farm · 6 | **Ambrosia** — the one crop; the tech tree branches what it becomes (food, fibre, brew, paper, soil, fuel) | — |
| Herbalist | Hearthstone · 3 | food, herbs, **holy** | **Shaman** |
| Stalker | Lodge · 2 | hunts | — |
| Digger | X Mine · 3 | stone / iron / silver / gold / coal / algastone — **one mineral per mine** | **Firewalker** |
| Angler | Angler's Hut · 2 | fish (adjacent water with fish) | **Mariner** |
| Bolder | Bolder's Cabin · 3 | **builder — required for every building** (even stone has a wood frame); places 5 material/sec base | **Mason** |
| Learner | Study · 3 | **gathers Tech**; no XP bonus; superseded by Teachers once Schooling is learned | **Teacher** |
| Maker | Maker's Lodge · 3 | crafting hands — tools, goods, the Ship (not buildings) | — |
| Fighter | Fighter Camp · 3 | **War Power** | **Warden** |

**Ambrosia is the only crop.** The First Farm is a gift; the Claykin take it from there. Ambrosia's branches all land on codex names: Grain → Bread · Rope → Cloth → Silk · Ale → Spirits · Pulp → Paper → Vellum → Book · Compost → Farmland · Oil. Farmed Ambrosia is world-side; the codex versions are the deity's.

**The tech engine — supplication grows the tree.** *Supplication → gift → study → craft.* ("The Claykin see trees but cannot harvest the wood. They request something sharp to cut." → gift an Axe → Learners study it → Makers learn to craft more.) Not everything comes from the Claykin; the mystery gift is the crux of the tech tree. **The Tech Tome:** part of the Transcension ritual — logs the Claykin's works and passes to the next generation; what's learned is *known* next world and only needs unlocking, not rediscovery.

**PARKED — a hostile world (lean form):** other races may attack, or need conquering and converting (Wardens fight; Mariners ferry Wardens and Stalkers). **Not rendered on the map** — a **randomly seeded direction** that they exist, discovered by expanding that way. Abstract unless procedural generation can place them convincingly. Spec later.

## LOCKED — The Claykin (the created life)

- **Claykin = Clay + Souls.** Clay (a compound) is the body; Souls (the hoard) are the life — closing the convergence loop ("Souls → life").
- **Belief/happiness = the integrity of the clay:** content = fired & whole; neglected = dry, **crack, crumble to dust** (population loss). Heresy is literal breakage.
- **The raze = "return to dust":** Claykin crumble back to clay and you **reclaim their souls as Faithful Souls**. *"From clay I formed you; to clay you return."* The reset is an **un-forming**, not a delete.
- Pottery is **transformation, not leveling** (see Castes).

## LOCKED — Castes (transformation = consecration, not upgrade)

Base **greenware** Claykin do the primal work. **Firing in the Kiln** transforms a greenware into a **specialist** — **caste-only work, permanent, cannot take another job** (removed from the idle pool: a real commitment).

**The Kiln.** The first **2nd-tier building** (buildings have **tiers and footprints**); a **triangular prism spanning 3 tiles**, **one per world**, tech-tree unlock, built from Clay + Charcoal. **Fire and glaze as many Claykin as you want** — a small pool at first, a significant one by world 3. The only place a Claykin can be fired. **The deity is the potter** — firing and glazing are **god-clicks** (shaping the clay is the one act that's the deity's by nature; the Claykin terraform and build). Both open once the Claykin discover and build the Kiln. **No potter job, no cracking.**

**The level-20 ladder (LOCKED).** *Time in the work is the price, not materials.* A greenware Claykin must reach **level 20 in the precursor job** to be fired into its caste, and a caste Claykin must reach **level 20 in the caste** to be glazed into its Revenant. **Per-job XP, hard gate** — a level-50 farmer is a level-0 fighter. The **firing compound stays, at a flat cost** (no escalation; the player pays in time). **Glazing escalates: ×1.15 per glaze.**

| Precursor (lvl 20) | → Caste | Fired with | Workplace · cap | Job |
|---|---|---|---|---|
| Bolder | **Mason** | Masonry | Stoneworks · 3 | places **stone** (same rate/bonus as Bolders); heavy terraform (removing a Mountain) |
| Digger | **Firewalker** | Obsidian | Forge · 2 (adj. Lava) | works Lava (cooling → Obsidian ground); **makes obsidian** at the Forge |
| Angler | **Mariner** | Timber | Dock · 6; 2 per Ship, **3 ships berth per Dock**, 1 ship per water tile when out | deep-water fishing, **trade**, ferrying troops / missionaries / trade goods |
| Fighter | **Warden** | Axe | Outpost · 3 / Barracks · 6 | **defense and offense**; War Power |
| Herbalist | **Shaman** | Lotus | Spirit Lodge · 6 | rites; produces **holy** (**no** blight purifying — Blight is static) |
| Learner | **Teacher** | Scripture | School · 3 / College · 6 | the Tech source once Schooling is learned; XP boost |

**Glazing IS the Revelation.** The three Covenant castes can be glazed with their axis compound into the god-voice: **Warden + Hellfire → Cleric** (Dark) · **Shaman + Holy Water → Priest** (Holy) · **Teacher + Scripture → Scrivener** (Wisdom). **One caste-line glazed per world; glaze as many of that caste as you want** (×1.15 per glaze). The pottery ladder: **greenware → fired (caste) → glazed (Revenant).** The full chains: Fighter → Warden → Cleric · Herbalist → Shaman → Priest · Learner → Teacher → Scrivener. At the Revelation the player answers two questions: **"Which caste is closest to you in this world?"** (holy / dark / wisdom → the **Chosen**, glazed, bonus) and **"Which caste is the farthest from you?"** (of the two remaining → the **Reviled**, negative). The last one left is **supporting** (neutral).

Compounds forge castes → **mixing (Phase 1) feeds society (Phase 2).** Same system, three jobs (shields → economy → castes).

## LOCKED — The Revenants: the push forward

**The Faithful, not Faith, is the prestige.** (There is **no "Faith" resource** — nixed. The Claykin's holy output is the world material **Holy**.) The Revenants *spread faith* = **convert Claykin into the Faithful**, and **the Faithful produce Faithful Souls at Transcend.** Each Revenant converts a different way. All three hubs are **9-tile buildings on Hallowed Ground**; one per world in practice — **hubs have no price ratio**; instead each grants **×1.10 to its Power per 10 Revenants stationed in the hub** (only the hub counts).

**Three Powers, one per axis:** **War Power** (Fighters + Wardens + Clerics; enables **raiding parties**) · **Holy Power** (Cathedral) · **Tech Power** (Laboratory). Each rung of a line contributes its own weight; the hub multiplies.

| Revenant | Hub | Power | Spreads faith by | Pushes | If Reviled |
|---|---|---|---|---|---|
| **Cleric** (Warden + Hellfire) | **Citadel** | War | **the sword** | territory & survival — but **no cheaper campfires; spreading has a cost** | calamities hit harder, threats spread |
| **Priest** (Shaman + Holy Water) | **Cathedral** | Holy | **piety** | boosts the *spread* of faith; produces **holy**; consecrates ground | Faithful grow slowly, Belief fragile |
| **Scrivener** (Teacher + Scripture) | **Laboratory** | Tech | **education** | tech & skill — research speed, XP, yields | the tree crawls |

The supporting caste does its job — no bonus, no penalty. **Ships serve the Covenant:** troops, missionaries, and trade goods are *all* always available; the Covenant only tilts them (Revenant boosted + extra buildings · supporting normal · Reviled disadvantaged).

## LOCKED — Hallowed Ground (consecration)

**Hallowed Ground is a tile state.** Each Revenant consecrates with its own compound, and all three produce the same state:
- **Clerics** — **Dawn** (Holy + Fire)
- **Priests** — **Hallowed Earth** (Holy + Earth) — *the compound was renamed from "Hallowed Ground" to avoid the collision*
- **Scriveners** — **Scripture** (Holy + Research)

**Any building available only to the Revenant caste must be built on Hallowed Ground** — the three hubs and any unique Revenant buildings. A 9-tile hub means 9 consecrated tiles first: **a deliberate material sink.** Ordinary buildings never need it.

## LOCKED — Buildings (the world 1 set)

**Price ratio = growth per unit owned, counted on the total owned across all tiles** (never resets per tile): `cost = base × ratio^(N−1)`. **Base costs are deferred** until the material list. Steep ratios (Shack 2.5, Barn 1.75) are steep because of the *material bill*, not to punish. Bonuses fire **only on a full team**. Footprints are on the record only where stated (1-tile, 3-tile, 9-tile); everything else is a count-per-tile or a team cap, not a size.

**Housing**
| Building | Per tile | Claykin each | Ratio |
|---|---|---|---|
| Shack | 6 | 1 | 2.5 |
| Cabin | 4 | 1 | 1.15 |
| Cottage | 4 | 2 | 1.15 |

**Storage** — each type lives on **one tile for all of them** and **upgrades** (ratio per upgrade level). Lumber and stockpile fold into these; Docks also add storage. *What each holds: TBD with the material list.*
| Building | Ratio |
|---|---|
| Barn | 1.75 |
| Granary | 1.15 |
| Warehouse | 1.15 |

**Tech** — 1 tile each, upgraded indefinitely by ratio; both workplace and multiplier.
| Building | Ratio | Holds | Effect |
|---|---|---|---|
| Library | 1.15 | — | Tech multiplier (Learners/Teachers/Scriveners are the source) |
| School | 1.15 | Teachers 3 | Tech accumulation bonus |
| College | 1.10 | Teachers 6 | Tech accumulation bonus |

**Greenware workplaces** — ratio 1.15; team cap; full-team bonus in brackets.
| Building | Team | Bonus | Notes |
|---|---|---|---|
| Chopper Camp | Choppers 6 | ×1.15 | on/adjacent Forest |
| Farm | Farmers 6 | ×1.15 | one Farm per tile; Ambrosia |
| Lodge | Stalkers 2 | ×1.10 | hunting returns |
| X Mine | Diggers 3 | ×1.15 | X = stone / iron / silver / gold / coal / algastone (more later); **Quarry tech upgrades mines** |
| Angler's Hut | Anglers 2 | ×1.10 | adjacent water tile with fish |
| Maker's Lodge | Makers 3 | ×1.15 | output |
| Study | Learners 3 | — | the bonus lives in the Tech buildings |
| Bolder's Cabin | Bolders 3 | ×1.15 to placement rate | **required for any building**; 5 material/sec base (before XP) |
| Hearthstone | Herbalists 3 | — | food, herbs, holy |
| Fighter Camp | Fighters 3 | — | War Power |

**Caste workplaces** — ratio 1.15.
| Building | Team | Bonus | Notes |
|---|---|---|---|
| Stoneworks | Masons 3 | ×1.15 to placement rate | same placement mechanic as Bolders, for stone |
| Forge | Firewalkers 2 | ×1.10 output | adjacent Lava; makes obsidian |
| Dock | Mariners 6 | — | adds storage; berths 3 Ships |
| Outpost | Wardens 3 | — | |
| Barracks | Wardens 6 | — | |
| Spirit Lodge | Shamans 6 | — | holy |

**Revenant hubs** — 9 tiles, Hallowed Ground, no ratio, ×1.10 Power per 10 stationed.
| Hub | Holds | Power |
|---|---|---|
| Citadel | Clerics | War |
| Cathedral | Priests | Holy (also produces holy) |
| Laboratory | Scriveners | Tech |

**Special**
| Item | Rule |
|---|---|
| Kiln | 3 tiles (triangular prism), **one per world**, Clay + Charcoal; tech-tree unlock |
| Campfire | lights radius 2; placed on a lit tile or one into fog; permanent; **cost ×2 each**; the *second* campfire is a tech (Campfire node) |
| Ship | built at a Dock (likely a Maker craftable, ratio TBD); crew 2 Mariners, must be full to sail; 3 berth per Dock, 1 per water tile when out; payload = troops / missionaries / trade goods |

*No further buildings for now — unique Revenant buildings beyond the hubs are deferred.*

## LOCKED (pending play) — The Tech Tree (Science tree)

Modelled on Kittens Game's science tree, trimmed to our ceiling (Tier 3 materials — no space, no time travel) and renamed. **Two trees, maybe a third later:** this one (unlocks buildings, jobs, castes) and the **Workshop tree** (what Makers can craft — *not* flat job multipliers; TBD). **Gifts open a domain; tech extends it.** Everything requires **Omens** (learning to learn). Some ordering will only settle in play.

**Wave 0 — gifts:** The First Bonfire · The First Farm (Ambrosia) · The Hammer (Tools: the Claykin shape the Axe and Pick themselves)

**Wave 1 — survival**
- **Omens** — root. Study, Learners. A **countdown to the next Calamity** (later techs refine *what* is coming; no seasons).
- **Agriculture** — First Farm. Farm, Farmers, Barn.
- **Tools** — Hammer. Axe and Pick. Chopper Camp, Maker's Lodge.
- **Campfire** — Bonfire. The second campfire; expansion begins.
- **Rites** — Agriculture. Hearthstone, Herbalists; holy trickles.

**Wave 2 — industry**
- **Hunting** — Agriculture. Lodge, Stalkers.
- **Mining** — Tools. X Mine (stone), Diggers.
- **Carpentry** — Tools + Agriculture. Bolder's Cabin, Cabin, Warehouse.
- **Charcoal** — Campfire + Tools. Makers burn wood to Charcoal.
- **Edicts** — Omens + Agriculture. The commandments layer opens.

**Wave 3 — the Kiln**
- **Kilncraft** — Charcoal + Mining. **The Kiln; firing begins. The choke point — every caste hangs off it.**
- **Fishing** — Carpentry. Angler's Hut.
- **Warcraft** — Hunting + Tools. Fighter Camp, Fighters.
- **Scripture** — Edicts. Paper branch, Library. The law written down.
- **Ironwork** — Mining + Kilncraft. Iron mine; better Axe and Pick.

**Wave 4 — castes**
- **Stonework** — Kilncraft + Carpentry. Stoneworks, Masons, Granary.
- **Shamanism** — Kilncraft + Rites. Spirit Lodge, Shamans.
- **Garrison** — Kilncraft + Warcraft + Stonework. Outpost, Barracks, Wardens.
- **Seafaring** — Kilncraft + Fishing + Carpentry. Dock, Ships, Mariners.
- **Firewalking** — Kilncraft + Ironwork. Forge, Firewalkers, obsidian.
- **Schooling** — Kilncraft + Scripture. School; **Teachers supersede Learners.**
- **Trade** — Edicts + Carpentry. Trade-goods payload.
- **Brewing** — Agriculture + Kilncraft + Edicts. **Ale raises Belief** (the one consumable Belief lever); Spirits = Tier 3 version and premium trade good. Kept small.

**Wave 5 — the world matures**
- **Masonry** — Stonework + Schooling. Cottage, College.
- **Quarrying** — Stonework + Ironwork. Quarry upgrades mines.
- **Alchemy** — Firewalking + Scripture. Algastone mine (fuel/"oil").
- **Revelation** — Scripture + Shamanism + Garrison + Schooling. **Glazing, consecration, all three hubs. The Covenant is chosen here.** (Replaces a separate Theology node — one moment, not three.)

**Wave 6 — later worlds**
- **Steel** — Firewalking + Quarrying. Needs Tier 3 material → world 3 at the earliest.
- **Clockwork** — Steel + Masonry. Machines.

**Tech as a resource (LOCKED — numbers lean on Kittens Game).**
- **Tech is a capped stockpile**, produced per second. Amount gained and cap follow Kittens' science model: Learners produce like scholars (Teachers more once Schooling supersedes them; Scriveners most); the **Library** multiplies and **raises the cap**; School and College add on top; Tech Power multiplies again. Late nodes need bigger Tech buildings before they are affordable.
- **A node costs Tech AND requires its gift.** The gift is the prerequisite, Tech is the price. The Claykin **supplicate for the gift**: *"The Claykin want to learn Tools, but they need a Hammer. Grant or deny."* Once gifted, they refine it themselves (Hammer → Axe & Pick).
- **Cost ladder follows Kittens' science curve**: Wave 1 ≈ tens–hundreds · Wave 2 ≈ hundreds–low thousands · Wave 3 ≈ low thousands · Wave 4 ≈ 5k–20k · Wave 5 ≈ 20k–60k · Wave 6 ≈ six figures. Workshop nodes follow Kittens' workshop curve, cheaper than the science node they hang on.
- **The Tech Tome = an automatic gift on a new world.** Everything the Claykin knew in the previous world is **known again: no supplication, no re-gifting — just enough Tech.** Full Tech price (the tree still takes time), but the deity's hand is never needed for old ground; the player's attention goes to *new* nodes.

## LOCKED (pending play) — Materials & base costs (mapped from Kittens Game; their ratios kept)

**Raw world materials:** wood · stone · iron · silver · gold · coal · algastone · Ambrosia · fish · herbs · holy. **Gold is a building material *or* a trade good, as the player sees fit.** **X Mine minerals:** stone / iron / silver / gold / coal / algastone.

**Opening sequence.** The Origin starts with the First Bonfire and the **First Farm (free)**. At **10 Ambrosia** the first supplication fires: *"The Claykin have found trees, but need a way to harvest them. They beg for a tool!"* → grant the **Hammer** → Tools → wood begins. No other starting stockpile.

**Population (LOCKED, ratio pending play).** The world starts with **2 created Claykin** (both farm until 10 Ambrosia trips the Hammer supplication, then one swaps to wood — the first job-swap). After that **births are automatic**: a birth needs **a free bed and a food surplus**, and **draws Souls from the hoard** — Souls → life made literal; no souls, no birth. **No birth timer.** The draw ramps as **base × 1.2 per Claykin alive** (placeholder) so that **~50 Claykin is getting hard, ~70 is a real time sink, ~100 is near impossible** — *population is the push to raze.* Two walls stack: housing cost (Shack 2.5) and the soul draw. Base tuned in play against god-phase soul income.

**Food.** Borrowed from Kittens: each Claykin eats **0.85 Ambrosia/tick**; a Farmer makes **1.0/tick** base (a Farmer feeds itself with a little over; team bonus and XP make the surplus). No seasons, so keeping up is easy by design.

**Components & consumables** (Kittens: beam 175 wood · slab 250 minerals · plate 125 iron · concrete 2500 slab + 25 steel)
| Item | Cost | Note |
|---|---|---|
| Plank | 175 wood | |
| Block | 250 stone | |
| Ingot | 125 iron | |
| **Brick** | **25 Block + 1 Ingot** | **carved from Block — our "concrete"; hangs on Stonework + Ironwork** (not clay) |
| Charcoal | 100 wood | |
| Rope | 175 Ambrosia | |
| Paper | 175 Ambrosia | |
| Ale | 100 Ambrosia | |
| Arms | 10 Ingot + 5 Plank | |
| Wares | 10 Ale + 10 Paper + 5 Rope | trade grade 1 |
| Fine Wares | 10 Brick + 10 silver + 5 Ale | trade grade 2 |
| Rich Wares | 10 gold + 10 Ingot + 5 Fine Wares | trade grade 3 — higher grades pay more per hold |
| Boat | 100 Plank + 25 Rope | |
| Ship | 150 Ingot + 500 Plank + 50 Rope | |

**Housing** (Hut · Log House · Mansion)
| Building | Cost | Ratio |
|---|---|---|
| Shack | 5 wood | 2.5 |
| Cabin | 200 wood + 250 stone | 1.15 |
| Cottage | 25 gold + 185 Brick + 75 Ingot | 1.15 |

**Storage** (Barn · Warehouse) — capacity per level
| Building | Cost | Ratio | Holds per level |
|---|---|---|---|
| Barn | 50 wood | 1.75 | wood 200 · stone 250 · iron 50 |
| Granary | 100 wood + 50 stone | 1.15 | Ambrosia 5000 · fish 500 · herbs 250 |
| Warehouse | 2 Plank + 2 Block | 1.15 | each component 100 · coal 100 · silver 50 · gold 50 · holy 100 |

**Tech** (Library · Academy · Observatory)
| Building | Cost | Ratio |
|---|---|---|
| Study | 25 wood | 1.15 |
| Library | 50 wood + 70 stone + 100 Tech | 1.15 |
| School | 200 wood + 250 stone + 3 Paper | 1.15 |
| College | 250 Ingot + 35 Block + 50 Plank + 1000 Tech | 1.10 |

**Greenware workplaces** (Field · Mine · Workshop · Pasture) — ratio 1.15
| Building | Cost |
|---|---|
| Farm | 30 wood |
| Chopper Camp | 50 wood |
| Lodge | 100 wood |
| X Mine | 100 wood |
| Angler's Hut | 75 wood + 10 Rope |
| Maker's Lodge | 100 wood + 400 stone |
| Bolder's Cabin | 40 wood |
| Hearthstone | 75 wood + 50 stone |
| Fighter Camp | 150 wood + 100 stone |

**Caste workplaces** (Lumber Mill · Smelter · Harbor · Tradepost · Chapel) — ratio 1.15
| Building | Cost |
|---|---|
| Stoneworks | 100 Plank + 250 Block + 50 Ingot |
| Forge | 200 Block + 50 Ingot + 100 Charcoal |
| Dock | 250 Plank + 50 Block + 75 Ingot |
| Outpost | 200 Plank + 250 Block |
| Barracks | 500 Plank + 200 Block + 10 gold + 50 Arms |
| Spirit Lodge | 2000 Block + 250 Paper + 250 holy |

**Revenant hubs** (Temple, scaled for 9 tiles) — plus **9 Hallowed tiles first**
| Hub | Cost |
|---|---|
| Citadel | 500 gold + 250 Block + 150 Ingot + 100 Arms |
| Cathedral | 500 gold + 250 Block + 150 Ingot + 100 Paper + 500 holy |
| Laboratory | 500 gold + 250 Block + 150 Ingot + 100 Paper + 1000 Tech |

**Special**
| Item | Cost |
|---|---|
| Kiln | 100 Clay + 50 Charcoal (deity compounds, gifted) |
| Campfire | 20 wood, ×2 each |
| **Hallowed Ground** | **77 of the caste's compound per tile** (Dawn / Hallowed Earth / Scripture) — a 9-tile hub = 693 |

## LOCKED — The Workshop tree (what Makers can craft)

**Not job multipliers** (the Claykin already get those from full teams and job XP). Every craft does one of three things: **enables**, **is consumed**, or **is a component**. Each node is a **recipe learned** the same way as science — gift the thing once, Learners study it, Makers can then make it from world materials — and hangs on the science node it needs.

**The Maker tab.** Every learned recipe is a row with **+/− buttons**; assigned Makers convert world materials into that item at a rate. No crafting clicks. **A row stalls when its inputs run dry** — either supply is short or too many Makers are on the demand. Tools never appear as rows (nothing to assign).

**Tools — one-time enables; every Claykin uses the best tool discovered**
| Tool | Science node | Enables |
|---|---|---|
| Stone Axe & Pick | Tools | Chopper Camp, stone mines |
| Iron Axe & Pick | Ironwork | iron mines, faster clearing |
| Steel tools | Steel | world 3 |

**Components — Tier 1, the 4-set.** Buildings cost components, not raw logs, past the first wave (Shack, Study, Bolder's Cabin build from raw wood). Bolder and Mason placement rates are measured in components placed.
| Component | From | Science node | Used by |
|---|---|---|---|
| Plank | wood | Carpentry | the frame of every building |
| Brick | carved from Block (+ Ingot) — our "concrete" | Stonework + Ironwork | Cottage, Fine Wares, late stone buildings |
| Block | stone | Stonework | hubs, Stoneworks, anything Masons place |
| Ingot | iron | Ironwork | Forge, Barracks, Dock hardware |

**Consumables — the Maker rows, world 1 order**
| Row | From | Science node | Spent on |
|---|---|---|---|
| Charcoal | wood | Charcoal | fuel — Kiln, Forge (world 1 fuel) |
| Rope | Ambrosia fibre | Agriculture (fibre studied) | Boats, Docks, Ships |
| Paper | Ambrosia pulp | Scripture | the Scripture line; feeds Tech |
| Ale | Ambrosia | Brewing | Belief |
| Arms | Ingots + Planks | Garrison | equips a raiding party; spent when it sails |
| Wares (3 grades) | bundles — see Materials | Trade | the trade-goods payload; spent when a trade Boat/Ship sails |
| Boat | Planks + Rope | Fishing | crew 2 Mariners; **coastal only** — deep-water fishing, Wares along the coast; no troops/missionaries |
| Ship | Planks + Rope + Ingots, at a Dock | Seafaring | crew 2; crosses deep water; **all three payloads** (troops / missionaries / trade goods) |

**Later worlds:** Cloth, Vellum, Spirits, Silk, and whatever Clockwork yields, as their tiers open.

**Fuel.** Two sources with a reason each: **Charcoal** (from wood, world 1) and **Coal** — **X Mine gains Coal** (and **Silver**, for Fine Wares) as minerals (stone / iron / silver / gold / coal / algastone). Coal burns cleaner; the Forge and the Steel node want Coal, not Charcoal.

## LOCKED — The World Arc (four beats)

1. **The Unseen Hand.** You drop **gifts** (the compounds you refined) anonymously. Claykin don't know a god exists; they advance on their own to a **ceiling**.
2. **The Kiln.** Breaking the ceiling requires **firing** — which requires *you*. The gate to advancement.
3. **The Revelation.** You choose **who to speak through** — by **glazing** a fired caste in the Kiln (Warden→**Cleric**, Shaman→**Priest**, Teacher→**Scrivener**). That caste becomes the **sole source of edicts (your will down) and petitions (their needs up)**.
4. **The Covenant.** That choice **defines the civilization**. Theology of it: the erased god returns as a *mystery*, then reveals itself once its people are ready.

## LOCKED — Covenants & the Six Societies

- **One Covenant per world** (Reformation-at-high-cost PARKED for later).
- **Straight choice — no slider.** Made at glazing with two questions: *"Which caste is closest to you?"* → the **Chosen** (your Revenants — bonus, the edict/petition voice); *"Which is the farthest?"* → the **Reviled** (negative). The remaining caste is **supporting** (neutral). Penalties are static: **bonus / neutral / negative.**
- **The three axes are already in the game:** **Holy → piety** (Priests) · **Dark → war** (Clerics) · **Wisdom/Research → knowledge** (Scriveners) — live elements *and* ascension-path themes (holy/shadow/mystic).
- **"Revenants"** = the chosen deity-contact caste (Cleric/Priest/Scrivener = the flavor of whichever you pick). Thematic: a revenant returns from death, and the deity is a killed god clawed back. **Unique buildings unlock per the Revenants chosen.**

Base archetypes: **Martial** (Clerics) · **Pious** (Priests) · **Enlightened** (Scriveners). Blended (dominant + supporting) → **six societies** (mirrors the 6 forms):

| Dominant + Minor | Society | Fantasy |
|---|---|---|
| Martial + Pious | **The Crusade** | zealots at war |
| Martial + Enlightened | **The Legion** | engineered, disciplined warfare |
| Pious + Martial | **The Inquisition** | militant church |
| Pious + Enlightened | **The Monastery** | scholar-monks; *preserves knowledge across the raze* |
| Enlightened + Martial | **The Arsenal** | science forged into might |
| Enlightened + Pious | **The Mystery School** | sacred knowledge / gnostics |

Rough bonus↔cost sketch:
- **Martial:** fast expansion, clears barriers/threats, Faithful won by conflict ↔ weak knowledge, high attrition, Belief hard in peacetime.
- **Pious:** most Faithful, stable Belief, heresy-resistant, **fastest Faithful Souls** ↔ slow tech/industry, poor expansion, zealotry.
- **Enlightened:** fastest tech/recipes, best yields, wonders sooner ↔ few Faithful, doubt-heresy, fragile vs threats.

## LOCKED — Living-world loop

- **Petitions:** Needs (unmet → Belief falls) & Wants (granted → the Faithful grow) surface on a timer; **Grant / Deny / time-out** each swing Belief and the Faithful. Flavored by the Covenant (a Martial world petitions for weapons; Pious for temples; Enlightened for schools).
- **Edicts** (= the old "commandments" — one system now): the rules you issue **through the Revenant** (Iron Fist vs Free Will, Industry vs Devotion) that bias how petitions resolve.
- **Belief** = happiness (= clay integrity); **Ale** is its one consumable lever. **The Faithful** = output → minted into **Faithful Souls** at the raze. (No "Faith" resource.)
- **Two-layer tech tree:** the entity's element discoveries gate what Claykin *may* learn (top-down); Claykin labor XP gates how *good* they are (bottom-up); minions bridge them.
- **Scaling:** the discovery/build chain **cannot finish in one playthrough** — Faithful Souls from razing accelerate the next run.

## Replay engine
Two independent build axes: **3 God Souls** (terrain/events) × **Covenant** (society), plus terrain synergies. God-souls (286 combos) × 6 societies × terrain = no two worlds alike.

---

# OPEN QUESTIONS / PARKED

**Blocks Phase-1 code (must settle first):**
- **Confirm the god power-unlock order** — user reviewing the 13-god/power list before locking (Odin early, Athena late).
- **The gods pass** (next task): re-derive each shield + counter onto the locked order (rare Holy/Dark counters stay latest); map which **compound** counters each of the final 7; finalize power magnitudes / BS costs.
- **Mixing interaction/UI** — how you actually combine (crafting grid vs recipe list). System is item+item(+item); the UI is undecided.

**Open decisions (not Phase-1 blockers):**
- **Covenant: 3 societies or 6?** With supporting = neutral, leaning **3 Revenant-defined societies** (unique buildings each) + a spare-vs-penalize sub-choice for the other two; six names kept as flavor. Confirm.
- **Covenant caste count** — leaning **keep 3** (Holy/Dark/Research = the "soul" castes; only they can be god-voice). Expanding to more god-voices = later, like Reformation.
- **Friction events — OUT** (no schisms; the Revenant choice is final). Penalties are static: **Revenant = bonus · supporting = neutral · unchosen = equal negative** (values TBD).
- **Reformation** (change Covenant mid-world at high cost) — PARKED.

**Phase-2 still open (in working order):**
- God Souls boon/bane (×13) · board size · terraform costs · petition/supplication list · Edict + Covenant value tables · unique Revenant buildings · **raiding parties / War Power numbers** · Faithful Souls math · hostile world (parked) · hero flavor text.
- Structural: expand the god map from **6 stubbed nodes** to 13, split **5 Stairway + 8 Worlds** (Hades gateway + 7 creation days); reuse `#godmap-overlay` with final-node-unlocks-next-map + forward/back navigation (LOCKED approach).

**Settled since consolidation:** Faithful Souls (kept) · Revenant = god-voice caste · no schisms · Edicts = Commandments (merged) · Thor = auto-mixing · discovery → base-element production speedup · codex persists · mixing tree = item+item(+item), tiers 3–4 restart-gated · god-map navigation approach.
