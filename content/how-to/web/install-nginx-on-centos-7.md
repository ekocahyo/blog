+++
title = "Install Nginx on Centos 7"
date = 2020-06-05T22:11:50+07:00
tags = ["web"]
categories = ["How to"]
draft = false
+++

## Install Nginx
#### Install dari repo epel
`yum install -y epel-repo && yum install -y nginx`
#### Install dari official repo nginx
```
cat << EOF > /etc/yum.repos.d/nginx.repo
[nginx-stable]
name=nginx stable repobaseurl=http://nginx.org/packages/centos/$releasever/$basearch/
gpgcheck=1
enabled=1
gpgkey=https://nginx.org/keys/nginx_signing.key
module_hotfixes=true
EOF && yum install -y nginx
```
reference: [*repo nginx*](http://nginx.org/en/linux_packages.html#RHEL-CentOS)

## Manajemen service nginx
- Testing nginx config:
`nginx -t`
- Memulai nginx:
`systemctl start nginx`
- Menghentikan nginx:
`systemctl stop nginx`
- Memuat ulang nginx
`systemctl restart nginx`
- Load konfigurasi file nginx:
`systemctl reload nginx`
- Mengaktifkan secara otomatis layanan nginx saat booting:
`systemctl enable nginx`
- Nonaktifkan Nginx untuk memulai otomatis saat boot:
`systemctl disable nginx`

## Struktur file konfigurasi nginx
```
/
├─ etc/
│  ├─ nginx.conf
│  ├─ conf.d/
│  │  ├─ domain.conf
├─ var/
│  ├─ log/
│  │  ├─ nginx/
│  │  │  ├─ access.log
│  │  │  ├─ error.log
├─ usr/
│  ├─ share/
│  │  ├─ nginx/
│  │  │  ├─ html/
│  │  │  │  ├─ index.html
```