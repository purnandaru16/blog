---
layout: post
title: "Hybris Installation Guide"
date: 2019-12-11
---

Langkah-langkah installasi Hybris:

1. Pastikan sudah terinstall java di laptop dan dan LOCAL_PATH sudah diset
2. Bisa dicek lewat terminal ```java --version``` dan ```javac --version``` untuk cek installed java dan ```$echo JAVA_HOME``` untuk mengecek LOCAL_PATH
3. Ekstrak ```HYBRISCOMM6600P_3-70003031.ZIP```
4. Masuk ke /installer dan jalankan terminal ```./install.sh -r <recipe>```, gunakan recipe ```b2c_acc```
5. Masuk ke /hybris/bin/platform dan jalankan ```. ./setantenv.sh```
6. Jalankan ```ant all```
7. Start Hybris menggunakan ```./hybrisserver.sh``` atau ```./hybrisserver.sh debug``` jika ingin menggunakan mode debugging
8. Setelah server up, masuk ke ```https://localhost:9002/```  di browser
9. Initialize
