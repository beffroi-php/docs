---
title: Introspection and revocation
status: draft
description: Asking what a token is, and ending it. RFC 7662 and RFC 7009.
---

# Introspection and revocation

Introspection describes a token to the client it was issued to and to nobody else, as JSON or as a signed
JWT. Revocation ends a token and what depends on it, and it answers the same way whether the token existed or
not.

This page will describe both endpoints, who may call them, what introspection returns, and what a revocation
reaches.
