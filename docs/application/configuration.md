---
title: Configuration
status: draft
description: The environment the application reads.
---

# Configuration

Everything that varies by deployment is an environment variable: the issuer, the key management DSN, the
database, the broker, the lifetimes, the host that asks for a client certificate. Nothing secret is in a
file that is committed.

This page will list the variables and what each one decides.
