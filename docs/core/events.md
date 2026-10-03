---
title: The events of the core
status: draft
description: What the core announces, and what each event carries.
---

# The events of the core

The core dispatches PSR-14 events and nothing else: it knows no bus and no broker. An event is built where
it is raised, its constructor takes exactly what it carries, and it carries a domain object only when that
object survives the queue it may be written to, facts by identifier otherwise.

This page will list the events and what each one holds. The full list for both packages is in
[the reference](../reference/events.md).
