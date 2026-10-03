---
title: Access tokens
status: draft
description: Either a signed JWT the resource server verifies, or a reference it introspects.
---

# Access tokens

An access token here is `at+jwt` (RFC 9068) or an opaque reference, per client, and never an ambiguous shape:
a resource server must know what it is validating. Both carry the same facts, and both can be bound to a key
or a certificate.

This page will describe the claims of an `at+jwt`, what introspection returns for a reference, and how the
format of a client is chosen.
