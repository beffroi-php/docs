---
title: Passkeys
status: draft
description: WebAuthn enrolment and assertion, and what a passkey lets a relying party require.
---

# Passkeys

A passkey is a WebAuthn credential (W3C Web Authentication Level 3), enrolled from the account pages and
usable on its own, with no password in the way. It is what lets a client require a stronger authentication
with `acr_values`, and what the provider answers `acr` with once it has been used.

This page will describe enrolment, assertion, what is checked of an attestation, and the FIDO metadata the
check reads.
