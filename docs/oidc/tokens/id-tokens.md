---
title: ID tokens
status: draft
description: What the provider says about the person, OIDC Core §2.
---

# ID tokens

An ID token is a statement about an authentication, addressed to one client: who the person is, when they
proved it, how, and with which provider. It is signed, it may be encrypted, and it is never a credential for
an API.

This page will describe the claims, what `nonce`, `auth_time`, `acr` and `amr` carry, and the algorithms a
client may register.
