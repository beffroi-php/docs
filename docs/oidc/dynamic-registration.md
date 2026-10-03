---
title: Dynamic registration
status: draft
description: A client the provider has never seen, RFC 7591 and RFC 7592.
---

# Dynamic registration

Registration is served when the tenant says so, and the tenant decides the mode: who may register, what an
initial access token buys, and whether an authority it pinned may vouch for a piece of software this provider
never issued. A registered client then reads, replaces and deletes itself at the URI it was handed (RFC
7592).

This page will describe the modes, the initial access tokens, the software statements, and what is refused.
