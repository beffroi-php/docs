---
title: Token exchange
status: draft
description: Acting for somebody else, RFC 8693.
---

# Token exchange

Token exchange is how a gateway acts on behalf of a service, or a service on behalf of a person, without
either of them handing over their own token. The result names the subject and the actor, and a resource
server can tell them apart.

This page will describe the parameters, delegation against impersonation, and what the issued token claims.
