---
title: Keys
status: draft
description: The signing keys of a tenant: sealed, published, rotated without an outage.
---

# Keys

A tenant signs with keys it owns, each one sealed by a key management service: the application asks for an
operation and never holds the master key. A key has a status, a use and dates, and the JWK Set publishes the
ones a client may need, which includes a key staged for a rotation and a key still retiring.

A rotation is therefore not an outage: the new key is published before it is used, and the old one stays
published until nothing it signed can still be verified.

This page will describe the statuses, the rotation, the staging delay, and what `--compromised` does
differently.
