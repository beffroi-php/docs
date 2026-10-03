---
title: Client authentication
status: draft
description: The methods a client may register, and the one it then uses.
---

# Client authentication

A client authenticates with the one method it registered and no other (RFC 6749 §2.3.1): a secret sent as
HTTP Basic or in the body, a JWT it signed with its own key (`private_key_jwt`, RFC 7523), a mutual TLS
certificate (RFC 8705), or nothing at all for a public client. A method is a class implementing the
interface of that capability, and what the provider announces is what is wired.

This page will describe each method, what it requires of a client, and what the provider checks.
