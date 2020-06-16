---
title: "The Practice Of Programming"
date: 2020-03-11T03:11:33+05:30
draft: false
summary: "Summary of The Practice Of Programming by Rob Pike"
truncated: true
backtotop:  true
---


I read the book **The Practice of Programming**

### Basic Principles of Good Software

- Simplicity : *keeping programs short and manageable*
- Clarity : *making sure they are easy to understand, for people as well as machines*
- Generality *they work well in a broad range of situations and adapt well as new situations arise*

## Style

### Purpose of Style

> Make the code easy to read for yourself and others

### Rules Regarding

#### Naming

A variable or a function name labels an object, conveys information about its purpose.

Why Bother ?
> Naming conventions make it easier to understand your own code. as well as code
> written by others. They also make it easier to invent new names as the code is being
> written. The longer the program, the more important is the choice of good. descriptive,
> systematic names

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

#### Expressions and Statements

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

#### Consistency and Idioms

Consistency leads to better programs.

any variation suggests a genuine difference, one worth noting.

Use a consistent indentation and brace style

specific style is much less important than its consistent application. Pick one style,
preferably ours, use it consistently, and don't waste time arguing.

IF you work on a program you didn't write, preserve the style you find
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

#### Function Macros

->>

#### Magic Numbers

Magic numbers are the constants, array sizes, character positions, conversion factors,
and other literal numeric values that appear in programs.

#### Give names to magic numbers

A raw number in program source gives no indication of its importance or derivation, making the program harder to understand and modify

By giving names to the principal numbers in any calculation, we can make the
code easier to follow, and change

#### Use character constants, not integers**

#### Comments

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

Weel-written code is easier to read and to understand, almost
surely has fewer errors, and is likely to be smaller than code that has been carelessly
tossed together and never polished.
In the rush to get programs out the door to meet some deadline, it's easy to push style aside, to worry about it later.
Sloppy code is bad code-not just awkward and hard to read, but often broken.

The key observation is that good style should be a matter of habit. If you think
about style as you write code originally, and if you take the time to revise and
improve it, you will develop good habits. Once they become automatic, your subconscious
will take care of many of the details for you, and even the code you produce
under pressure will be better.

------------------------

## Algorithms & Data Structures

There are several steps to choosing an algorithm

First, assess potential algorithms and data structures

Consider how much data the program is likely to process.

If the problem involves modest amounts of data, choose simple techniques; if the data
could grow, eliminate designs that will not scale up to large inputs

Then, use a library or language feature if you can
Failing that, write or borrow a short, simple, easy to understand implementation

Try it
If measurements prove it to be too slow, only then should you upgrade to a more advanced technique.

------------------------

## Design & Implementation

As a rule, try to handle irregularities and exceptions and special cases in data.
Code is harder to get right so the control flow should be as simple and regular as possible

It's hard to design a program completely and then build it
constructing real programs involves iteration and experimentation
The act of building forces one to clarify decisions that had previously been glossed over.
As much as possible, start with something simple and evolve it as experience dictates

## Interfaces

Among the issues to be worked out in a design of an interface are

Interfaces: what services and access are provided? The interface is in effect a
contract between supplier and customer. The desire is to provide services that
are uniform and convenient, with enough functionality to be easy to use but not
so much as to become unwieldy.

Information hiding: what information is visible and what is private? An interface
must provide straightforward access to the components while hiding details
of the implementation so they can be changed without affecting users.

Resource management: who is responsible for managing memory and other
limited resources? Here, the main problems are allocating and freeing storage.
and managing shared copies of information.

Error handling: who detects errors. who reports them, and how? When an error
is detected, what recovery is attempted?

### Principles

simple, general. regular,
predictable, robust-and it must adapt gracefully as its users and its implementation change.

### Key Takeaways

Hide implementation details.
Avoid global variables;
wherever possible it is better to pass references to all data
through function arguments

Choose a small orthogonal set of primitives

