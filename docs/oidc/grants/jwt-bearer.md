---
title: JWT bearer
status: draft
description: An assertion from an issuer the tenant trusts, RFC 7523.
---

# JWT bearer

A client presents a JWT signed by an issuer the tenant has pinned, and gets a token in exchange. What the
tenant trusts is declared explicitly: an issuer, its keys, and what it is allowed to assert.

This page will describe the trusted issuers, what is checked of an assertion, and what it may obtain.
