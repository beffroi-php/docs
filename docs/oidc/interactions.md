---
title: Interactions
status: draft
description: What happens between the request and the answer.
---

# Interactions

An interaction is the part a person sees: signing in, proving a second factor, agreeing to what a client
asks. The request waits on it, identified rather than held in a session, so a person can finish it in
another tab and so a provider restricted to the protocol plane never serves it.

This page will describe the model, `prompt`, `max_age`, `acr_values`, and what a client learns of an
interaction that did not finish.