Narrow interfaces are to be preferred to wide ones, at least until one has strong
evidence that more functions are needed. Do one thing, and do it well. Don't add to
an interface just because it's possible to do so, and don't fix the interface when it's the
implementation that's broken

Do the same thing the same way everywhere

Resource Management
Write code that is reentrant, which means
that it works regardless of the number of simultaneous executions

ERROR DETECTION

Detect errors at a low level, handle them at a high level.
As a general principle,
errors should be detected at as low a level as possible, but handled at a high level. In
most cases, the caller should determine how to handle an error, not the callee.

Use exceptions only for exceptional situations.
Exceptions should not be used for handling
expected return values eg EOF, 500, 200

Defensive programming, that is, making sure that a program is invulnerable to bad
input, is important both for protecting users against themselves and also as a security
mechanism.

The text of error messages, prompts, and dialog boxes should state the form of
valid input. Don't say that a parameter is too large; report the valid range of values.

------------------------

## Debugging

### Key Takeaways

The reality is that there will always be errors that we find by testing and eliminate by debugging.

 Every bug you find can teach you how to prevent a similar bug from happening again or to recognize it if it does.

Techniques that help reduce debugging time
include good design, good style, boundary condition tests, assertions and sanity
checks in the code, defensive programming, well-designed interfaces, limited global
data, and checking tools

On the opposite side of the coin, some features are prone to error, like
goto statements, global variables, unrestricted pointers, and automatic type conversions.

Clicking over statements takes longer than scanning the output of
judiciously-placed displays. It takes less time to decide where to put print statements
than to single-step to the critical section of code, even assuming we know where that
is.

More important, debugging statements stay with the program; debugger sessions
are transient.

Blind probing with a debugger is not likely to be productive. It is more helpful to
use the debugger to discover the state of the program when it fails, then think about
how the failure could have happened.

Examine the evidence in the erroneous output and try to infer how it could have been
produced. Look at any debugging output before the crash; if possible get a stack trace
from a debugger. Now you know something of what happened, and where. Pause to
reflect. How could that happen? Reason back from the state of the crashed program
to determine what could have caused this.

Debugging involves backwards reasoning, like solving murder mysteries. Something
impossible occurred, and the only solid information is that it really did occur.
So we must think backwards from the result to discover the reasons. Once we have a
full explanation, we'll know what to fix and, along the way, likely discover a few
other things we hadn't expected.

Look for familiar patterns

Examine the most recent change

Don't make the same mistake twice
Look for  identical errors
Easy code can have bugs if its familiarity causes us to let down our guard. Even
when code is so simple you could write it in your sleep, don't fall asleep while writing
it.

Debug it now, not later.

Read before typing.

Take a break for a while; sometimes what you see in the source code is what you
meant rather than what you wrote, and an interval away from it can soften your misconceptions
and help the code speak for itself when you return.
Resist the urge to start typing; thinking is a worthwhile alternative.
Explain your code to someone else. Another effective technique is to explain

Make the bug reproducible

Study the numerology of failures

Display output to localize your search. If

Write self-checking code

After a bug is fixed, don't throw check away. Leave it in the source, commented
out or controlled by a debugging option, so that it can be turned on again when the
next difficult problem appears.
If they're not expensive, it might be wise to leave them always enabled.

Draw a picture. Sometimes pictures are more effective than text for testing and
debugging. Scatter plots display misplaced values more effectively
than columns of numbers. A histogram of data reveals anomalies in

Keep records

------------------------

## Testing

Test as You Write the Code
The earlier a problem is found, the better.

Test code at its boundaries.

Test pre- and post-conditions.

Program defensively. A useful technique is to add code to handle "can't happen"
cases, situations where it is not logically possible for something to happen but
(because of some failure elsewhere) it might anyway.

Check error returns

Never throw away a test. It can help you decide whether a bug report is valid or
describes something already fixed. Keep a record of bugs, changes, and fixes; it will
help you identify old problems and fix new ones

Systematic Testing

Test incrementally.

Test simple parts first.

Know what output to expect

Test Automation

Automate regression testing.

------------------------

## Performance
