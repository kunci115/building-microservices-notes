# building-microservices-notes(bahasa indonesia)
building-microservices-summary sam newman

Apa itu Microservices ?
 - Microservices itu servis kecil yang bekerja bersama di masing2 engine
 - konsep microservices itu dynamic tergantung kebutuhan masing2

**Bab 1. Beberapa Karakteristik Yang Biasanya ada pada microservices**
  1. **Technology Heterogeneity**
    Simplenya heterogen ini setiap services bisa mempunyai teknologi yang berbeda
        contoh: Facebook mempunyai object engine seperti post status, friends relation sama penyimpanan gambar(pictures)
                - untuk Post status menggunakan teknologi Ruby yang bisa mudah adaptasi dengan documentstore
                - untuk Friends relation bisa menggunakan golang yang dikombinasikan dengan graphdb agar keterkaitan antar orang dapat terlihat dengan baik
                - dan untuk penyimpanan gambar(pictures) menggunakan java karena bisa memanfatkan database blob storenya
    jadi dengan microservices kita bisa adaptasi teknologi dengan cepat.

  2. **Resilence**
    Konsep resilence engineering yang dimaksud adalah ketika satu service mati, maka tidak akan mengganggu fungsionalitas dari servis yang lain

  3. **Scaling**
    Konsep Scaling ini biasanya dibutuhkan ketika request pada suatu service melebihi kapasitas dari instance service tersebut
     contoh: Posts service tiba2 banayk request yang masuk karena sedang ada event tertentu. maka service apps tersebut dapat menyesuaikan dan di up lagi kapasitas requestnya.

  4. **Ease Of Deployment**
    Konsep ease of deployment itu lahir dari monolithic apps yang jika kodenya diubah untuk deployment kita butuh waktu berkali2 memastikan tidak akan menggangu       fungsi yang lain, nah dengan konsep microservice seharusnya ini bisa diatasi karena kode yang terdapat dalam repository hanya akan berpengaruh pada service       itu    sendiri.

  5. **Organizational Alignment**
    Karakteristik ini biasanya untuk memudahkan pembentukan team pada sebuah apps, jadi orgnasasi dapat mengalokasikan resource programmer terhadap arsitektur appsnya(ini akan berkaitan dengan Consway's Law yang akan kita bahas nanti)
    
  6. **Composability**
    Dalam Service oriented architecture kelebihanya kita bisa reuse fungsi2 yang bisa digunakan untuk tujuan berbeda.
  
  7. **Optimizing For Replaceability**
    Karakteristik ini adalah merepresentasikan bahwa suatu service harus mudah untuk di rewrite, kalau monolith kan kita akan panik sendiri karena terlalu             kompleks, nah ini kebalikanya.
    
**Bab 2. The Evolutionary Architect**
