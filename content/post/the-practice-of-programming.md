---
title: "The Practice Of Programming"
date: 2020-03-11T03:11:33+05:30
draft: false
summary: "Something goes here"
backtotop:  true
---


I read the book **The Practice of Programming**

### Basic Principles of Good Software

- Simplicity (keeping programs short and manageable)
- Clarity (making sure they are easy to understand, for people as well as machines)
- Generality (means they work well in a broad range of situations and adapt well as new situations arise)

=> Automation (which lets the machine do the work for us, freeing us from mundane tasks)

## Style

### Purpose of Style

> Make the code easy to read for yourself and others

### Rules

#### Regarding Naming

A variable or a function name labels an object, conveys information about its purpose.

Why Bother ?
> Naming conventions make it easier to understand your own code. as well as code
> written by others. They also make it easier to invent new names as the code is being
> written. The longer the program, the more important is the choice of good. descriptive,
> systematic names

tl;dr:

- informative
- Concise
- memorable,
- and pronounceable

The broader the scope of a variable, the more information should be conveyed by its name.

Since Global variables can crop up anywhere in a program, they need names long enough and
descriptive enough to remind the reader of their meaning.
Use descriptive names for globals, short names for locals.


**Be consistent**
Give related things related names that show their relationship and highlight
their difference. Eg in a class

**Use active names for functions**
Function names should be based on active verbs, perhaps followed by nouns:
Functions that return a boolean (true or false) value should be named so that the return
value is unambiguous (check vs is)

**Be accurate.**
It conveys information to the reader. A misleading name can result in mystifying bugs
At the time the code is written, this might not cause trouble, but if the program is modified later, perhaps by a different programmer,
the name is sure to confuse.

Consistent adherence to a sensible convention.
