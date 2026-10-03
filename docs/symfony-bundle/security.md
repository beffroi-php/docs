---
title: Security
status: draft
description: The firewalls, the authenticators, and what a session holds.
---

# Security

The bundle brings its own authenticators for the interaction plane and expects nothing of the host
application's security configuration beyond a firewall to put them on. The provider's session is its own: it
records what was proven, and it is not the host application's login session.

This page will describe the firewalls to declare, the authenticators, and the rate limits that apply.
