---
title: "The PoP : Part 4 - Debugging"
date: 2020-07-11T03:11:33+05:30
draft: false
summary: "Summary of The Practice Of Programming. Part 4 : Debugging"
truncated: true
backtotop:  true
description: "Summary of The Practice Of Programming. Part 4 : Debugging"
weight: 1
aliases: []
categories: ["pop"]
---
---

## Debugging

### Key Takeaways

The reality is that there will always be errors that we find by testing and eliminate by debugging.

Every bug you find can teach you how to prevent a similar bug from happening again or to recognize it if it does.

Techniques that help reduce debugging time
- include good design
- good style
- boundary condition tests
- assertions and sanity
- checks in the code
- defensive programming
- well-designed interfaces
- limited global data
- checking tools

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

Display output to localize your search

Write self-checking code

After a bug is fixed, don't throw check away. Leave it in the source, commented
out or controlled by a debugging option, so that it can be turned on again when the
next difficult problem appears.
If they're not expensive, it might be wise to leave them always enabled.

Draw a picture. Sometimes pictures are more effective than text for testing and
debugging. Scatter plots display misplaced values more effectively
than columns of numbers. A histogram of data reveals anomalies in

Keep records

---;
