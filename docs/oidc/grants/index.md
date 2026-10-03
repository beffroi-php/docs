---
title: Grants
status: draft
description: The seven ways a token is obtained here.
---

# Grants

A grant is a class implementing the grant interface, tagged in the wiring; the token endpoint holds no
`match` on a grant type, and the discovery document announces exactly the grants that are tagged. What a
grant can do is declared by the interfaces it implements: whether it sends a person to the client, whether
it issues refresh tokens, whether it acts for the client itself, whether it exchanges a token.

| Grant type | Page |
|---|---|
| `authorization_code` | [Authorization code](authorization-code.md) |
| `refresh_token` | [Refresh token](refresh-token.md) |
| `client_credentials` | [Client credentials](client-credentials.md) |
| `urn:ietf:params:oauth:grant-type:device_code` | [Device code](device-code.md) |
| `urn:openid:params:grant-type:ciba` | [Backchannel authentication](backchannel-authentication.md) |
| `urn:ietf:params:oauth:grant-type:token-exchange` | [Token exchange](token-exchange.md) |
| `urn:ietf:params:oauth:grant-type:jwt-bearer` | [JWT bearer](jwt-bearer.md) |

The resource owner password credentials grant is not in that list and never will be.
