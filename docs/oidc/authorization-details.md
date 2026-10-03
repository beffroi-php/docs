---
title: Authorization details
status: draft
description: Asking for something a scope cannot express, RFC 9396.
---

# Authorization details

`authorization_details` is how a client asks for an authorization a scope cannot describe: an amount, an
account, a document, a named action. The provider validates each detail against the types it supports, shows
the person what is being asked, and puts what was granted in the token.

This page will describe the types, the validation, and what the consent page shows of them.
