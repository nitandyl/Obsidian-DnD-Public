---
title: <% tp.file.title %>
aliases:
  - <% tp.file.title.replace(/-/g, " ") %>
category: recipe
tags:
  - homebrew/ingredient
cssclasses:
  - json5e-item
obsidianUIMode: preview
item: <% tp.file.title.replace(/^Recipe-/, "") %>
rarity: Common
rarity_temp: 
dc: 8
costs: 25
type: recipe
tool: 
source: 
---
# <% tp.file.title.replace(/-/g, " ") %>
*`INPUT[inlineSelect(option(0, common), option(1, uncommon), option(2, rare), option(3, very rare), option(4, legendary)):rarity_temp]` `VIEW[ {rarity_temp} == 0 ? "Common" :  ({rarity_temp} == 1 ? "Uncommon" :  ({rarity_temp} == 2 ? "Rare" :  ({rarity_temp} == 3 ? "Very Rare" :  "Legendary")))][math(hidden):rarity]`, `VIEW[{type}]`*

- **Tool**: `VIEW[{tool}]`
- **DC**:`VIEW[  {rarity_temp} == 0 ? 8 :  ({rarity_temp} == 1 ? 12 :  ({rarity_temp} == 2 ? 15 :  ({rarity_temp} == 3 ? 18 :  20)))][math:dc]`
- **Costs**: `VIEW[ {rarity_temp} == 0 ? 25 :  ({rarity_temp} == 1 ? 100 :  ({rarity_temp} == 2 ? 500 :  ({rarity_temp} == 3 ? 1000 :  2500)))][math:costs]`  gp
- **Ingredients**: 


> [!important] Potion `VIEW[{item}]`
>
> `=embed(link(this.item))`

*Source: `VIEW[{source}]`*
