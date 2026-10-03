---
title: Request objects
status: draft
description: The authorization request, signed, RFC 9101.
---

# Request objects

A request object is the authorization request as a JWT the client signed, so the provider reads what the
client meant rather than what a browser passed along. A client registers the algorithm it will sign with,
and one that registered nothing is never read an unsigned object.

This page will describe the object, the algorithms, `request` against `request_uri`, and the rules about
what may differ between the object and the query.
