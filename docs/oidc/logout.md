---
title: Logout
status: draft
description: Ending a session, and telling the others.
---

# Logout

Three specifications, and they are not interchangeable: RP-initiated logout is a client asking for a session
to end, front-channel logout tells the other clients through the browser, and back-channel logout tells them
server to server with a signed logout token. A provider that implements only the first one has not logged
anybody out of anywhere else.

This page will describe each one, what a client registers for it, and what a logout can and cannot promise.
