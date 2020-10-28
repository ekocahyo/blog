+++
title = "Step by Step Create Content on Hugo"
date = 2020-10-28T11:28:28+07:00
tags = ["hugo"]
categories = ["how to"]
draft = false
+++

## Buat file MarkDown (MD)
Buat file baru dengan format .md pada direktori content. 
```
hugo new how-to/hugo/step-by-step-create-content-on-hugo.md
```

## Tulis konten
Tulis artikel pada file yang barusan di buat. Lokasinya di sini 
```
content/how-to/hugo/step-by-step-create-content-on-hugo.md
```

## Preview
Untuk liat hasilnya dulu sebelum di publish / generate, pakai perintah ini: 
```
hugo serve
```

## Generate html file
Jika sudah oke, generate file html nya dengan perintah ini: 
```
hugo
```
hasilnya akan masuk pada direktori `public`

## Upload ke github
Sedikit tips dari saya pribadi, project hugo dengan public (html file) saya pisah dan saya jadikan 2 repo. Karena direktori public akan saya taruh langsung ke repo ekocahyo.github.io. Sedangkan repo hugo akan saya pisah sendiri sehingga tidak ikut masuk ke repo ekocahyo.github.io. Jadi saya bikin repo ekocahyo.github.io sebagai submodule nya repo hugo. Step by step uploadnya seperti ini.

### Push ke repo ekocahyo.github.io
```
cd public
git add .
git commit -m “pesan perubahan”
git push origin master
```

### Push ke repo hugo
```
cd ..
git submodule update
git add .
git commit -m “pesan perubahan”
git push
```

## Summary
Semua langkah di atas sebenernya bisa dijadikan 1 script shell script dan bisa di jalan kan dalam 1 langkah saja. Tapi terkadang dasar seperti ini perlu di catat karena suatu saat akan membutuhkannya lagi.