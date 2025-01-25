---
title: <% tp.file.title %>
aliases:
  - <% tp.file.title.replace(/-/g, " ") %>
category: section
tags:
  - homebrew/section
  - section
cssclasses:
  - json5e-note
  - hide-file-column
  - encounter-table
obsidianUIMode: preview
type: section
source: Homebrew
stories:
  - "[[Akt 1-K1 Durch die Wilderlande]]"
---
# <% tp.file.title %>
*Source: `VIEW[{source}]`*

- **Teil der Story**: `INPUT[inlineListSuggester(optionQuery("2_2-World/Orte"), optionQuery(#story and !#log),useLinks(partial),option(keine)):stories]`

## Encounter in diesem Abschnitt

```dataview
TABLE portrait AS "Bild", file.link AS "Name", encounter-Type AS "Encounter Type", locations AS "Orte"
FROM "2_1-Encounter" or #encounter
WHERE contains(sections, this.file.link)
SORT file.link ASC
```