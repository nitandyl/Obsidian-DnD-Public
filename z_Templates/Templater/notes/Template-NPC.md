---
title: <% tp.file.title %>
aliases:
  - <% tp.file.title.replace(/-/g, " ") %>
category: npc
tags:
  - npc
  - homebrew/NPC
cssclasses:
  - json5e-note
  - encounter-table
  - hide-file-column
obsidianUIMode: preview
type: npc
source: Homebrew
portrait: '![[<% tp.file.path(relative=true).replace(".md", ".png") %>]]'
portrait_path: <% tp.file.path(relative=true).replace(".md", ".png") %>
importance: 
age: 
lvl: 
languages:
  - common
---
# <% tp.file.title %>
*Source: `VIEW[{source}]`* `VIEW[!\[\[{portrait_path}\]\]][text(hidden,renderMarkdown):portrait]`
> [!infobox | left clean collapse wsmall]
> ```meta-bind
>INPUT[imageSuggester(optionQuery("z_Assets/Artwork/NPCs")):portrait_path]
> ```

- **Profil**:
	- **Rasse**: `INPUT[suggester(defaultValue(unbekannt),optionQuery("3-Ressources/CLI/races" or "3-Ressources/Homebrew/races" or #creature or "3-Ressources/CLI/bestiary" or "3-Ressources/Homebrew/bestiary"),useLinks(partial),option(unbekannt)):race]`
	- **Gender**: `INPUT[inlineSelect(option(M),option(W),option(D),option(unbekannt)):gender]`
	- **Alter**: `INPUT[number(class(nb-mb-65),placeholder(Alter)):age]`
	- **Gesinnung**: `INPUT[inlineSelect(option(chaotisch gut),option(chaotisch neutral),option(chaotisch böse),option(rechtschaffen gut),option(rechtschaffen neutral),option(rechtschaffen böse),option(neutral),option(unbekannt)):alignment]`
	- **Relevanz**: `INPUT[inlineSelect( option(minor), option(medium),option(major), option(highest)):importance]`
- **Fähigkeiten**:
	- **Sprachen**: `INPUT[inlineListSuggester(useLinks(partial),optionQuery(#language or "3-Ressources/CLI/languages" or "3-Ressources/Homebrew/languages"),option(common),option(dwarvish),option(elvish),option(giant),option(gnomish),option(goblin),option(halfling),option(orc),option(abyssal),option(celestial),option(draconic),option(deep speech),option(infernal),option(primordial),option(sylvan),option(undercommon)):languages]`
	- **Kampf Stärke**: ~Lvl `INPUT[number(class(nb-mb-35)):lvl]` `INPUT[suggester(optionQuery(#class or "3-Ressources/CLI/classes" or "3-Ressources/Homebrew/classes"),useLinks(partial),defaultValue(None)):class]`
	- **Magisches Talent**: `INPUT[slider(minValue(0),maxValue(5),defaultValue(0),addLabels(true)):magic]`
- **Zugehörigkeit**:
	- **Zu Hause**: `INPUT[inlineListSuggester(optionQuery(#location or "3-World/Orte"),useLinks(partial),option(unbekannt)):locations]`
	- **Sozialer Stand**: `INPUT[inlineSelect(option(leibeigen),option(arm),option(gewöhnlich),option(wohlhabend),option(adlig),option(keiner)):standing]`
	- **Fraktionen**: `INPUT[inlineListSuggester(optionQuery(#fraction or "3-World/Fraktionen"),useLinks(partial),option(unbekannt),option(fraktionslos)):factions]`
	- **Bekannte NPCs**: `INPUT[inlineListSuggester(optionQuery(#npc or "3-World/NPCs"),useLinks(partial)):relations]`
- **Besondere Items**: `INPUT[inlineListSuggester(optionQuery(#item or "3-Ressources/CLI/items" or "3-Ressources/Homebrew/items"),useLinks(partial)):items]`

**Berufung**: `INPUT[textArea(placeholder(Berufung)):vocation]`
```dataview
TABLE portrait AS "Bild", file.link AS "Name", encounter-Type AS "Encounter Type", locations AS "Orte"
FROM "2_1-Encounter" or #encounter
WHERE contains(npcs, this.file.link)
SORT file.link ASC
```

## Charakter und Verhalten

## Ziele & Motivationen

- **Primärziel:** 
- **Motivation:** 
- **Innerer Konflikt:**
- **Langfristige Überlegung:** 

## Backstory