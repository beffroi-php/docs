---
title: Authorization code
status: draft
description: The grant every browser flow ends with, RFC 6749 §4.1 and OIDC Core §3.1.
---

# Authorization code

A code is single use, short lived, bound to the client it was issued to, to the redirect URI it was asked
for and to the PKCE verifier that will be presented. Spending it yields the tokens the request asked for and
nothing more.

This page will describe the exchange, every check it runs, and what a replayed code does.
