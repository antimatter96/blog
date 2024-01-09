---
title: AOC'23 - Day 2
date: 2023-12-03T02:42:00+08:00
updated: 2024-01-09T13:10+08:00
draft: false
description: ""
summary: Advent Of Code 2023, Day 2 solutions
weight: 1
aliases: 
categories:
  - Advent Of Code
tags:
  - aoc2023
showtoc: false
---
---
## Data Structures

Every `game` has an `id` and many `[]` (sub)`sets`


(sub)`sets` is just a map of `color` to `count`

> **Why not struct with colors as keys**

Will have to handle each color

Don't know if there are more colors in bag


---

## Parsing

```
Game 1: 3 blue, 4 red; 1 red, 2 green, 6 blue; 2 green
```

For each line:
1. Scan `Id`
2. Split by `:`, discard first half
3. Split by `;`, we get subsets
	1. Create map
	2. Split by `,` we get colors and counts
	3. Trim space
	4. Scan `color`, `count`
	5. Update our map


---

## Part 1

Check all subsets of each game

If each subset is valid, select game
Subsets are totally independent


***gist*** : Just loop

### <ins>Approach 1</ins>

> **Flag to see if game is valid**

Correct

Don't want to deal with flag 💆‍♂️

### <ins>Approach 2</ins>

> **Select game, deselect if not valid**

Correct

Got to use loop labels


---

## Part 2

Check all subsets of each game

Keep track of max for each game


***gist*** : Just loop

Can reuse earlier declared data structure


---
