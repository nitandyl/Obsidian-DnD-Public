---
title: <% tp.file.title %>
aliases:
  - <% tp.file.title.replace(/-/g, " ") %>
category: location
tags:
  - location
  - homebrew/location
cssclasses:
  - json5e-note
  - npc-table
  - encounter-table
  - hide-file-column
obsidianUIMode: preview
type: location
source: Homebrew
portrait: '![[<% tp.file.path(relative=true).replace(".md", "") %>.png]]'
portrait_path: <% tp.file.path(relative=true).replace(".md", "") %>.png
---
# <% tp.file.title %>
*Source: `VIEW[{source}]`* `VIEW[!\[\[{portrait_path}\]\]][text(hidden,renderMarkdown):portrait]`
> [!infobox | clean collapse wfull]
> ```meta-bind
> INPUT[imageSuggester(optionQuery("z_Assets/Artwork/Locations")):portrait_path]
> ```

- **Regierende Fraktion**: `INPUT[suggester(defaultValue(keine),optionQuery(#faction or "3-World/Fraktionen"),option(keine),option(unbekannt))]`
- **Machthabende NPCs**: `INPUT[inlineListSuggester(option(niemand),option(unbekannt),optionQuery(#npc or "3-World/NPCs")):rulers]`
- **Fraktionen**: `INPUT[inlineListSuggester(optionQuery(#faction or "3-World/Fraktionen")):factions]`

## Nennenswerte NPCs

```dataview
TABLE portrait AS "Bild", file.link AS "Name", race AS "Rasse", vocation AS "Beruf"
FROM "3-World/NPCs" or #npc
WHERE contains(locations, this.file.link)
SORT file.link ASC
```

## Encounter an diesem Ort 

```dataview
TABLE portrait AS "Bild", file.link AS "Name", npcs AS "NPCs", encounter-Type AS "Encounter Type"
FROM "2_1-Encounter" or #encounter
WHERE contains(locations, this.file.link)
SORT file.link ASC
```

## Lore und Hintergründe