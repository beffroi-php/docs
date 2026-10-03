---
title: Clients
status: draft
description: What a client is, where it came from, and what it registered.
---

# Clients

A client is an application the provider answers, identified by a `client_id`, holding the redirect URIs it
may be sent back to, the methods it authenticates with and the metadata it registered. A client declared by
the configuration and a client that registered itself are the same object with a different source, and the
source is visible wherever clients are read.

This page will describe the model, every piece of metadata a client may hold, and what the provider refuses
at registration time rather than at request time.
