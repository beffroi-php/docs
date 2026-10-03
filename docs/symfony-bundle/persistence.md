---
title: Persistence
status: draft
description: The Doctrine mapping, the migrations, and the DBAL types.
---

# Persistence

The model is mapped with XML, outside the entities, and a value object a column holds whole goes in one
column with a DBAL type of the bundle that reads it back through the object's own constructor. There is no
embeddable fixing one type per field for the whole model, which is what lets the same kind of value be sealed
in one table and readable in another.

This page will describe the schema, the migrations, the types, and what a sealed column changes about a
query.
