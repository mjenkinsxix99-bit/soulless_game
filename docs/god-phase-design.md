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
- **Stripping the shield is stockpile-gated (simplified — no real-time channel/regen):** each shield is a pool with a counter cost; accumulate **enough of the right counter element or compound** and spend it to wipe the gold bar. Compounds are heavy ammunition (count for more / hit multi-element shields).
- Then the **mortal HP phase** is beaten with your normal combat build.
- **Two-fold gate:** combat investment clears the HP; the right element/compound stockpile clears the shield. Miss either → wall.
- Sequential (gold to zero, *then* red). **Shield resets if you flee** (a single committed assault).
- Optional **re-shield spice** (god re-armors during mortal phase) — PARKED, use only if too easy.

## LOCKED — The Counter Wheel (which element strips which shield)

Closed loop over the 10 elements — a **perfect permutation** (every element counters exactly one and is countered by exactly one):

- **5-cycle (Wu Xing destruction):** Wood breaks Earth · Earth dams Water · Water quenches Fire · Fire melts Metal · Metal chops Wood.
- **3-cycle (works):** Research carves Stone · Stone smothers Plant · Plant reclaims Research.
- **2-cycle (the pair):** Holy ↔ Dark.

Shield element → counter you channel: Earth←Wood · Water←Earth · Fire←Water · Metal←Fire · Wood←Metal · Stone←Research · Plant←Stone · Research←Plant · Holy←Dark · Dark←Holy.

**Shield complexity scales with god power:** single-element (early) → layered/peel (mid) → blended/simultaneous (late). **Holy/Dark are the rare counters, saved for the endgame gods**, so the finale gates behind farming your rarest minion elements.

## LOCKED-ish — The 13 gods (shields, counters, lore)

Difficulty order (original), with shield element(s) → counter needed:

| # | God | Pantheon | Shield | Counter(s) | Lore hook |
|---|---|---|---|---|---|
| 1 | Morrigan | Celtic | Water | Earth | Washer at the Ford; herald of war/fate |
| 2 | Amun-Ra | Egyptian | Fire | Water | Waning sun-king; his fall = "first light" |
| 3 | Thor | Norse | Metal | Fire | Mjölnir; brute, honest wall |
| 4 | Hades | Greek | Earth | Wood | Grave-soil; roots crack the tomb |
| 5 | Athena | Greek | Research | Plant | Wisdom undone by wild growth |
| 6 | Durga | Hindu | Stone | Research | Mountain-daughter; out-think the immovable |
| 7 | Isis | Egyptian | Water + Wood | Earth, Metal | Nile flood + green life; can re-knit shield |
| 8 | Brahma | Hindu | Holy + Research | **Dark**, Plant | The Creator; grants element mixing |
| 9 | Sekhmet | Egyptian | Fire + Metal | Water, Fire | Bloodlust enrage (shield regen ramps) |
| 10 | Shiva | Hindu | Fire + Dark | Water, **Holy** | The destroyer you become |
| 11 | Odin | Norse | Research + Dark | Plant, **Holy** | Sacrifices shield HP to buff |
| 12 | Zeus | Greek | Metal + Fire + Holy | Fire, Water, **Dark** | The king to dethrone |
| 13 | NYX | Greek | Dark + Holy + Water | **Holy**, **Dark**, Earth | Primordial night; beat her → Creation |

> **NOTE:** These shields were derived for the *original difficulty order*. The **power-unlock order** (below) reorders the gods, so shields/counters must be **re-derived onto the new order** to keep the counter-difficulty ramp (rare counters late). — OPEN task.

## LOCKED — Element Mixing (the tie-in that makes it load-bearing)

