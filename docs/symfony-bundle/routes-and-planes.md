---
title: Routes and planes
status: draft
description: The two planes, and restricting a process to one.
---

# Routes and planes

Every route of the bundle carries its plane in its name: `beffroi_protocol_*` for what a client or a resource
server calls, `beffroi_interaction_*` for what a browser reads. `BEFFROI_PLANE` restricts a process to one of
them, so a provider can serve the protocol on machines a browser never reaches.

This page will describe the import, the planes, and what a request to the wrong plane gets.
[The endpoints](../reference/endpoints.md) lists every route.
