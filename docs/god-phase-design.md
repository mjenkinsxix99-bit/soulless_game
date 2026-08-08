# Soulless — God Phase & World Phase Design Notes

> Living brainstorm doc. **LOCKED** = agreed direction, don't relitigate without cause.
> **OPEN** = still spitballing. Nothing here is implemented yet.

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

---

## LOCKED — The Convergence (every currency cashes out in the World)

The World tab is the sink that finally consumes the **entire** economy. One role each,
nothing orphaned:

| Currency | Becomes | Role |
|---|---|---|
| **Souls** | Life itself | Spend the hoard to breathe worshippers into being. Hoard → harvest. |
| **Tattered Souls** | The substrate | Too broken to live — become land, soil, the dead you build *on*. |
| **Burning Souls** | The divine spark | Fuel for miracles & creation events; the heat/light that powers the world. |
| **Minions** | The first servants | Turned army = labor/angels tier — assigned to build, tend, teach mortals. |
| **Elements (compounds)** | The physical world | Terrain, biomes, structures. |
| **God Souls** | The laws/domains | Shape how the world forms & what events occur (see World Creation). |
| **Divinity** | The crux | Prestige multiplier — makes the next clawback faster. |

---

## LOCKED-ish — Three-Act Structure

1. **Act I — The Pantheon:** defeat the 13 gods. Challenging enough to feel like a win,
   **NOT a drawn-out slog.** Beating them yields their power/bonuses + their God Soul.
2. **Act II — Genesis:** defeat NYX (primordial night) → unlock the power to CREATE →
   World tab opens.
3. **Act III — The Cycle:** build a world → run it (living-world loop) → raze it for a
   **significant bonus** (Divinity) → rebuild differently. Replay is the point.

Prestige nesting: existing **Ascension → Reincarnation**, plus new **World Rebirth** on top.

---

## OPEN — World Creation: the "Choose 3 God Souls" draft

- On defeating NYX, before building, the player **chooses 3 God Souls** from the pantheon.
- Each soul has a **positive AND negative** effect (some combos harder, some easier).
- The 3 chosen souls **seed the world**: terrain, available biomes, and which **events/
  petitions** occur. They also add flat bonuses.
- The other god powers (from beating them) still apply as general bonuses; only the 3
  chosen ones *shape this particular world*.
- Replay driver: pick a different 3 next cycle → a different world. (13 choose 3 = 286 combos.)

## OPEN — World representation (grid / map / structures)

Candidates (see chat for tradeoffs):
- **Node/POI map** reusing the existing god-map overlay — lowest lift, tiny saves, consistent UI. Good MVP.
- **Hex grid** — adjacency puzzles, pretty; save-safe *if* encoded as a compact int array (biome id + structure id per cell), not fat objects.
- **Square grid / concentric rings / abstract settlement panel** — other points on the spatial↔abstract axis.
- Save rule (from perf discussion): store the world as **counts/config or compact int arrays**, never big per-object arrays.

## OPEN — The Living World loop

- Everything hinges on **forked, mandatory decisions** about how to help people while they toil.
- People: collect food → build shelter → learn better structures & shrines.
- **Two-layer tech tree:**
  - *Top-down:* the entity's own **element-combination discovery chain** gates what people CAN build/use/learn.
  - *Bottom-up:* the people's own labor **XP/mastery** at learned tasks.
  - **Minions bridge them** — assigned to a task, they make the people efficient (XP boost for the people).
- **Petitions:** Needs (unmet → Belief falls) & Wants (granted → Faith surges) surface on a timer.
  Grant / Deny / time-out each swing Belief and Faith. **Commandments** (Iron Fist vs Free Will,
  Industry vs Devotion, etc.) bias how petitions resolve.
- **Belief** = happiness rating: high → Faith + growth; low → heresy/revolt/loss.
- **Faith** = the world's output. Peak followers/Faith → minted into **Divinity** at World Rebirth.
- **Scaling:** the discovery chain is long enough that it **cannot be finished on the first
  playthrough.** X followers = N Divine Souls → game+ significantly faster; chosen god souls
  stack further bonuses.

## OPEN — God fight verb (from earlier, still unsettled)

- Not out-DPS'd — **Weaken, then Take.** Weaken via **countering** (opposing elements) and
  **turning the god's own worshippers/servants** (reuse the minion-capture loop, aimed upward).
  Strip enough divinity → god drops mortal → kill & take power.
- Must stay **short and punchy**, not a slog. (Tension to resolve with the "choose 3" model —
  see chat.)

## OPEN — God Souls as regalia (parked, maybe partial)

- Earlier idea: wear god souls as **regalia/accoutrements** (build the entity's divine body),
  which later **imbue the world**. Player leaning toward the "choose 3 at creation" model instead;
  keeping regalia parked in case a hybrid emerges.
