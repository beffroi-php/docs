---
title: DPoP
status: draft
description: A proof signed by the client on every request, RFC 9449.
---

# DPoP

The client signs a proof with a key it holds, the provider binds the token to the thumbprint of that key, and
a resource server refuses the token to anybody who cannot sign a matching proof. It works for a public
client, which is what makes it the useful one for a mobile or browser application.

This page will describe the proof, the nonce, the replay window, and what a resource server must check.
