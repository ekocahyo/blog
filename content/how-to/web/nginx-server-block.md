+++
title = "Nginx Server Block"
date = 2020-10-28T10:44:20+07:00
tags = ["web"]
categories = ["How to"]
draft = false
+++

## Single server block
Dalam 1 server hanya ada 1 website:
```
server {
  listen 80;
  server_name _;
  access_log logs/access.log main;
  root /path/to/site;
}
```
## Multiple server block
Dalam 1 server ada beberapa website:
```
server {
  listen 80;
  server_name domain1.tld;
  access_log logs/domain1.access.log main;
  root /path/to/domain1;
}
server {
  listen 80;
  server_name domain2.tld;
  access_log logs/domain2.access.log main;
  root /path/to/domain2;
}
server {
  listen 80;
  server_name domain3.tld;
  access_log logs/domain3.access.log main;
  root /path/to/domain3;
}
```