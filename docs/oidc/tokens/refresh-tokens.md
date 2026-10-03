---
title: Refresh tokens
status: draft
description: What is stored, what is rotated, and what a revocation reaches.
---

# Refresh tokens

A refresh token is the longest lived thing the provider issues, so it is the one with the most rules: a
lifetime and an absolute lifetime, the authentication snapshot of the session it came from, and a chain that
a reuse breaks.

This page will describe storage, rotation, reuse, and what revoking one takes with it.
