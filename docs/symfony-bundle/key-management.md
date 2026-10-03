---
title: Key management
status: draft
description: The client the private keys are sealed with.
---

# Key management

The bundle seals private keys with a client of `symfony/key-management`, named in the configuration and
declared where that component is configured. Which provider it talks to, and whether there are several, is a
decision of the deployment and not of the bundle.

This page will describe the clients available, what each one needs, and how to move from one to another.
