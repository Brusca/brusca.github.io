---
title: "How To: Validate Let's Encrypt Cert using IIS"
excerpt_separator: "<!--more-->"
categories:
  - How To
tags:
  - IIS
  - Let's Encrypt
  - SSL
  - Certificate
---


### Problem: Let's encrypt web validation using IIS doesn't work

Let's encrypt web validation is the easiest way to validate your SSL, but when your site is hosted on IIS, you can't access the URL like *http://www.yourdomain.com/.well-known/acme-challenge/ZxryhS93t0xIu-uR_K0kBL2a44zYOp6o0BddCkwBKkw*

In order to access this kind of URL, you have to add a web.config file inside **acme-challenge** directory:


### web.config

```
<?xml version="1.0" encoding="UTF-8"?>
<configuration>
    <system.webServer>
        <staticContent>
            <mimeMap fileExtension="." mimeType="text/plain" />
        </staticContent>
    </system.webServer>
</configuration>
```




References:
<br>[sslforfree.com](https://www.sslforfree.com/)
<br>[letsencrypt.org](https://letsencrypt.org/)
