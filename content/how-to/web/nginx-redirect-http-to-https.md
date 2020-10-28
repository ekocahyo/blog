+++
title = "Nginx Redirect Http to Https"
date = 2020-10-28T08:55:55+07:00
tags = ["web"]
categories = ["How to"]
draft = false
+++

## Redirect all site (HTTP) to HTTPS
Semua server block yang ada pada nginx akan di arahkan ke https termasuk localhost. Buat 1 block config pada folder /etc/nginx/conf.d/http-to-http.conf. Isinya seperti ini:
```
server {
    listen 80 default_server;
    server_name _;
    return 301 https://$host$request_uri;
}
```

## Redirect specific site (HTTP) to HTTPS
Jika butuh untuk site tertentu. Maka tambahkan di block config yang ingin di redirect seperti ini:
```
server {
    listen 80;
    server_name domain.tld;
    return 301 https://domain.tld$request_uri;
}
```