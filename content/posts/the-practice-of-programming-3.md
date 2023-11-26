---
title: "The PoP : Part 3 - Design & Implementation and Interfaces"
date: 2020-07-10T03:11:33+05:30
draft: false
summary: "Summary of The Practice Of Programming. Part 3 : Design & Implementation and Interfaces"
truncated: true
backtotop:  true
description: "Summary of The Practice Of Programming. Part 3 : Design & Implementation and Interfaces"
weight: 1
aliases: []
categories: 
- "Book Summaries"

tags:
- pop

---


---

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

- Simple
- General
- Regular
- Predictable
- Robust
- Must adapt gracefully as its users and its implementation change.

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
valid input.
Don't say that a parameter is too large; report the valid range of values.

---
