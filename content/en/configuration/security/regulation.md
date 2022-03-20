---
title: "Regulation"
description: "RegulationConfiguration"
lead: "An introduction into configuring Authelia."
date: 2022-03-19T04:53:05+00:00
lastmod: 2022-03-19T04:53:05+00:00
draft: false
images: []
menu:
  configuration:
    parent: "security"
weight: 104300
toc: true
---


**Authelia** can temporarily ban accounts when there are too many
authentication attempts. This helps prevent brute-force attacks.

## Configuration

```yaml
regulation:
  max_retries: 3
  find_time: 2m
  ban_time: 5m
```

## Options

### max_retries

{{< confkey type="integer " default="3" required="no" >}}

The number of failed login attempts before a user may be banned. Setting this option to 0 disables regulation entirely.

### find_time

{{< confkey type="duration " default="2m" required="no" >}}

The period of time in [duration notation format](../prologue/common.md#duration-notation-format) analyzed for failed attempts. For
example if you set `max_retries` to 3 and `find_time` to `2m` this means the user must have 3 failed logins in
2 minutes.

### ban_time

{{< confkey type="duration" default="5m" required="no" >}}

The period of time in [duration notation format](../prologue/common.md#duration-notation-format) the user is banned for after meeting
the `max_retries` and `find_time` configuration. After this duration the account will be able to login again.