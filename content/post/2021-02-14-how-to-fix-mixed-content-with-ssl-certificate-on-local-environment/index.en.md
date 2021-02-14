---
title: How to Fix MIxed Content with SSL Certificate on Local Environment
author: Rob Wiederstein
date: '2021-02-14'
slug: []
categories:
  - SSL
tags:
  - https
lastmod: '2021-02-14T07:31:28-06:00'
keywords: []
description: ''
comment: no
toc: no
autoCollapseToc: no
postMetaInFooter: no
hiddenFromHomePage: no
contentCopyright: no
reward: no
mathjax: no
mathjaxEnableSingleDollar: no
mathjaxEnableAutoNumber: no
hideHeaderAndFooter: no
flowchartDiagrams:
  enable: no
  options: ''
sequenceDiagrams:
  enable: no
  options: ''
---

# Introduction

This article was extremely helpful in diagnosing the problem entitled, ["Fixing mixed content"](Fixing mixed content).

See [How to get HTTPS working on your local development environment in 5 minutes](How to get HTTPS working on your local development environment in 5 minutes).

# Download OpenSSL

Go to [OpenSSL](https://www.openssl.org) to create SSL certificate. OpenSSL is a software toolkit that must be downloaded. The software can be downloaded from their [website] or github.

After download, I then moved into the new directory `~/Downloads/openssl-3.0.0-alpha11`  and ran the following commands:

```bash
### Unix / Linux / macOS

    $ ./Configure
    $ make
    $ make test
    
```

Generate a RSA-2048 key and save it to a file rootCA.key.

```bash
openssl genrsa -des3 -out rootCA.key 2048
```

```bash
openssl req -x509 -new -nodes -key rootCA.key -sha256 -days 1024 -out rootCA.pem
```

# Add Certificate

On my MAC, I initially went to the `Applications>Utilities>Keychain Access.app>File>Import Items` but did not get a response after attempting to import the file `rootCA.pem`.  Out of frustration, I went back to the directory where I'd downloaded the application, found the file, and clicked on `rootCA.pem` and it opened a dialog.  The file was installed in the system's root directory. (I'm the only one that uses my laptop.)

## Create a new OpenSSL configuration file server.csr.cnf



