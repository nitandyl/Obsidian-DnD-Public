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
rarity: Minor
dc: 7
costs: 10
duration: 2
costs_m: 45
duration_m: 8
type: recipe
tool: Alchemist's Supplies or Herbalism Kit
source: Potion Brewing and Ingredient Gathering
---
# <% tp.file.title.replace(/-/g, " ") %>
*`VIEW[{rarity}]`, `VIEW[{type}]`*

- **Tool**: `VIEW[{tool}]`
- **DC**:`VIEW[{dc}]`
- **Costs**: `INPUT[number(class(nb-mb-65)):costs]`  gp
- **Crafting Time**: `VIEW[{duration}]` h
- **Ingredients**: 

**Crafting a batch of 5**:
- **Costs**: `VIEW[round({costs}*4.5,2)][math:costs_m]`
- **Crafting Time**: `VIEW[{duration}*4][math:duration_m]` h
- **same Ingredients**

> [!important] Potion `VIEW[{item}]`
>
> `=embed(link(this.item))`

*Source: `VIEW[{source}]`*
