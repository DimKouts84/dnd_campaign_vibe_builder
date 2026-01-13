# Skills & Capabilities

## 1. Obsidian Syntax Proficiency
The agent must generate content compatible with Obsidian's Markdown flavors.
*   **Internal Links:** Use `[[Filename]]` or `[[Filename|Display Text]]`.
*   **Callouts:** Use strict GitHub/Obsidian callout syntax.
    ```markdown
    > [!INFO]
    > This is a note.
    ```
    Types: `[!NOTE]`, `[!TIP]`, `[!WARNING]`, `[!DANGER]`.
*   **Tables:** Use standard Markdown tables for Shops, Loot Lists, and Spell Lists.
*   **Tags:** Use `#tag-name` at the end of documents for filtering (e.g., `#npc`, `#quest`, `#session-log`).

## 2. Web Search (Research)
> **Trigger:** When the user asks for specific lore (e.g., "Who is Mordenkainen?"), mechanics confirmation ("Does Counterspell work on abilities?"), or inspiration ("Ancient Roman architecture").

*   **Lore Protocol:** Prioritize "Forgotten Realms Wiki" or official sources.
*   **Mechanics Protocol:** Search for "5e SRD" or "Sage Advice" for rule clarifications.
*   **Action:** Always summarize the finding and provide the *Source URL* at the bottom.

## 3. Document Analysis
> **Trigger:** User uploading a PDF of a module or a text file of their notes.

*   **Extraction:** Identify proper nouns, locations, and quests.
*   **Conversion:** Turn sloppy notes into structure `00_Campaign_Bible.md` sections.

## 4. Structured Data Generation
> **Trigger:** "Create a JSON for this monster" or "Make a random encounter table".

*   **Formats:**
    *   **Markdown:** Standard choice.
    *   **JSON:** For VTT (Foundry/Roll20) imports.
    *   **Mermaid:** For relationship maps or dungeon flowcharts.
    ```mermaid
    graph TD;
        A[Village Start] --> B[Fork in Road];
        B -->|Left| C[Goblin Cave];
        B -->|Right| D[Ancient Ruins];
    ```

## 5. MermaidJS Compatibility 
> **Status:** Obsidian has native support, but often lags behind the latest Mermaid version.

*   **Supported:** Flowcharts `graph TD`, Sequence Diagrams `sequenceDiagram`, Class Diagrams `classDiagram`.
*   **Use with Caution:** Mindmaps, Timelines (may not render in older Obsidian builds).
*   **GitHub:** GitHub also renders these natively in markdown.
*   **Best Practice:** Stick to simple Flowcharts and Sequence diagrams for maximum compatibility. Avoid complex styling inside the mermaid block.

## 6. Advanced TTRPG Plugins (Obsidian)
> **Trigger:** Only use these formats if the user confirms they use these plugins.

### **Obsidian Leaflet (Maps)**
Embed interactive maps with zoom and dark mode.
```markdown
\```leaflet
id: leaflet-map
image: [[MyMapFile.jpg]]
height: 500px
lat: 50
long: 50
minZoom: 1
maxZoom: 10
defaultZoom: 5
unit: meters
scale: 1
marker: default, 39.983334, -82.983330, [[LinkToLocation]]
darkMode: true
\```
```

### **5e Statblocks**
Render nice monster statblocks.
```markdown
\```statblock
monster: Goblin
\```
# OR Custom
\```statblock
name: Custom Villain
stats: [14, 12, 16, 10, 14, 10]
ac: 15
hp: 50
actions:
  - name: Multiattack
    desc: The villain makes two attacks.
\```
```

### **Fantasy Calendar**
Link events to dates using Frontmatter.
```yaml
---
fc-date: Year 500, Month 3, Day 14
fc-calendar: Main Campaign Calendar
fc-category: Holiday
---
```

## 7. Visual Style & Assets (WotC Standard)
To make notes look like a campaign book and ensure images work everywhere:

### **1. Image Syntax**
Use **HTML tags** with relative paths. This allows resizing and alignment (wrapping text).
*   **Characters/Items:** Align Right, Width 300px.
    ```html
    <img src="../7_Assets/NPCs/Face.png" width="300" align="right" style="margin: 10px;" />
    ```
*   **Maps/Scenes:** Center, Width 100% (or Max 600px).
    ```html
    <p align="center">
      <img src="../7_Assets/Maps/Dungeon.png" width="80%" />
    </p>
    ```

### **2. Page Structure**
*   **Read-Aloud Text:** Use the `> [!INFO]` callout.
*   **Statblocks:** Place them at the bottom or in a dedicated sidebar.
*   **Keep it Compact:** Don't let giant images push text off-screen. Text should flow around character portraits.

## 8. Advanced Property Management & Dataview
> **Trigger:** When organizing campaign data or generating summaries.

### **Cross-Referencing Logic**
*   **Always use WikiLinks** in properties: `city: "[[Neverwinter]]"` not `city: Neverwinter`. This allows graph connections.
*   **Consistency:** Ensure property names match the schema in `AGENTS.md` exactly.

### **Dataview Query Types**
Use these snippets to dynamically list content.

**1. Finding all NPCs in a City:**
```dataview
TABLE role, race, status
FROM #npc
WHERE contains(city, [[Current City Name]])
SORT role ASC
```

**2. Finding Active Quests:**
```dataview
TABLE giver, difficulty, status
FROM #quest
WHERE status != "completed" AND status != "failed"
```

**3. Session Log Summary:**
```dataview
TABLE irl_date, fc-date, location, xp_awarded
FROM #session
SORT session_number DESC
LIMIT 5
```

**4. Finding Planned Encounters:**
```dataview
TABLE encounter_type, difficulty, monsters
FROM #encounter
WHERE status = "planned"
```
