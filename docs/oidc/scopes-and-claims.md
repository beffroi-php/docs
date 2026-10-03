---
title: Scopes and claims
status: draft
description: What a client may ask for, and what it is told.
---

# Scopes and claims

A scope is a request for claims, and `claims` asks for them one by one (OIDC Core §5.5). The provider gives
what the person agreed to, what the client is allowed, and what it actually holds, which is the intersection
and never the union.

This page will describe the standard scopes, the `claims` parameter, and where a claim is read from.
