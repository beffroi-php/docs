---
title: Discovery and JWKS
status: draft
description: The two documents a client reads before anything else.
---

# Discovery and JWKS

`/.well-known/openid-configuration` (OIDC Discovery 1.0) and `/.well-known/oauth-authorization-server`
(RFC 8414) describe the provider, and `/jwks` publishes the keys a client needs to verify what it receives.
Both documents are derived from what is wired: a grant, a client authentication method or an algorithm
appears there because it exists, never because somebody added a line.

This page will describe every field published, what is cacheable, and what changes during a key rotation.
