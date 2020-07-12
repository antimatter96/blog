---
title: "The Practice Of Programming : Part 1 - Style"
date: 2020-07-01T03:11:33+05:30
draft: false
summary: "Summary of The Practice Of Programming. Part 1 : Style"
truncated: false
backtotop:  true
---
---

I read the book **The Practice of Programming**

### Basic Principles of Good Software

- Simplicity : *keeping programs short and manageable*
- Clarity : *making sure they are easy to understand, for people as well as machines*
- Generality : *they work well in a broad range of situations and adapt well as new situations arise*

## Style

### Purpose of Style

> Make the code easy to read for yourself and others

Rules Regarding

### Naming

A variable or a function name labels an object, conveys information about its purpose.

***Why Bother?***

- Naming conventions make it easier to understand your own code as well as code written by others.
- They also make it easier to invent new names as the code is being written

The longer the program, the more important is the choice of good. descriptive, systematic names

**tl;dr:**

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

### Expressions and Statements

- Write the clearest code that does the job

- Indent to show structure

- Use the natural form for expressions

- Conditional expressions that include negations are always hard to understand

- Parenthesize to resolve ambiguity

- Grouping the operands of higher-precedence operators helps the reader to see the structure more quickly.

- Break up complex expressions.

Be clear. Programmers' endless creative energy is sometimes used to write the most
concise code possible, or to find clever ways to achieve a result. Sometimes these
skills are misapplied, though, since the goal is to write clear code, not clever code.

The `? : ` operator is fine for short expressions where it can replace four lines of if-else

Clarity is not the same as brevity. Often the clearer code will be shorter, but it can also be longer

The proper criterion is ease of understanding.

Be careful with side effects.

### Consistency and Idioms

Consistency leads to better programs.

Any variation suggests a genuine difference, one worth noting.

Use a consistent indentation and brace style

specific style is much less important than its consistent application. Pick one style,
preferably ours, use it consistently, and don't waste time arguing.

If you work on a program you didn't write, preserve the style you find
there. When you make a change, don't use your own style even though you prefer it.
The program's consistency is more important than your own, because it makes life
easier for those who follow.

Use idioms for consistency

Braces
Indentation should be idiomatic, too.
iteration

Sprawling layouts also force code onto multiple screens or pages, and thus detract
from readability.

Use else-ifs for multi-way decisions.

Trailing else parts may be omitted if there is no action for the
default, although leaving it in with an error message may help to catch conditions that
"can't happen."

Attempts to re-use pieces of code often lead to tightly knotted programs:

Cases should almost always end with a break, with the rare exceptions commented

The increase in size is more than offset by the increase in clarity

### Function Macros

->> Can have side-effectss

### Magic Numbers

Magic numbers are the constants, array sizes, character positions, conversion factors,
and other literal numeric values that appear in programs.

#### Give names to magic numbers

A raw number in program source gives no indication of its importance or derivation, making the program harder to understand and modify

By giving names to the principal numbers in any calculation, we can make the
code easier to follow, and change

#### Use character constants, not integers**

### Comments

Comments are meant to help the reader of a program. They do not help by saying
things the code already plainly says, or by contradicting the code, or by distracting the
reader with elaborate typographical displays. The best comments aid the understanding
of a program by briefly pointing out salient details or by providing a lager-scale
view of the proceedings.

Don't belabor the obvious

Comments should add something that is not immediately evident from the code,
or collect into one place information that is spread through the source.

Comment functions and global data.

Don't comment bad code, rewrite it.
Comment anything unusual or potentially confusing, but when the comment outweighs the code, the code probably needs fixing.

Don't contradict the code
When you change code, make sure the comments are still accurate
comment should say so, and the code should do so

Clarify, don't confuse. Comments are supposed to help readers over the hard parts,
not create more obstacles.

Sometimes code is genuinely difficult, perhaps because the algorithm is complicated
or the data structures are intricate. In that case, a comment that points to a
source of understanding can aid the reader. It may also be valuable to suggest why
particular decisions were made

------------------------

Well-written code is easier to read and to understand, almost
surely has fewer errors, and is likely to be smaller than code that has been carelessly
tossed together and never polished.


In the rush to get programs out the door to meet some deadline, it's easy to push style aside, to worry about it later.
Sloppy code is bad code-not just awkward and hard to read, but often broken.

The key observation is that good style should be a matter of habit. If you think
about style as you write code originally, and if you take the time to revise and
improve it, you will develop good habits.

Once they become automatic, your subconscious
will take care of many of the details for you, and even the code you produce
under pressure will be better.

------------------------
