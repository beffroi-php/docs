---
title: Events
status: draft
description: Every event both packages dispatch, and what each one carries.
---

# Events

The core and the protocol dispatch PSR-14 events, and the bundle turns the ones that must leave the process
into messages. An event carries exactly what it is about: a domain object only when that object survives a
queue, and facts by identifier otherwise.

This page will list every event of both packages, what it carries, and whether it crosses a broker.
