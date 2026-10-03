---
title: Endpoints
description: Every route the bundle serves, its method, the plane it belongs to and the specification it answers.
---

# Endpoints

Paths are relative to the issuer, which is where the application imports the routes of the bundle. A
deployment whose issuer is `https://op.example.com` serves the token endpoint at
`https://op.example.com/token`.

Every route name carries its plane. `beffroi_protocol_*` is server to server, called by a client or a
resource server; `beffroi_interaction_*` is a browser, where a person reads a page and answers. The
`BEFFROI_PLANE` environment variable restricts a process to one plane, so an interaction never reaches a
machine that only serves the protocol, and the other way round.

## The protocol plane

| Method | Path | Route | Specification |
|---|---|---|---|
| `GET` | `/.well-known/openid-configuration` | `beffroi_protocol_discovery` | OIDC Discovery 1.0 §4 |
| `GET` | `/.well-known/oauth-authorization-server` | `beffroi_protocol_authorization_server_metadata` | RFC 8414 |
| `GET` | `/jwks` | `beffroi_protocol_jwks` | RFC 7517 |
| `POST` | `/token` | `beffroi_protocol_token` | RFC 6749 §3.2 |
| `GET` `POST` | `/userinfo` | `beffroi_protocol_userinfo` | OIDC Core §5.3 |
| `POST` | `/introspect` | `beffroi_protocol_introspection` | RFC 7662 |
| `POST` | `/revoke` | `beffroi_protocol_revocation` | RFC 7009 |
| `POST` | `/par` | `beffroi_protocol_pushed_authorization_request` | RFC 9126 |
| `POST` | `/device_authorization` | `beffroi_protocol_device_authorization` | RFC 8628 §3.1 |
| `POST` | `/backchannel_authentication` | `beffroi_protocol_backchannel_authentication` | CIBA Core §7 |
| `POST` | `/register` | `beffroi_protocol_client_registration` | RFC 7591 |
| `GET` | `/register/{client_id}` | `beffroi_protocol_client_configuration_read` | RFC 7592 §2.1 |
| `PUT` | `/register/{client_id}` | `beffroi_protocol_client_configuration_update` | RFC 7592 §2.2 |
| `DELETE` | `/register/{client_id}` | `beffroi_protocol_client_configuration_delete` | RFC 7592 §2.3 |

The endpoints a deployment actually announces are the ones it has wired. The discovery document is built
from what is wired, never from a list kept beside it, so a grant you did not enable is not advertised.

## The interaction plane

| Method | Path | Route | What it is |
|---|---|---|---|
| `GET` `POST` | `/authorize` | `beffroi_interaction_authorize` | The authorization endpoint, OIDC Core §3.1.2 |
| `GET` `POST` | `/login` | `beffroi_interaction_login` | Where a person proves who they are |
| `GET` `POST` | `/login/code` | `beffroi_interaction_login_code` | The second factor, when one is asked for |
| `POST` | `/login/passkey/options` | `beffroi_interaction_passkey_login_options` | The assertion options of a passkey ceremony |
| `POST` | `/login/passkey` | `beffroi_interaction_passkey_login` | The assertion itself |
| `GET` `POST` | `/consent` | `beffroi_interaction_consent` | What a client is asking for, and the answer |
| `GET` `POST` | `/logout` | `beffroi_interaction_logout` | RP-initiated logout, OIDC RP-Initiated Logout 1.0 |
| `GET` `POST` | `/device` | `beffroi_interaction_device` | Where the code shown by a device is confirmed, RFC 8628 §3.3 |
| `GET` | `/initiate-login` | `beffroi_interaction_initiate_login` | Third party initiated login, OIDC Core §4 |
| `POST` | `/locale` | `beffroi_interaction_locale` | The language a person chose for the pages |

### The account pages

A person reads what the provider holds of them, and takes it back, without an administrator.

| Method | Path | Route |
|---|---|---|
| `GET` | `/account` | `beffroi_interaction_account` |
| `GET` | `/account/profile` | `beffroi_interaction_account_profile` |
| `GET` `POST` | `/account/passkeys` | `beffroi_interaction_account_passkeys` |
| `GET` `POST` | `/account/two-factor` | `beffroi_interaction_account_two_factor` |
| `GET` | `/account/sessions` | `beffroi_interaction_account_sessions` |
| `GET` | `/account/consents` | `beffroi_interaction_account_consents` |
| `GET` `POST` | `/account/approvals` | `beffroi_interaction_account_approvals` |
| `GET` `POST` | `/account/notifications` | `beffroi_interaction_account_notifications` |

[:octicons-arrow-right-24: The account pages](../symfony-bundle/account.md)

### The scripts the pages load

Served by the bundle so a deployment has no build step to run for them.

| Method | Path | Route |
|---|---|---|
| `GET` | `/passkey.js` | `beffroi_interaction_passkey_script` |
| `GET` | `/push.js` | `beffroi_interaction_push_script` |
| `GET` | `/push-worker.js` | `beffroi_interaction_push_worker` |
