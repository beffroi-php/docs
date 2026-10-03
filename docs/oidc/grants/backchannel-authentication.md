---
title: Backchannel authentication
status: draft
description: CIBA: the device that asks is not the one that answers.
---

# Backchannel authentication

In CIBA (CIBA Core 1.0) the client asks the provider to reach a person it names, and the person answers on
their own device. The client then polls, or is pinged, and the two FAPI-CIBA profiles are what judge this
implementation.

This page will describe the request, the hints that name a person, the poll and ping modes, and how the
person is actually reached.
