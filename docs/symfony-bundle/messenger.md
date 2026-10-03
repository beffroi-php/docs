---
title: Messenger
status: draft
description: Which writes are asynchronous, and which the protocol waits for.
---

# Messenger

No write is synchronous unless the protocol needs its result in the same request, and every exception is
listed in the Messenger configuration with the reason it is one. Messages are commands, queries, events or
explicitly synchronous messages, and a handler calls a use case rather than holding logic of its own.

This page will describe the transports, the queues, what runs where, and what happens when the broker is
down.
