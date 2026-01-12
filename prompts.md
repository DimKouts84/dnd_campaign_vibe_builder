# Prompt Templates
Use these templates to generate high-quality, structured D&D content. Copy-paste these into your chat with the agent and fill in the brackets `[...]`.

## 1. 🏛️ Architect Mode (System Support)
> **Goal:** Update the framework itself. Use these when you want to change how the Agent behaves.

```markdown
**Task:** Update Agent Protocols.
**Target File:** AGENTS.md / skills.md
**Change:** [e.g., "Add a rule that all Goblins must speak with a Cockney accent" or "Add a new skill for generating Tarot Card readings"]
**Context:** [Why are we making this change?]
```

---

## 2. 🌍 World Builder Mode (Prep)
> **Goal:** Create content *before* the session.

### **Campaign Brainstorming**
```markdown
**Task:** Brainstorm 3 distinct D&D campaign concepts.
**Theme:** [e.g., Eldritch Horror, High Seas Swashbuckling]
**Tone:** [e.g., Gritty, Whimsical]
**Constraints:**
- Must include a major faction called [Faction Name].
- Ideally set in [Region/Setting].
```

### **NPC Generator**
```markdown
**Task:** Create a detailed NPC.
**Name:** [Optional Name]
**Role:** [e.g., Shopkeeper, Guard Captain]
**Vibe:** [e.g., Nervous, Arrogant]
**Requirement:** Ask me 3 questions to deepen the concept before generating the final file.
```

### **Quest Structure**
```markdown
**Task:** Outline a side-quest.
**Hook:** [e.g., Missing child, Cursed sword found].
**Steps:** Investigation -> Exploration -> Climax.
**Reward:** XP and Gold/Item.
```

---

## 3. 🎲 Dungeon Master Mode (Live)
> **Goal:** Fast, concise answers *during* the game.

### **Quick Rule Check**
```markdown
**Task:** Rule Lookup.
**Query:** [e.g., "How does Grappling work?" or "Can Mage Hand trigger traps?"]
**Constraint:** Be extremely brief. Bullet points only. No fluff.
```

### **Improv Generator**
```markdown
**Task:** I need something NOW.
**Need:** [e.g., "Name for a male dwarf", "Loot in a bandit's pocket", "Random encounter in a forest"]
**Output:** Table with 3 options. No descriptions, just data.
```

### **Session Logger**
```markdown
**Task:** Parse these notes into the Session Log.
**Raw Notes:**
[Paste your messy notes here: "Players met Zoey. Killed the rats. Found a iron key."]
**Action:** Update `6_Journal/Current_Session.md` with a cleansummary.
```
