---
title: Authorization request
status: draft
description: What is read, what is refused, and what goes back.
---

# Authorization request

The authorization endpoint reads the request, finds the client, compares the redirect URI exactly, requires
PKCE with `S256`, and decides whether a person has to be shown a page at all. Every response carries `iss`
(RFC 9207), so a client can tell which provider answered it.

This page will describe each parameter, the order the checks run in, and which errors go back to the client
rather than to the person.
