---
title: "Translations"
description: "Information on contributing translations to the Authelia project."
lead: "Authelia has translations for many using facing areas of the web portal. Contributing to these translations is a very easy process."
date: 2022-03-19T04:53:05+00:00
lastmod: 2022-03-19T04:53:05+00:00
draft: false
images: []
menu:
  contributing:
    parent: "prologue"
weight: 130
toc: true
---

The way the translation process is facilitated is via [Crowdin]. We encourage members of the community to
[join the Authelia Crowdin project](https://crwd.in/authelia) and help translate their preferred language.

## New Langauges

If the language you wish to translate is not on [Crowdin] then you have a few options:

1. Ask for the language to be added via the [Crowdin] interface.
2. Ask a maintainer to add it via one of the [contact options](../../information/contact.md).
3. Make a pull request directly on GitHub modifying the translation files within
[this directory](https://github.com/authelia/authelia/tree/master/internal/server/locales).

## Overrides

Users can override translations easily locally using the [assets](../configuration/server.md#locales) directory. This is
useful if you wish to perform a translation and see if it looks correct in the browser.

[Crowdin]: https://crowdin.com/project/authelia