---
title: AOC'23 - Day 2
date: 2023-12-03T02:42:00+08:00
updated: 2024-01-08T15:16+08:00
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
### Data Structures

Every `game` has an `id` and many `[]` (sub)`sets`


(sub)`sets` is just a map of `color` to `count`

> **Why not struct with colors as keys**

Will have to handle each color

Don't know if there are more colors in bag

### Parsing

```
Game 1: 3 blue, 4 red; 1 red, 2 green, 6 blue; 2 green
```

For each line:
1. Scan `Id`
2. Split by `:`, discard first half
3. Split by `;`, we get subsets
	1. Split by `,` we get colors and counts
	2. Trim space
	3. Scan `color`, `count`


### Part 1

Extract a number from each line, alphabets are useless

Need a two digit number


```
rr123rr37t => 17
rr8t => 88
```



***gist*** : Find a number once from the front and once from the back



### <ins>Approach 1</ins>

> **Treating `string` as `[]byte`,  (`for i:= 0; i <....`)**

Easy but incorrect for edge cases

Does not deal properly with non-alphanumeric characters which take more than 1 byte

### <ins>Approach 2</ins>

> **Treating `string` as `[]rune`, (`for _, r := range`)**

Correct

But did not want to deal with reversing the string to get the last digit


---

### Part 2

Extract a number from each line, alphabets can be numbers spelled out

Need a two digit number

```
a1onetwo7three => 13
aonenine => 19
```

***gist*** : Replace words with numbers, then do Part 1



### <ins>Approach 1</ins>

> **Replace words with corresponding number, (`one => 1`)**

Incorrect

Direct replacing will fail as words might overlap
```
twone => 2ne => 2
BUT
twone => 21
```
### <ins>Approach 2</ins>

> **Replace words with corresponding number and the word, (`one => one1one`)**

Correct

Hacky but works 🤷‍♀️
```
twone => twone1one => two2twone1one
OR
twone => two2twone => two2twone1one
```
Verified that order does not matter as long as we are replacing only once



---
