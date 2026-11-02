<p align="center">
  <img src="images/art_26.jpg" alt="Fight to Steal" width="100%">
</p>

<h1 align="center">⚔️ Fight to Steal</h1>

<p align="center">
  <b>Catch them. Train them. Fight for them. The winner steals.</b><br>
  A Roblox creature-collecting game for kids, designed and built by one developer working with AI.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Roblox-Aug–Oct_2026-E2231A?style=for-the-badge&logo=roblox&logoColor=white" alt="Roblox">
  <img src="https://img.shields.io/badge/Luau-145K_lines-00A2FF?style=for-the-badge&logo=lua&logoColor=white" alt="Luau">
  <img src="https://img.shields.io/badge/design_rulings-850+-8957e5?style=for-the-badge" alt="850+ design rulings">
  <img src="https://img.shields.io/badge/built_with-Claude_Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white" alt="Built with Claude Code">
</p>

---

## 🎮 The game

A wild island full of blocky fighters, from lions and sharks to ninjas and very confused cows. You catch them, carry them home and put them in your pen, where **every fighter earns you cash every second**. You train them, hatch more, and then put one on the line: **fight another player, and the winner steals the fighter.**

That's the hook. Every creature is both a fighter and an income stream, so even one you never fight with is worth stealing, and worth defending.

```mermaid
flowchart LR
    A["🧭 EXPLORE<br/>10 zones of wilds"] --> B["🎯 CATCH<br/>throw, chase, grab"]
    B --> C["🏃 CARRY HOME<br/>beat the clock"]
    C --> D["💰 PEN<br/>cash every second"]
    D --> E["💪 TRAIN<br/>treadmills, levels"]
    E --> F["⚔️ DUEL<br/>winner steals"]
    F --> D
    D --> G["🥚 EGGS<br/>rare + secret fighters"]
    G --> D
    D --> H["🔄 REBIRTH"]
    H --> A
```

<table>
  <tr>
    <td width="50%"><img src="images/caught.jpg" alt="Caught a Legendary"><br><sub><b>Caught!</b> A Legendary FIRE fighter joins the team.</sub></td>
    <td width="50%"><img src="images/collection.jpg" alt="Zone collection"><br><sub><b>Collect.</b> Fill each zone's page, from Common to Legendary.</sub></td>
  </tr>
  <tr>
    <td><img src="images/treadmill.jpg" alt="Training on the treadmill"><br><sub><b>Train.</b> Treadmills build SPEED, and eggs wait in every zone.</sub></td>
    <td><img src="images/fighters_lineup.jpg" alt="Fighters on the field"><br><sub><b>The cast.</b> Fighters roam the island in the wild.</sub></td>
  </tr>
</table>

## ✨ What's inside

| | |
|---|---|
| 🌍 **10 zones** | One island, ten biomes, from forest and beach through desert, jungle, snow and sky to ocean and space, each with its own roster and landmarks. |
| 🐾 **170+ fighters** | Common, Rare, Epic and Legendary, plus Secret and OG variants and mutations. |
| 🔥 **5 families** | WATER → FIRE → LEAF → BLADE → ZAP → WATER. A type wheel that "water puts out FIRE" explains to an eight-year-old. |
| ⚔️ **Fights** | Pick your fighter and time your special. Every fight plays out the same on every server, because a fighter is at stake. |
| 🏃 **The catch** | Throw a ball, chase down wilds that run, and carry your catch home against a clock. |
| 💰 **Idle income** | Your pen pays every second, even while you're away. |
| 🏟️ **Arena + gauntlet** | Climb a ladder of challengers, fight other players, rescue raids. |
| 🎉 **Live world** | Restock rushes, timed events, weather, day and night, and a music director. |
| 📖 **Index** | Every fighter you've met, page by page, with rewards for full pages. |
| 🛒 **Shop** | Moment offers, a starter pack, boosts, all aimed at the moments a kid actually wants them. |

<table>
  <tr>
    <td width="33%"><img src="images/fighters_close.jpg" alt="Fighters up close"></td>
    <td width="33%"><img src="images/volcano.jpg" alt="Volcano zone"></td>
    <td width="33%"><img src="images/landmarks.jpg" alt="Zone landmarks"></td>
  </tr>
</table>

### Store art

<table>
  <tr>
    <td width="33%"><img src="images/art_6.jpg" alt="Winner steals"></td>
    <td width="33%"><img src="images/art_2.jpg" alt="K.O."></td>
    <td width="33%"><img src="images/art_19.jpg" alt="Mine now"></td>
  </tr>
  <tr>
    <td><img src="images/art_10.jpg" alt="Income per second"></td>
    <td><img src="images/art_23.jpg" alt="Mystery fighter"></td>
    <td><img src="images/art_5.jpg" alt="Versus"></td>
  </tr>
</table>

## 🤖 How it was built

I designed the game. **Claude Code** sessions built it by driving Roblox Studio directly over MCP: reading and editing live scripts, running play sessions and taking screenshots.

**A design ledger instead of memory.** Every design call, from "fighters are fought for, never bought" to "water beats fire", was written down as a numbered ruling with its reason, **853 of them** by the end. Each new session read the ledger before touching anything, so two months of decisions never got lost or quietly undone.

**Systems, not one big script.** About 40 server services (duels, arena, matchmaking, pens, income, eggs, chases, gauntlet, rescues, restocks, events, rebirth, saves) plus about 60 focused client scripts for animation, feel, camera and phone performance.

**A fight engine you can trust with stakes.** The battle core has no randomness, no clock and no side effects. The same fighters and the same button presses always give the same fight. That's what makes stealing fair.

**Measured, not guessed:**

- An in-game test harness of **9,000+ assertions** ran on every change.
- The economy and growth curves were **simulated in Python** before a number changed.
- **Analytics funnels** tracked every first-time step, and a daily dashboard showed where kids left.
- Phone performance was profiled live, with a quality governor for slow devices.

## 🧭 What happened next

Fight to Steal ran from August to early October 2026, and by then it had grown big: 434 scripts, 168K lines, 160 feature switches. For the young kids it was made for, it had become too much to take in. So I made a hard call: keep everything I learned (the tools, the test harness, the analytics, the way of working) and **start fresh** with one simple loop. That became [**+1 Spin to Fly**](https://github.com/Idosiloni/Spin-To-Fly), built and launched in five days on the same place.

## 🧰 Tech

**Roblox Studio + Luau** (server-authoritative, strict-typed core, backed-up DataStore saves) · **Roblox Studio MCP** · **Python** simulators · **Roblox AnalyticsService + Open Cloud** · **Claude Code**

---

<p align="center">
  <sub>The source code is private. This repo is a showcase.<br>
  Made by <b>Ido Siloni</b> · 2026 · also by me: <a href="https://github.com/Idosiloni/Spin-To-Fly">+1 Spin to Fly</a> · <a href="https://github.com/Idosiloni/Lucky-Ticket-Tycoon">Lucky Ticket Tycoon</a></sub>
</p>
