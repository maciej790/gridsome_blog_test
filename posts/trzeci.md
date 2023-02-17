---
excerpt: aaaa
path: /archived
summary: Archived Post Example - Just add is_archived true to your markdown post.
thumbnail: ./archived.png
date: 2021-10-18
is_archived: true
title: Archived aaaa
tags:
  - archived
categories:
  - archived
sidebar: Alternative
---

## How to Archive Post

To archive a post add `is_archived: true` to your markdown post. This will add div block
on top of the archived post with title and text. To change the default archive title and text add following
key to the .env file

```dotenv
ARCHIVE_TITLE='ARCHIVED POST'
ARCHIVE_TEXT='This Post is outdated.'
```
