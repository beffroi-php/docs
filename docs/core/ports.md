---
title: The ports of the core
status: draft
description: The interfaces the outside implements, one capability each.
---

# The ports of the core

The core asks the outside for what it cannot do itself: repositories, a clock, a source of randomness, a
password hasher, a key management client. Each port has one to five methods, so a caller sees what it calls
and nothing more, and what an implementation may throw is written in the contract.

This page will list the ports, what each one is for, and which implementations ship in the bridge.
