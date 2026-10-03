---
title: Pushed authorization requests
status: draft
description: The request sent server to server first, RFC 9126.
---

# Pushed authorization requests

The client pushes its authorization request to the provider, authenticating itself, and receives a
`request_uri` the browser then carries. Nothing of the request travels in a URL, and the provider knows the
request was not tampered with on the way.

This page will describe the endpoint, the lifetime of a `request_uri`, and what a tenant may require.
