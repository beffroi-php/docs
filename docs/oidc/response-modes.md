---
title: Response modes
status: draft
description: How the answer travels back: query, form post, or a signed JWT.
---

# Response modes

The response mode decides how the authorization response reaches the client: in the query, in a
self-submitting form (`form_post`), or as a signed and optionally encrypted JWT (JARM). A signed response is
what lets a client prove the answer came from this provider and was not rewritten.

This page will describe each mode, what a cross-site POST does to a session cookie, and what JARM carries.
