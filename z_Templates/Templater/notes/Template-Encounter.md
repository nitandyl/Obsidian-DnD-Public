---
title: <% tp.file.title %>
aliases:
  - <% tp.file.title.replace(/-/g, " ") %>
category: Encounter
tags:
  - encounter
  - homebrew/Encounter
cssclasses:
  - json5e-note
obsidianUIMode: preview
type: Encounter
encounter-Type: 
source: Homebrew
portrait: "![[z_Assets/Artwork/Encounter/default.png]]"
portrait_path: z_Assets/Artwork/Encounter/default.png
locations: 
sections: 
stories:
  - "[[Akt 1-K1 Durch die Wilderlande]]"
---
# <% tp.file.title %>
*Source: `VIEW[{source}]`* `VIEW[!\[\[{portrait_path}\]\]][text(hidden,renderMarkdown):portrait]`
> [!infobox | clean collapse wsmall]
> ```meta-bind
> INPUT[imageSuggester(optionQuery("z_Assets/Artwork/Encounter"), optionQuery("z_Assets/Artwork/Locations")):portrait_path]
> ```

- **Encounter Type:** `INPUT[inlineSelect(option(other), option(Combat), option(Exploration),option(Roleplay), option(Combat & Roleplay), option(Exploration & Roleplay),option(Combat & Exploration), option(Combat Roleplay & Exploration) ):encounter-Type]`
- **Nennenswerte NPCs:** `INPUT[inlineListSuggester(optionQuery(#npc or "3-World/NPCs"),useLinks(partial)):npcs]`
- **Orte:** `INPUT[inlineListSuggester(optionQuery(#location or "3-World/Orte"),useLinks(partial),option(keine)):locations]`
- **Teil der Story**: `INPUT[inlineListSuggester(optionQuery("2_2-World/Orte"), optionQuery(#story and !#log),useLinks(partial),option(keine)):stories]`
	- **Abschnitt**: `INPUT[inlineListSuggester(optionQuery(#section and !#template)useLinks(partial)):sections]`
- **Items**: `INPUT[inlineListSuggester(optionQuery(#item or "3-Ressources/CLI/items" or "3-Ressources/Homebrew/items"),useLinks(partial)):items]`

## Setup

- Die Party ist auf dem Weg nach [[Silberfurt]] durch die [[Wilderlande]]

## Details


## Outcomes & Rewards

