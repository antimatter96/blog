---
title: "The PoP : Part 5 - Testing"
date: 2020-07-12T03:11:33+05:30
draft: false
summary: "Summary of The Practice Of Programming. Part 5 : Testing"
truncated: true
backtotop:  true
description: "Summary of The Practice Of Programming. Part 5  : Testing"
weight: 1
aliases: []
categories: 
- "Book Summaries"
tags:
- pop

---


---

## Testing

Test as You Write the Code

The earlier a problem is found, the better.

Test code at its boundaries.

Test pre- and post-conditions.

### Program defensively

A useful technique is to add code to handle "can't happen" cases:

Situations where it is not logically possible for something to happen but (because of some failure elsewhere) it might anyway.

### Check error returns

** Never throw away a test ** : It can help you decide whether a bug report is valid or describes something already fixed.

Keep a record of bugs, changes, and fixes; it will help you identify old problems and fix new ones

Systematic Testing

Test incrementally.

Test simple parts first.

Know what output to expect

Test Automation

Automate regression testing.

---
