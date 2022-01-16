---
title: "Journal des modifications"
description: "Journal des modifications."
lead: ""
date: 2022-01-07T22:19:51.911Z
lastmod: 2022-01-07T22:19:51.911Z
draft: false
images: []
menu: 
  docs:
    parent: "en-decouvrir-plus"
weight: 620
toc: true
---

## Problems updating npm packages

Delete the `./node_modules` folder, and run again:

```bash
npm install
```

## Problems with cache

Delete the temporary directories:

```bash
npm run clean
```
