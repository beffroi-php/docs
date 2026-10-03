---
title: Mutual TLS
status: draft
description: Client certificates, for authentication and for binding, RFC 8705.
---

# Mutual TLS

A client authenticates with a certificate, and the token it receives is bound to that certificate's
thumbprint. The provider reads the certificate the TLS listener actually validated, from the edge to PHP, and
refuses one carried in a header by whoever felt like adding it.

This page will describe both halves of RFC 8705, the endpoint aliases a provider announces for them, and how
the certificate reaches the application.
