+++
title = "Install Apache on Centos 7"
date = 2020-06-05T22:11:50+07:00
tags = ["web"]
categories = ["How to"]
draft = false
+++

## Install apache
`yum install -y httpd`

## Manajemen service apache
- Testing apache config:
`httpd -t`
- Memulai apache:
`systemctl start apache`
- Menghentikan apache:
`systemctl stop apache`
- Memuat ulang apache
`systemctl restart apache`
- Load konfigurasi file apache:
`systemctl reload apache`
- Mengaktifkan secara otomatis layanan apache saat booting:
`systemctl enable apache`
- Nonaktifkan apache untuk memulai otomatis saat boot:
`systemctl disable apache`

## Struktur file konfigurasi apache
```
/
├─ etc/
│  ├─ conf/
│  │  ├─ httpd.conf
│  ├─ conf.d/
│  │  ├─ domain.conf
│  ├─ conf.modules.d/
│  │  ├─ ssl.conf
├─ var/
│  ├─ log/
│  │  ├─ apache/
│  │  │  ├─ access.log
│  │  │  ├─ error.log
│  ├─ www/
│  │  ├─ html/
│  │  │  ├─ index.html
```