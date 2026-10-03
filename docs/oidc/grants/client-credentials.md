---
title: Client credentials
status: draft
description: A service asking for itself, RFC 6749 §4.4.
---

# Client credentials

There is no person in this grant: a confidential client asks for a token for itself, for the resource it
named. No ID token is issued, no consent is involved, and no refresh token is given, because the client can
simply ask again.

This page will describe what the token carries, and what a resource server reads of it.
