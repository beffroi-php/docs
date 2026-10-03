---
title: Passwords
status: draft
description: Typed hashes, the algorithm named in the hash, and rehashing on the next sign-in.
---

# Passwords

A password is stored as a hash that says which algorithm produced it, so several algorithms coexist and a
hash made by an older one is replaced the next time the person signs in successfully. A new algorithm is a
class implementing the hasher interface of its capability, registered in the wiring.

This page will describe the shape of a stored hash, the algorithms available, and how a migration from
another provider's hashes is handled.
