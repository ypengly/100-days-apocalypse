# 100 DAYS: APOCALYPSE

A browser-based survival strategy game. You have exactly 100 days to prepare
your camp before an unknown apocalypse arrives — every day is a trade-off
between gathering, building, exploring, and resting, and every night the
camp is tested.

## Play it

Open `index.html` in any modern browser. No install, no server, no
dependencies — it's a single self-contained file.

Your run autosaves to the browser's local storage after every action, so you
can close the tab and pick up where you left off. "Start a New Run" from the
title or ending screen wipes the save and begins fresh.

## How it plays

**Each day has three phases:**

- **Morning** — choose one camp-wide focus: Gather, Hunt, Build, Explore,
  Rest, or Scout. Building opens a menu of eight structures to construct or
  upgrade; Exploring offers three randomly drawn locations, each with its
  own risk and loot table.
- **Afternoon** — review resources, buildings, and survivor health, and
  spend medicine to treat the wounded before night falls.
- **Night** — a weighted random event resolves: raider attacks, storms,
  fire, theft, a strange unexplained happening, a stranger arriving at the
  gate (with a real four-way choice — let them in, trade, question, or
  refuse, each with different odds and outcomes), or a quiet night. Your
  buildings, scouting, and soldiers all shift the odds in your favor.

**Resources:** Food, Water, Wood, Metal, Medicine, Fuel. Food and water are
consumed daily by every survivor; let them run out and people start losing
health.

**Survivors** come in six traits — Farmer, Engineer, Doctor, Hunter,
Soldier, Mechanic — each with a real strength and a real weakness that
affects gathering, building cost, healing, combat, and upkeep.

**Buildings:** Shelter, Farm, Storage, Workshop, Watchtower, Medical Room,
Generator, Defensive Wall — each levels up and meaningfully changes your
odds (farm yields passive food, wall and watchtower cut attack damage and
frequency, workshop cuts build costs, and so on).

**Locations to explore:** Abandoned Supermarket, Hospital, Police Station,
Gas Station, Forest, Military Base, Underground Bunker — low-risk sites
give modest, reliable loot; high-risk sites like the Military Base and
Bunker can pay off big or cost you a survivor.

## Day 100

What you've built determines which of five endings you get, from being
overrun or left entirely alone, to holding the line, to becoming a true
fortress or a thriving community — scored on your survivors, defense,
resources, and base health at the end.

## Files

```
100-days-apocalypse/
├── index.html   # the entire game — open this
└── README.md    # this file
```

## Notes for customization

The whole game lives in `index.html`:

- `TRAITS`, `LOCATIONS`, and `BUILDINGS` near the top of the `<script>`
  block are plain data objects — safe to tweak numbers, add entries, or
  rename things without touching any logic.
- `NIGHT_EVENTS` / `resolveNight()` controls the night event odds and
  effects.
- `computeEnding()` controls the day-100 scoring and ending text.
- Styling is a single `<style>` block using CSS custom properties at the
  top (`:root { --bg, --rust, --moss, --amber, ... }`) — change the
  palette there to reskin the whole game.

No build step, no external JS dependencies — just HTML, CSS, and vanilla
JavaScript in one file.
