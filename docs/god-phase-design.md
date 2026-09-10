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
| **Faith** | The world's output | Farmed from Claith via the Covenant/priesthood. |
| **Faithful Souls** | The prestige crux (was "Divinity") | Banked at the raze; makes each re-run much faster. |

---

## LOCKED — Three-Act Structure

1. **Act I — The Pantheon:** defeat the 13 gods. Challenging but **not a slog**. Each yields a power + its God Soul.
2. **Act II — Genesis:** defeat **NYX** (primordial night) → unlock the power to CREATE → World tab opens.
3. **Act III — The Cycle:** build a world → run it → **raze it** for Faithful Souls → rebuild differently. Replay is the point.

Prestige nesting: existing **Ascension → Reincarnation**, plus new **World Rebirth** on top.

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

## LOCKED — Element Mixing (the tie-in that makes it load-bearing)

**Unlocks mid-phase, at the stairway→worlds-zone gate** (after god #6) — because that's exactly when it becomes required. Base elements are minion-produced, **capped at 5,000** (raised from 2400 to give the new sinks room; the Portal still requires 2400 — split `ELEMENT_CAP=5000` from `PORTAL_REQ=2400`), and **wipe every reincarnation**. **Compounds are uncapped and permanent.** Mixing **transmutes ephemeral base elements into PERMANENT compounds** — the machine that makes farming last. Compounds do three jobs:

1. **God-shield ammunition (Phase 1) — hard gate:** the **5 Stairway gods are stripped by base elements; the 8 Worlds gods (Hades + the 7 creation days) ONLY by compounds.** Base elements go inert at the map boundary (Hades = the first, gentlest compound fight), forcing full mixing engagement mid-phase. Compounds counter *two* bands at once when they carry both counter-elements (e.g. **Holy Water** `water+holy` strips both of Shiva's bands). All god-counter compounds are 2-element (tier-1) — triple/transcension-gated compounds are never counters.
2. **Economy engine:** spend a compound to **boost production of the elements/compounds below it on the tree** (the fine-tuning dial).
3. **World material (Phase 2):** the same hoard is what you build the world (and Claykin) from. Destroyer's tools become creator's tools.

**Discovery:** each discovered compound stays **known in the codex forever** (survives all resets); each discovery → a small permanent **base-element production speedup**. (No compound-production bonus — production automation is a god power, see Thor.)

**Recipe tree (LOCKED shape):** simple **item + item (+ item) = new item** combinatorial system (Little-Alchemy style). ~45 pairs + chained tiers ≈ **90 nodes**, curated to ~50–70, culminating in 6-element **wonders** and **Life** (Clay + Souls). **Deliberately un-completable run 1:** the **3rd and 4th tiers lock behind restarts** (prestige-gated), so the codex fills across many cycles. Optional **Yggdrasil-tree** visual — presentation only, undecided. Full tree layout in chat history.

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

## LOCKED — Representation: fixed isometric hex board

- **Fixed board, fully on-screen — no scrolling/camera/pathfinding.** Art = pre-drawn iso hex tiles (sprites), stamped at grid positions; redraw only on change (off the hot path).
- **Procedurally seeded each life by the 3 chosen God Souls** (weighted terrain roll + a guarantee pass for playability).
- **Tiles = resource / barrier / threat** (grass, forest→wood, mountain→stone/ore, water→fish, lava→threat, sand). **Terraform verbs:** clear, cool, mine, irrigate, replant, build.
- **Barriers replace fog** — you expand by *taming* obstacles (cool the lava → obsidian ground), not by revealing gray tiles.
- **Save-safe:** store the board as a **flat array of small ints** (terrain id + structure id per hex), never fat per-object arrays.
- Two technical wrinkles (both standard): iso **draw order** (back-to-front) and **hex hit-detection** (Red Blob Games reference).

## LOCKED — The Claykin (the created life)

- **Claykin = Clay + Souls.** Clay (a compound) is the body; Souls (the hoard) are the life — closing the convergence loop ("Souls → life").
- **Belief/happiness = the integrity of the clay:** content = fired & whole; neglected = dry, **crack, crumble to dust** (population loss). Heresy is literal breakage.
- **The raze = "return to dust":** Claykin crumble back to clay and you **reclaim their souls as Faithful Souls**. *"From clay I formed you; to clay you return."* The reset is an **un-forming**, not a delete.
- Pottery is **transformation, not leveling** (see Castes).

## LOCKED — Castes (transformation = consecration, not upgrade)

Base **greenware** Claykin do the primal work (food, basic huts). **Firing with a specific compound** transforms a greenware into a **specialist** — dedicated to one job, removed from the general pool (a real allocation cost). Worker castes so far:

- **Masons** — structures & breaking barrier tiles
- **Firewalkers** — work lava/forges/hostile tiles
- **Mariners** — sail, cross water, explore/expand
- **Wardens** — war/defense · **Shaman** — rites · **Teachers/Scribes** — learning
- (more to define)

Compounds forge castes → **mixing (Phase 1) feeds society (Phase 2).** Same system, three jobs (shields → economy → castes).

## LOCKED — The World Arc (four beats)

1. **The Unseen Hand.** You drop **gifts** (the compounds you refined) anonymously. Claykin don't know a god exists; they advance on their own to a **ceiling**.
2. **The Kiln.** Breaking the ceiling requires **firing** — which requires *you*. The gate to advancement.
3. **The Revelation.** You choose **who to speak through** — a worker caste ascends into your **channel** (Warden→**Cleric**, Shaman→**Priest**, Teacher→**Scrivener**). That caste becomes the **sole source of edicts (your will down) and petitions (their needs up)**.
4. **The Covenant.** That choice **defines the civilization**. Theology of it: the erased god returns as a *mystery*, then reveals itself once its people are ready.

## LOCKED — Covenants & the Six Societies

- **One Covenant per world** (Reformation-at-high-cost PARKED for later).
- **Straight choice — no slider.** Pick your **Revenants** (dominant deity-contact caste) + a **supporting** caste; the **third, unchosen caste inflicts a negative** (that faction, neglected). Dominant = full bonuses + penalties + the edict/petition voice; supporting = patches the dominant's weakness.
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
- **Martial:** fast expansion, clears barriers/threats, Faith from conflict ↔ weak knowledge, high attrition, Belief hard in peacetime.
- **Pious:** highest Faith, stable Belief, heresy-resistant, **fastest Faithful Souls** ↔ slow tech/industry, poor expansion, zealotry.
- **Enlightened:** fastest tech/recipes, best yields, wonders sooner ↔ low Faith, doubt-heresy, fragile vs threats.

## LOCKED — Living-world loop

- **Petitions:** Needs (unmet → Belief falls) & Wants (granted → Faith surges) surface on a timer; **Grant / Deny / time-out** each swing Belief & Faith. Flavored by the Covenant (a Martial world petitions for weapons; Pious for temples; Enlightened for schools).
- **Edicts** (= the old "commandments" — one system now): the rules you issue **through the Revenant** (Iron Fist vs Free Will, Industry vs Devotion) that bias how petitions resolve.
- **Belief** = happiness (= clay integrity). **Faith** = output → minted into **Faithful Souls** at the raze.
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

**Later content (design-doc only for now):**
- God Souls boon/bane (×13) · hex tile types + terraform costs + board size · worker-caste jobs & firing recipes · petition list · Edict + society value tables · unique buildings · Faithful Souls bonus math · hero flavor text.
- Structural: expand the god map from **6 stubbed nodes** to 13, split **5 Stairway + 8 Worlds** (Hades gateway + 7 creation days); reuse `#godmap-overlay` with final-node-unlocks-next-map + forward/back navigation (LOCKED approach).

**Settled since consolidation:** Faithful Souls (kept) · Revenant = god-voice caste · no schisms · Edicts = Commandments (merged) · Thor = auto-mixing · discovery → base-element production speedup · codex persists · mixing tree = item+item(+item), tiers 3–4 restart-gated · god-map navigation approach.
