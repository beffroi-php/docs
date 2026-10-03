---
title: Personal data
status: draft
description: Sealed columns, blind indexes, and data keys that can be rewrapped live.
---

# Personal data

Personal data is sealed in its column with a data key of the tenant, itself wrapped by the key management
service, so a database alone reads nothing. The lookups that must still work use blind indexes rather than
a readable column.

The data keys can be rewrapped onto another key management client while the provider serves sign-ins, and
destroying them is the one operation that cannot be undone.

This page will describe what is sealed, what is indexed blind, the scopes a data key covers, and the
rewrapping.
