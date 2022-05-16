---
title: "BookStack"
description: "Integrating BookStack with Authelia via OpenID Connect."
lead: ""
date: 2022-03-19T04:53:05+00:00
lastmod: 2022-03-19T04:53:05+00:00
draft: false
images: []
menu:
  integration:
    parent: "openid-connect"
weight: 420
toc: true
---

{{< alert icon="⚠️" context="danger" >}}
This documentation is maintained by the community, it is not guaranteed to be complete or up-to-date. If you find an
error with this documentation please either make a pull request or start a GitHub Discussion.
{{< /alert >}}

## Tested Versions

- Authelia: v4.33.2
- BookStack: 20.10

## Before You Begin

You are required to utilize a unique client id and a unique and random client secret for all [OpenID Connect] relying
parties. You should not use the client secret in this example, you should randomly generate one yourself. You may also
choose to utilize a different client id, it's completely up to you.

This example makes the following assumptions:

- **Application Root URL:** `https://bookstack.example.com`
- **Authelia Root URL:** `https://auth.example.com`
- **Client ID:** `bookstack`
- **Client Secret:** `bookstack_client_secret`

## Configuration

### Application

To configure [BookStack] to utilize Authelia as an [OpenID Connect] Provider:

1. Edit your .env file
2. Set the following values:
   1. AUTH_METHOD: `oidc`
   2. OIDC_NAME: `Authelia`
   3. OIDC_DISPLAY_NAME_CLAIMS: `name`
   4. OIDC_CLIENT_ID: `bookstack`
   5. OIDC_CLIENT_SECRET: `bookstack_client_secret`
   6. OIDC_ISSUER: `https://auth.example.com`
   7. OIDC_ISSUER_DISCOVER: `true`

### Authelia

The following YAML configuration is an example **Authelia**
[client configuration](../../../configuration/identity-providers/open-id-connect.md#clients) for use with [BookStack]
which will operate with the above example:

```yaml
- id: bookstack
  secret: bookstack_client_secret
  public: false
  authorization_policy: two_factor
  scopes:
    - openid
    - profile
    - email
  redirect_uris:
    - https://bookstack.example.com/oidc/callback
  userinfo_signing_algorithm: none
```

## See Also

- [BookStack OpenID Connect Documentation](https://www.bookstackapp.com/docs/admin/oidc-auth/)

[BookStack]: https://www.bookstackapp.com/
[OpenID Connect]: ../../openid-connect/introduction.md