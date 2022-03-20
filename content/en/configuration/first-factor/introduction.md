---
title: "First Factor"
description: "Configuring Duo"
lead: "Authelia uses a username and password for a first factor method. This section describes configuring this."
date: 2022-03-19T04:53:05+00:00
lastmod: 2022-03-19T04:53:05+00:00
draft: false
images: []
menu:
  configuration:
    parent: "first-factor"
weight: 102100
toc: true
---

There are two ways to store the users along with their password:

* [LDAP](ldap.md): users are stored in remote servers like OpenLDAP, OpenDJ, OpenAM, FreeIPA, or Microsoft Active
  Directory.
* [File](file.md): users are stored in YAML file with a hashed version of their password.

## Configuration

```yaml
authentication_backend:
  disable_reset_password: false
  file: {}
  ldap: {}
```

## Options

### disable_reset_password

{{< confkey type="boolean" default="false" required="no" >}}

This setting controls if users can reset their password from the web frontend or not.

### file

The [file](file.md) authentication provider.

### ldap

The [LDAP](ldap.md) authentication provider.