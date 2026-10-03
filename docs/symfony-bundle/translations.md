---
title: Translations
status: draft
description: Every string translated, and the locale read from the request.
---

# Translations

Every user-facing string is in XLIFF, in the `beffroi` domain, with intl-icu for plurals and parameters. The
locale of an interaction comes from `ui_locales` when the client sent one, then from `Accept-Language`, and
never from the URL.

This page will describe the domains, the locales shipped, how to add one, and how a person changes theirs.
