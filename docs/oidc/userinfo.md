---
title: UserInfo
status: draft
description: What a client reads about the person, OIDC Core §5.3.
---

# UserInfo

UserInfo answers the claims the access token allows, for the person it was issued for, as JSON or as a signed
and optionally encrypted JWT. It is the one endpoint where the answer depends on the token and on the consent
behind it rather than on the request.

This page will describe the request, the claims returned, and the signed and encrypted responses.
