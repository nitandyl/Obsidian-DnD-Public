---
title: <% tp.file.title %>
aliases:
  - <% tp.file.title.replace(/-/g, " ") %>
category: item
tags:
  - homebrew/ingredient
cssclasses:
  - json5e-item
obsidianUIMode: preview
weight: 0
value: 
rarity: 
rarity_temp:
type: ingredient
source: 
creature:
---
# <% tp.file.title %>
*`INPUT[inlineSelect(option(common), option(uncommon), option(rare), option(very rare), option(legendary)):rarity]` `VIEW[ {rarity_temp} == 0 ? "Common" :  ({rarity_temp} == 1 ? "Uncommon" :  ({rarity_temp} == 2 ? "Rare" :  ({rarity_temp} == 3 ? "Very Rare" :  "Legendary")))][math(hidden):rarity]`, `VIEW[{type}]`*

- **Cost**: `VIEW[ {rarity_temp} == 0 ? 5 :  ({rarity_temp} == 1 ? 10 :  ({rarity_temp} == 2 ? 50 :  ({rarity_temp} == 3 ? 150 :  500)))][math:value]` gp
- **Weight**: `VIEW[ {weight} == 0 ? "-" : {weight} + " lbs."]`

*Source: `VIEW[{source}]`*


> [!statblock] Creature Source: `VIEW[{creature}]`
> 
> - 
> - 
> `=embed(link(this.creature))`

