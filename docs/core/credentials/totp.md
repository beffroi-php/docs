---
title: TOTP
status: draft
description: A time-based one-time password as a second factor, RFC 6238.
---

# TOTP

A TOTP secret (RFC 6238, on the HOTP construction of RFC 4226) is a second factor a person enrols from the
account pages with a QR code, and is asked for when the policy or the client requires one.

This page will describe enrolment, the window accepted, replay, and revocation.
