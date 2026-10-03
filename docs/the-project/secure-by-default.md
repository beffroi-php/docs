---
title: Secure by default
description: The protections Beffroi applies with no option to turn them off, and the few exceptions, each one named and bounded.
---

# Secure by default

A provider that can be configured insecurely will be, and the person who pays for it is never the one who
wrote the option. So Beffroi has no option to do it wrong: the protections below are properties of the
code. There is no `insecure_` setting, no compatibility mode, and no global switch.

## What is always on

| Rule | Why |
|---|---|
| PKCE is mandatory, `S256` only | `plain` protects nothing against an attacker who reads the request. A code intercepted without the verifier is useless |
| No implicit flow | Tokens in a URL fragment end up in history, logs and referrers |
| No resource owner password credentials grant | It teaches applications to collect passwords, which is the habit the protocol exists to break |
| Redirect URIs are compared exactly | Prefix and wildcard matching is how an open redirector becomes a token leak |
| `iss` is in every authorization response | A client must be able to tell which provider answered. RFC 9207 |
| Access tokens are `at+jwt` or opaque references, never an ambiguous shape | A resource server must know what it is validating. RFC 9068 |
| No redirect is followed outbound | Fetching a client's metadata or keys must not become a request to an address the client chose |
| No boolean from a third party is ever cast | A missing claim and a false claim are not the same thing, and `(bool)` makes them one |
| Every secret string comes from a cryptographic source, every secret comparison is constant time | |

## Where an exception exists

An exception is named, bounded and written down, never a switch in a configuration file. Two examples of
the shape they take:

- **PKCE can be waived by the registration policy**, not by the client. A tenant that must serve a client
  which cannot do PKCE says so in its own policy, for that client, and the waiver is visible where clients
  are read.
- **Dynamic client registration is controlled.** The endpoint exists, and the tenant decides the mode it
  runs in: who may register, what an initial access token buys, and which authority may vouch for a piece
  of software it did not issue.

## Keys and personal data

Signing keys and the data keys that protect personal data are held by a key management service, never by
the application: the application asks for an operation and never holds the master key. Keys rotate
without a restart and without breaking a token already in flight.

Personal data is sealed in its column, with blind indexes for the lookups that must still work. A dump of
the database is searched byte by byte by a test that fails when it finds a value it should not, and the
same search finds a value the schema declares readable, so a green run is a search that was looking.

[:octicons-arrow-right-24: Keys](../core/keys.md) and [personal data](../core/personal-data.md).
