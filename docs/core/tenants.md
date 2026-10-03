---
title: Tenants
status: draft
description: The unit everything belongs to: one issuer, one set of keys, one population.
---

# Tenants

A tenant is the unit of isolation: it owns an issuer, a set of signing keys, a population of users, and the
clients that may ask about them. Nothing crosses from one tenant to another, and a subject identifier is
only meaningful inside the one that minted it.

This page will describe what a tenant holds, what belongs to the configuration and what belongs to its row,
and the one command that reconciles them.
