---
title: Configuration
status: draft
description: The tree under `beffroi`, section by section.
---

# Configuration

The configuration is one tree, built from a class per section, validated when the container is built rather
than when a request arrives. A section a deployment leaves out is a feature it does not serve: a tenant with
no `client_registration` has no registration endpoint, in its discovery document as on the wire.

This page will describe each section and what it decides. The exhaustive tree is in
[the reference](../reference/configuration.md).
