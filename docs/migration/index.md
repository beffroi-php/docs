---
title: Migration
status: draft
description: What changes between versions, and what to do about it.
---

# Migration

This section holds one page per version that asks something of you, with the changes listed and the way to
make them.

There is nothing here yet: no version of Beffroi is released, so no version has to be migrated from. The
first page will appear with the first release that changes a public interface.

## What to expect

- **Until `1.0`**, a minor version may change the public API. What changes is listed here, with the reason
  and the replacement, before the version is published.
- **A migration page describes the version it belongs to**, read from the version selector at the top of the
  page. It never describes a version you are not reading.
- **A database change ships as a Doctrine migration**, never as a sentence telling you to run some SQL.
- **A removal is announced before it happens.** A deprecation in one minor version, the removal in the next
  major one.

## Coming from another provider

Importing the users of an existing provider, with their credentials where that is possible at all, is
planned and not implemented. It is written in [the SCIM](../scim/index.md) and federation work rather than
here, because an import that forces every person to reset their password is not a migration anybody accepts.