**Unlocks mid-phase, at the stairway→worlds-zone gate** (after god #6) — because that's exactly when it becomes required. Base elements are minion-produced, capped 2400, and **wipe every reincarnation**. Mixing **transmutes ephemeral base elements into PERMANENT compounds** — the machine that makes farming last. Compounds do three jobs:

1. **God-shield ammunition (Phase 1) — hard gate:** the **first 6 gods (stairway) are stripped by base elements; the final 7 (worlds zone) ONLY by compounds.** Base elements go inert at the zone boundary, forcing full mixing engagement mid-phase (this *is* the mechanical meaning of the 6/7 map split). Compounds are stronger counters — strip a band faster / counter *two* bands at once (e.g. **Twilight** `holy+dark` for NYX).
2. **Economy engine:** spend a compound to **boost production of the elements/compounds below it on the tree** (the fine-tuning dial).
3. **World material (Phase 2):** the same hoard is what you build the world (and Claykin) from. Destroyer's tools become creator's tools.

**Discovery:** each discovered compound stays **known in the codex forever** (survives all resets); each discovery → a small permanent **base-element production speedup**. (No compound-production bonus — production automation is a god power, see Thor.)

**Recipe tree (LOCKED shape):** simple **item + item (+ item) = new item** combinatorial system (Little-Alchemy style). ~45 pairs + chained tiers ≈ **90 nodes**, curated to ~50–70, culminating in 6-element **wonders** and **Life** (Clay + Souls). **Deliberately un-completable run 1:** the **3rd and 4th tiers lock behind restarts** (prestige-gated), so the codex fills across many cycles. Optional **Yggdrasil-tree** visual — presentation only, undecided. Full tree layout in chat history.

**Unlock timing:** the mixing *system* goes live **mid-stairway (~god #4–5)** so Thor's #5 auto-mixing has something to act on; it becomes **mandatory at #7** (compound-only worlds zone).

**Body vs soul split:** the **7 physical elements** build the world's *body* (terrain, materials, Claykin flesh); the **3 abstract elements — Holy, Dark, Research** — define its *soul* (the Covenant axes, below).

**Brahma's power (OPEN):** since mixing now unlocks as a phase gate, Brahma's #11 slot can no longer *be* the unlock — it becomes a mixing **perk** (bonus compound yield / auto-reveal recipes — TBD in the god-writing pass).

## LOCKED — God Powers (de-duplicated; upgraded with Burning Souls)

Full audit confirmed the **multiplier economy is saturated** (DPS/click/souls/TS/crit/mana/cost all touched by 3–11 sources), so every god power sits on **whitespace** (zero/single-source levers) — automation, meta, or new-system, never a plain multiplier. **God powers upgrade with Burning Souls, same as hero powers** (no new currency layer). **God Souls are reserved for the 3-pick world seed.**

**Power-unlock ORDER** (this reorders the gods; accept two lore bends — Odin early, Athena late):

| Order | God | Power | Note |
|---|---|---|---|
| 1 | Morrigan | Auto-buy spell nodes | witch masters incantations |
| 2 | Amun-Ra | Offline earnings ×mult + raise 6h cap | the sun labors while you sleep |
| 3 | Odin | Auto-buy the sacrifice (tattered) grid | ⚠️ Allfather early = big lore bend |
| 4 | Hades | TS sink — deposit TS for 7.77% DPS (vs 6.66%) | novel conversion, his idea |
| 5 | Thor | **Auto-mixing** — auto-crafts discovered compounds; levels → faster mixing OR more parallel batches | replaces the old weak "elite-rush reach" |
| 6 | Isis | Spell auto-cast (levels = # spells automated) | |
| 7 | Durga | Boost Flurry hits/sec | her many arms; rate is fixed today |
| 8 | Shiva | Global ×Burning Souls | destruction fuels the pyres |
| 9 | Sekhmet | ×Reincarnation reward | replaces cut auto-mark; destruction→renewal |
| 10 | Athena | Auto-buy select hero powers (managed toggle) | ⚠️ wisdom-goddess late = bend |
| 11 | Brahma | Mixing perk (bonus compound yield / auto-reveal recipes) | mixing itself is a phase gate, not this power |
| 12 | Zeus | ×**some** hero-power effects | the king amplifies his champions |
| 13 | NYX | Unlock the World tab | the finale |

Cut for redundancy along the way: crit, click damage, enemy-HP reduction, overkill-chaining, elite-*timer* extension, auto-buy base upgrades, auto-collect urns, auto-mark-for-immolation (all already covered by tattered grid / minions / SMART Clickers / Jason).

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
- Structural: expand the god map from **6 stubbed nodes** to 13 (6 stairway + 7 worlds zone); reuse `#godmap-overlay` with final-node-unlocks-next-map + forward/back navigation (LOCKED approach).

**Settled since consolidation:** Faithful Souls (kept) · Revenant = god-voice caste · no schisms · Edicts = Commandments (merged) · Thor = auto-mixing · discovery → base-element production speedup · codex persists · mixing tree = item+item(+item), tiers 3–4 restart-gated · god-map navigation approach.
