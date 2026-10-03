---
title: Device code
status: draft
description: A device with no browser and no keyboard, RFC 8628.
---

# Device code

The device asks for a code, shows it to the person, and polls while they confirm it in a browser somewhere
else. The provider answers `authorization_pending` and `slow_down` as the specification requires, and the
confirmation page is part of the interaction plane.

This page will describe both endpoints, the polling rules, and the lifetime of a device code.
