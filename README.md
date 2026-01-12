# 🐉 The D&D Campaign Vibe Builder

Welcome, bold adventurer, to the **Campaign Vibe Builder**! This isn't just an *opinionated* collection of files; it's a **magical workshop** designed to turn your scattered thoughts into epic sagas. It is ready system with templates, to download a begin building.  

It can be used as an world builder, an organization system to keep notes and track your progress, to run your campaigns, and to generate content for your campaigns. Without getting lost with the help of LLMs & code editors (like GitHub Copilot, Claude, Cline, or Antigravity) and other amazing tools like Obsidian.

<br>

<p align="center">
  <img src="assets\dnd_campaign_vibe_banner_17682470515621.png" height="350" alt="D&D Campaign Vibe Builder Banner">
</p>

<br>

---

## 🌟 What is this?
This is an **Agentic Framework** based on the **Agentic AI Foundation (AAIF)** standards. It empowers you to collaborate with AI agents (like Claude, Cline, or Antigravity) to build D&D 5th Edition campaigns that feel *alive*.

## 🧙‍♂️ How to Use
1.  **Summon the Agent:** Open this folder in your favorite AI code editor.
2.  **Read the Grimoire:** Check `AGENTS.md` to understand your new assistant's personality (Positive! Imaginative! Helpful!).
3.  **Cast a Spell:** Copy a template from `prompts.md` into the chat to generate instant content.
4.  **Build Your World:**
    *   Duplicate the `mock_campaign_{name}` folder.
    *   Rename it to your campaign's title (e.g., `The_Frozen_Throne`).
    *   Start filling in the `1_Locations`, `2_NPCs`, and `3_Quests` with the help of your AI co-DM!

<br>

## 🧩 Advanced Plugin Support
We support power-user features for heavily modded Obsidian vaults!
*   **Obsidian Leaflet:** Ask for interactive maps.
*   **5e Statblocks:** Get beautifully rendered monster blocks.
*   **Fantasy Calendar:** Auto-tag your session logs with in-game dates.
*   *Just tell the agent you use them during setup!*

<br>

## 📂 The Workshop Structure

When you initialize a new campaign, you'll get this organized structure:

```text
{campaign_name}/
├── 00_Campaign_Bible.md       # The core concept, themes, and factions
├── 0_Chapters/                # High-level story arcs and syncopsis
├── 1_World/
│   └── {Region}/
│       └── {City}/
│           ├── Locations/     # Keys locations & POIs
│           ├── Shops/         # Merchants & inventories
│           └── Encounters/    # Combat & social scenarios
├── 2_NPCs/
│   └── {Region}/
│       └── {City}/            # Friendly & Hostile NPCs
├── 3_Quests/                  # Active and backlog quests
├── 4_Party/                   # PC Sheets (Stats, Backstories, Loot)
├── 6_Journal/                 # Session notes (Lazy DM style)
├── 7_Assets/                  # Maps, tokens, and handout images
└── Templates/                 # Ready-to-use MD templates & Schema
```

<br>

## 🚀 Key Features
*   **Obsidian Ready:** All files use `[[WikiLinks]]` and Callouts for beautiful rendering in Obsidian. Also includes specific skills to write accurate markdown code for Obsidian [TTRPG plugins](https://publish.obsidian.md/hub/02+-+Community+Expansions/02.01+Plugins+by+Category/Plugins+for+TTRPG).
*   **MermaidJS Support:** Visualize your dungeons and flowcharts.
*   **Imaginative Co-Pilot:** The agent is trained to be **proactive**—it won't just nod; it will suggest floating islands, cursed swords, and goblin masquerade balls!

<br>

---

> I took inspiration from the [**Power Word Spill** Youtube Video](https://www.youtube.com/watch?v=DBgWB1NF7hY) to create this project. <br>
> *May all your hits be **Crits**!* 🎲
