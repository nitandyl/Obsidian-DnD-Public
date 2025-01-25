---
title: <% tp.file.title %>
aliases:
  - <% tp.file.title.replace(/-/g, " ") %>
category: item
tags:
  - homebrew/item
cssclasses:
  - json5e-item
obsidianUIMode: preview
weight: 0
value: 50
rarity: Common
rarity_temp: 
type: potion
recipe: Recipe-<% tp.file.title %>
source: 
---
# <% tp.file.title %>
*`INPUT[inlineSelect(option(0, common), option(1, uncommon), option(2, rare), option(3, very rare), option(4, legendary), option(5, minor)):rarity_temp]` `VIEW[ {rarity_temp} == 0 ? "Common" :  ({rarity_temp} == 1 ? "Uncommon" :  ({rarity_temp} == 2 ? "Rare" :  ({rarity_temp} == 3 ? "Very Rare" : ( {rarity_temp} == 4 ? "Legendary":"Minor"))))][math(hidden):rarity]`, `VIEW[{type}]`*

- **Cost**: `VIEW[ {rarity_temp} == 0 ? 50 :  ({rarity_temp} == 1 ? 200 :  ({rarity_temp} == 2 ? 1000 :  ({rarity_temp} == 3 ? 2000 : ( {rarity_temp} == 4 ? 5000 : 20))))][math:value]` gp
- **Weight**: `VIEW[ {weight} == 0 ? "-" : {weight} + " lbs."]`
- **Recipe**: `=link(this.recipe)`

*Source: `VIEW[{source}]`*



