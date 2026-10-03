---
title: Credentials
status: draft
description: Several per person, each one a kind of its own, each one revocable on its own.
---

# Credentials

A person holds credentials, not a password: a password, a passkey, a TOTP secret and backup codes can exist
at the same time, and each one is a class of its own kind. A kind declares what it can do by the interfaces
it implements, so a credential that can be revoked and one that can prove a second factor are told apart by
their type and never by a `match` on a string.

Adding a kind is adding a class. This page will describe the model, and the four kinds below describe
themselves.
