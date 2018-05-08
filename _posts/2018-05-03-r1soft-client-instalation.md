---
title: "How To: Install R1Soft Client on Ubuntu 16.04"
excerpt_separator: "<!--more-->"
categories:
  - How To
tags:
  - R1Soft
  - Client
  - Ubuntu
---


### Add the R1Soft Repo:

```
echo deb http://repo.r1soft.com/apt stable main >> /etc/apt/sources.list
```

### Add the proper key & update:

```
wget http://repo.r1soft.com/r1soft.asc
apt-key add r1soft.asc 
apt-get update
```

### Installation

```
apt-get install serverbackup-enterprise-agent 
```

#### Proceed to Server configuration and configure on Web interface.

### On the Client, get key from Server

```
serverbackup-setup --get-key http://<server ipaddress>
```


