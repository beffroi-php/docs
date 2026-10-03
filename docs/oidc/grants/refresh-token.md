---
title: Refresh token
status: draft
description: Renewing without a person, RFC 6749 §6.
---

# Refresh token

A refresh token renews an access token without the person being there, which is why it is the one the rules
are strictest about: it has a lifetime and an absolute lifetime, it keeps the authentication snapshot of the
session that created it, and spending it may replace it.

This page will describe rotation, reuse detection, what a revocation takes with it, and what `offline_access`
changes.
