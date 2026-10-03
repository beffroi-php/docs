---
title: Encryption
status: draft
description: What the provider encrypts, and for whom.
---

# Encryption

A client may register that it wants its ID token, its UserInfo response or its authorization response
encrypted, with the algorithms it supports and the key it publishes. The provider then encrypts for that
client and for nobody else, and announces only what it can actually do.

This page will describe the registration, the algorithms, where the keys come from, and what fails when a
key set cannot be read.
