---
title: Sender-constrained tokens
status: draft
description: A token useless to whoever does not hold its key.
---

# Sender-constrained tokens

A bearer token is worth whatever stealing it is worth. A sender-constrained token is bound to something the
client proves it holds on every call: a key with [DPoP](dpop.md), or a client certificate with
[mutual TLS](mutual-tls.md). The binding is carried in the token's confirmation claim, and a resource server
checks it.

A confirmation method is a class implementing the interface of that capability, which is why both methods
work on both shapes of access token.
