---
title: Users
status: draft
description: A person in the provider: their username, their claims, and the stable subject clients know them by.
---

# Users

A user belongs to a tenant, is named by a username unique within it, and is known to clients by a subject
identifier that never changes, even when the username or the email address does. The standard claims of
OIDC Core §5.1 are held beside the identity, each one as what it is rather than as a row in a bag of
strings.

This page will describe the identity, the claims that are set and the ones that are not, and the difference
between the two.
