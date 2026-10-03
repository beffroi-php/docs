---
title: Web push
status: draft
description: Reaching a person on a browser they signed in with, RFC 8030.
---

# Web push

A deployment that names a push subject lets the tenant draw an application server key and reach a person
through the push service of a browser they signed in with, which is how a decoupled request can be confirmed
without a second application. Nothing in a notification names the request it is about.

This page will describe the subscription, the encryption, what a notification carries, and what a `410` from
a push service does.
