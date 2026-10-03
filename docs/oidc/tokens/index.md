---
title: Tokens
status: draft
description: What the provider issues, and in which shape.
---

# Tokens

Three kinds of token leave this provider, and a client never has to guess which it is holding: an
[access token](access-tokens.md) for a resource server, an [ID token](id-tokens.md) about the person, and a
[refresh token](refresh-tokens.md) to ask again. [Encryption](encryption.md) says what the provider encrypts
and for whom.

A token format is a class implementing the issuer interface of that format, so adding one is adding a class
and announcing it follows from wiring it.
