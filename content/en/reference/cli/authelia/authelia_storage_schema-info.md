---
title: "authelia storage schema-info"
description: "Reference for the authelia storage schema-info command."
lead: ""
date: 2022-05-31T11:13:56+10:00
lastmod: 2022-06-02T23:28:13+10:00
draft: false
images: []
menu:
  reference:
    parent: "cli-authelia"
weight: 130
toc: true
---

## authelia storage schema-info

Show the storage information

```
authelia storage schema-info [flags]
```

### Options

```
  -h, --help   help for schema-info
```

### Options inherited from parent commands

```
  -c, --config strings                         configuration files to load (default [configuration.yml])
      --encryption-key string                  the storage encryption key to use
      --mysql.database string                  the MySQL database name (default "authelia")
      --mysql.host string                      the MySQL hostname
      --mysql.password string                  the MySQL password
      --mysql.port int                         the MySQL port (default 3306)
      --mysql.username string                  the MySQL username (default "authelia")
      --postgres.database string               the PostgreSQL database name (default "authelia")
      --postgres.host string                   the PostgreSQL hostname
      --postgres.password string               the PostgreSQL password
      --postgres.port int                      the PostgreSQL port (default 5432)
      --postgres.schema string                 the PostgreSQL schema name (default "public")
      --postgres.ssl.certificate string        the PostgreSQL ssl certificate file location
      --postgres.ssl.key string                the PostgreSQL ssl key file location
      --postgres.ssl.mode string               the PostgreSQL ssl mode (default "disable")
      --postgres.ssl.root_certificate string   the PostgreSQL ssl root certificate file location
      --postgres.username string               the PostgreSQL username (default "authelia")
      --sqlite.path string                     the SQLite database path
```

### SEE ALSO

* [authelia storage](authelia_storage.md)	 - Manage the Authelia storage

###### Auto generated by spf13/cobra on 2-Jun-2022