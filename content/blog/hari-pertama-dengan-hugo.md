+++
title = "Hari Pertama Dengan Hugo"
date = 2020-05-06T11:23:44+07:00
tags = [
    "story",
    "other",
]
categories = [
    "Story",
]
draft = false
menu = "main"
+++

## Hello World!

Mungkin kata tersebut yang harus saya ucapkan pertamakali, seperti yang lainnya ketika berhasil menjalankan sesuatu (contoh xampp/apache). Ini pertama kalinya saya mencoba membuat blog dengan menggunakan generator web static dengan bahasa Go (Go lang). Awalnya saya coba menggunakan generator web static miliknya jekyll tapi selalu gagal dan saya rasa sulit untuk mempelajari bahasa rubby.

## Intro Hugo
Pertama kali saya coba Hugo, saya langsung di bikin jatuh hati. Salah satu yang bikin saya menyukainya adalah, ketika running servernya, dan saya ada edit content, tanpa perlu refresh browser, content sudah berubah sendiri. So easy, so clean, so fast. Jadi buat yang belum tahu tentang Hugo, coba saya share pandangan saya tentang hugo.

Menurut bang [Wiki](https://en.wikipedia.org/wiki/Hugo_(software)), Hugo adalah suatu generator web static yang di kembangkan dengan menggunakan bahasa Go. Hugo ini ternyata dibuat sama bang [Steve Francia](https://spf13.com/) pada tahun 2013. Silahkan yang mau ikutan mengucapkan terima kasih terhadap beliau. Hugo ini memiliki lisensi opensource. Jadi sama bang Steve di share itu coding nya. Sehingga tidak perlu bayar buat ngembangin atau pun cuma pakai. Buat yang ingin langsung mempelajari nya bisa mulai dari [sini](https://gohugo.io/getting-started/quick-start/) ya.

## Hosting to github

Di hari yang sama juga, saya baru tahu kalau github bisa di jadiin hosting blog. Ya meskipun hanya mendukung static web saja, itu lebih dari cukup menurut saya. Kan memang ini temanya static web. Jadi Hugo ini memiliki folder khusus hasil generate file static web nya. Nama foldernya `public`. Oh iya, hampir lupa. Hugo ini cara kita menulis content dengan bahasa Markdown(format file .md) bukan bahasa Go. Jadi kita tulis dalam file dengan format `.md`, lalu di generate sama Hugo hasilnya keluar di folder `public` dalam bentuk `.html`.

Kita lanjutin pembahasan ke hosting di github. Jadi yang akan kita taruh di github nantinya hanya folder public yang sudah di generate sama Hugo nya. Jadi pertama kalian harus punya akun github dulu pastinya. berikutnya bikin repository dengan format <em>username</em>.github.io. Kalian ganti usernamenya sesuai username kalian ya. Lalu folder public tadi kalian taruh deh ke repository tadi. Dan selamat, blog kalian sudah jadi.

## Summary
Open Source tidak lah buruk. Justru opensource bisa membuat wawasan kita menjadi lebih luas lagi. Intinya tetap membaca, tetap belajar, dan ketika sudah mahir, jangan lupa ikutan berkontribusi. Berbagi itu indah. Contoh nya dengan adanya hugo dan github, kita bisa ikutan merasakan mudah nya membuat blog yang gratis. Sudah ringan, gratis, simple, idaman sekali.
