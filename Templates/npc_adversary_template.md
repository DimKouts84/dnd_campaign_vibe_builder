---
type: npc
city: "[[{City Name}]]"
area: "[[{Region Name}]]"
faction: "[[{Faction Name}]]"
status: active
role: villain
race: "{Race}"
class: "{Class}"
alignment: "{Alignment}"
cr: {number}
tags:
  - npc
---

# {NPC Name}
**Race:** {Race} | **Class:** {Class} | **Alignment:** {Alignment}

<img src="../7_Assets/NPCs/{image_name}.png" width="300" align="right" style="margin: 0px 0px 10px 10px;" />

> [!WARNING] The Vibe
> {A menacing or unsettling description. E.g., "Shadows seem to lengthen around her. The air turns cold."}

## 📖 Backstory
{Detailed history. How they became who they are. Their tragedy or corruption. This should be intricate.}

## 🧠 Personality Profile
*   **Motivation:** {Grand goal. e.g., "Eternal youth at any cost."}
*   **Weakness:** {Fatal flaw. e.g., "Arrogance; underestimates mortals."}
*   **Ideal:** {Twisted belief. e.g., "Power is the only truth."}
*   **Flaw:** {Specific quirk. e.g., "Obsessed with mirrors."}

## ⚔️ Tactics & Schemes
*   **Current Plot:** {What are they doing right now?}
*   **Combat Style:** {Do they fight directly or use minions?}
*   **Escape Plan:** {How do they survive defeat?}

## 🩸 Statblock
```statblock
monster: {SRD Monster Name}
# OR Custom
name: {NPC Name}
hp: {HP}
ac: {AC}
actions:
  - name: Signature Move
    desc: {Description}
```
