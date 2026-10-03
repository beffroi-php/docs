---
title: Resources
status: draft
description: The audience a client asks its token for, RFC 8707.
---

# Resources

A client names the resource it intends to call, and the token is issued for that audience rather than for
everything the client might reach. A resource server that receives a token addressed elsewhere refuses it.

This page will describe the parameter, what the issued token carries, and what happens when several
resources are named.
