# 📇 Wuxian World — Players (Data Karakter Awal)

> **Modul:** players — dirujuk lewat `INDEX.md` §3, HANYA dipakai saat karakter yang namanya terdaftar di sini dimainkan untuk **pertama kali**.
> **⚠️ SIFAT FILE: READ-ONLY MUTLAK BAGI AI.** Ini murni referensi **data awal** karakter — bukan sistem save, bukan checkpoint, bukan status terkini. AI tidak pernah menulis, mengedit, atau menyarankan perubahan pada file ini. Hanya **admin (Inggoxxx)** yang berhak mengubah isinya, langsung di GitHub, di luar sesi roleplay.
> **Rujukan silang:** `00_CORE_RULES_AI_GM.md` §1.6 & §1.10, `09_CULTIVATION_LAW_SYSTEM.md` (Law Origin), `10_ECONOMY_SYSTEM.md` (Item Origin & mata uang)

---

## 0. Aturan Pemakaian (WAJIB DIPAHAMI AI)

1. File ini **hanya** berisi kondisi karakter **sebelum cerita dimulai**. Bukan status "terakhir dimainkan", bukan save slot, bukan progres yang sedang berjalan.
2. AI membaca file ini **satu kali saja** — persis di momen karakter yang namanya ada di sini mulai dimainkan untuk **pertama kalinya**. Sejak saat itu, seluruh perkembangan karakter (HP berubah, Qi terpakai, item baru, breakthrough, pindah lokasi, dst.) **hanya** dicatat di dalam blok "Profil Karakter" pada percakapan yang sedang berjalan (format resmi ada di `00_CORE_RULES_AI_GM.md` §2) — **tidak pernah** ditulis balik ke file ini.
3. AI **dilarang keras**: menulis ke file ini, menyarankan pemain "menyimpan"/"update" progres ke file ini, atau memperlakukan isi file ini sebagai kondisi karakter yang **terkini** setelah roleplay berjalan.
4. Untuk **melanjutkan** karakter yang sudah pernah dimainkan sebelumnya (bukan memulai baru), pemain menempelkan ulang blok "Profil Karakter" **terakhir** dari sesi sebelumnya di pesan pembuka. File ini **tidak dipakai** untuk kasus itu — isinya tetap/statis, tidak mengikuti progres apa pun.
5. Hanya admin yang menambah/mengubah isi file ini secara langsung di GitHub. AI hanya boleh membaca — tidak pernah menulis, tidak pernah "menyarankan" perubahan, dalam bentuk apa pun.

---

## 1. Daftar Karakter Terdaftar

| Nama | Lokasi Awal | Realm Awal | Sekte/Afiliasi Awal |
|---|---|---|---|
| Jiang Ziling *(contoh)* | Desa Xingcun, Central Plains | Foundation Establishment, Menengah | Dojo Bunga Aprikot |
| Tji An Coek | Pondok Tabib Gunung, Azure Mountain Range | Mortal Foundation, Awal | Sanxiu (tanpa sekte) |
| Nox | Desa Xingcun, Central Plains | Mortal Foundation, Awal | Sanxiu (tanpa sekte) |
| Ghi | Desa Qingshui, Central Plains | Mortal Foundation, Awal | Sanxiu (tanpa sekte) |
| Tatsuya / Yin Zheng | Kota Luoyang Kecil, Central Plains | Mortal Foundation, Awal | Sanxiu (tanpa sekte) |
| Wang Zixiin | Desa Luoye, Central Plains | Mortal Foundation, Awal | Sanxiu (tanpa sekte) |
| Ying Luo | Desa Qingfeng, Azure Mountain Range | Mortal Foundation, Awal | Sanxiu (tanpa sekte) |
| 神Nēru | Desa Tiedao, Central Plains | Mortal Foundation, Awal | Sanxiu (tanpa sekte) |
| Lu Qingxuan | Desa Xingcun, Central Plains | Mortal Foundation, Awal | Sanxiu (tanpa sekte) |
| Paijo | Kota Luoyang Kecil, Central Plains | Mortal Foundation, Awal | Sanxiu (tanpa sekte) |

*(Admin menambah baris baru di sini setiap kali mendaftarkan karakter baru di §4.)*

---

## 2. Skema Field (Penjelasan Singkat)

| Field | Isi |
|---|---|
| **Lokasi Awal** | Nama lokasi persis sesuai modul `01`–`07` |
| **Realm & Stage Awal** + **Qi Cap** | Sesuai `09_CULTIVATION_LAW_SYSTEM.md` §2 — `QiCap = RealmBase × StageMultiplier` |
| **Hukum Kultivasi Awal** + **Law Origin** | Kalau karakter sudah punya Hukum sejak cerita dimulai, wajib sertakan asal-usulnya (Guru/Manual/Pencerahan) sesuai `09` §3.0 |
| **Sekte/Afiliasi Awal** | Nama sekte + peran, atau "Sanxiu (tanpa sekte)" |
| **Kondisi Awal** | HP/Qi/Stamina/Satiety/Karma **di titik cerita dimulai** — nilai tetap, bukan yang di-update |
| **Currency Awal** | Kepemilikan mata uang saat cerita dimulai |
| **Equipment Awal** | Item yang sedang TERPAKAI/digenggam sejak cerita dimulai (senjata, zirah, aksesoris) — beda dari Inventory yang cuma dibawa. Lihat `00_CORE_RULES_AI_GM.md` §2 |
| **Inventory Awal** | Item yang dibawa tapi TIDAK sedang terpakai saat cerita dimulai |
| **Teknik Awal** | Harus konsisten dengan Law Origin |
| **Latar Belakang & Kepribadian** | Bio singkat: sifat, motivasi, relasi NPC yang relevan — fakta lore tetap, bukan log yang terus bertambah |

---

## 3. Template Kosong (Untuk Admin — Salin untuk Mendaftarkan Karakter Baru)

```
### 👤 [Nama Karakter]

**Lokasi Awal:** [nama lokasi, sesuai modul 01–07]
**Realm & Stage Awal:** [Realm, Stage] — Qi Cap: [angka]
**Hukum Kultivasi Awal:** [nama Hukum, atau "Belum ada — akan ditentukan lewat roleplay"]
**Law Origin (jika sudah ada Hukum):** Jalur [Guru/Manual/Pencerahan] — [detail singkat]
**Sekte/Afiliasi Awal:** [nama sekte + peran, atau "Sanxiu"]

**Kondisi Awal:** HP X/Y · Qi X/Y · Stamina X/100 · Satiety X% · Kondisi Normal · Karma Netral

**Currency Awal:** [rincian per denominasi]

**Equipment Awal (terpakai/digenggam):**
- Senjata: [nama item — Tier/Grade, asal singkat, atau "Tidak ada"]
- Zirah/Pelindung: [nama item, atau "Tidak ada"]
- Aksesoris: [nama item, atau "Tidak ada"]

**Inventory Awal (dibawa, tidak terpakai):**
- [Item 1 — Tier/Grade, asal singkat]
- [Item 2]

**Teknik Awal:**
- [teknik — sumber]

**Latar Belakang & Kepribadian:**
[1–2 paragraf: siapa dia, sifatnya, motivasinya, relasi penting dengan NPC kanon jika ada]
```

---

## 4. Detail Karakter

### 👤 Jiang Ziling *(CONTOH — admin bisa hapus/ganti dengan karakter sungguhan)*

**Lokasi Awal:** Desa Xingcun, Central Plains *(lihat `02_CENTRAL_PLAINS.md`)*
**Realm & Stage Awal:** Foundation Establishment (Pembentukan Fondasi), Menengah — Qi Cap: 750 *(500 × 1,5, RealmBase v3.0 — lihat `09_CULTIVATION_LAW_SYSTEM.md` §9)*
**Hukum Kultivasi Awal:** Dao Abadi (varian pedang ringan, gaya Dojo Bunga Aprikot)
**Law Origin:** Jalur Guru — diajarkan oleh **Guru Li Xingchun**, Kepala Dojo Bunga Aprikot, sejak usia 14 tahun. Teknik yang sudah dikuasai: *Jurus Pedang Bunga Gugur* (tingkat dasar).
**Sekte/Afiliasi Awal:** Dojo Bunga Aprikot (Desa Xingcun) — murid biasa, belum murid inti

**Kondisi Awal:** HP 300/300 · Qi 750/750 · Stamina 100/100 · Satiety 70% · Kondisi Normal · Karma Netral (belum ada catatan Merit/Sin)

**Currency Awal:**
- Tael Tembaga × 340
- Tael Perak × 28
- Tael Emas × 2

**Equipment Awal (terpakai/digenggam):**
- Senjata: Pedang Besi Standar — Tier 1, Huang-Grade, dibeli di Kota Luoyang Kecil
- Zirah/Pelindung: Jubah Katun Desa — Tier 1, Fan-Grade, bawaan dari desa (perlindungan minim, sekadar pakaian)
- Aksesoris: Tidak ada

**Inventory Awal (dibawa, tidak terpakai):**
- Pil Pemulih Qi Ringan × 3 — Tier 2, hadiah dari Guru Li Xingchun
- Buku Catatan Mendiang Ayah — non-tradeable, berisi catatan ramuan yang belum dipahami sepenuhnya

**Teknik Awal:**
- *Jurus Pedang Bunga Gugur* (dasar) — dari Guru Li Xingchun
- Meditasi Dasar Pemurnian Qi — teknik umum non-sekte

**Latar Belakang & Kepribadian:**
Jiang Ziling tumbuh di Desa Xingcun, menjadi yatim setelah ayahnya meninggal karena wabah semasa ia kecil. Diterima sebagai murid Dojo Bunga Aprikot oleh Guru Li Xingchun sejak usia 14 tahun, ia berlatih tekun hingga mencapai Foundation Establishment — pencapaian yang cukup jarang untuk dojo sekecil itu. Ia punya rivalitas ringan yang bersahabat dengan **Murid Senior Ah Jian**, yang gemar menantangnya duel iseng untuk pamer. Ziling menyimpan buku catatan mendiang ayahnya yang berisi petunjuk soal ramuan penyembuh yang belum sepenuhnya ia pahami — misteri yang diam-diam ingin ia pecahkan. Tujuannya: membuktikan Dojo Bunga Aprikot bukan sekte remeh, terinspirasi kisah alumni dojo yang jadi legenda jianghu. Ia menghormati **Kepala Desa Wu Lao** sebagai tetua desa yang bijaksana.

---

### 👤 Tji An Coek

**Lokasi Awal:** Pondok Tabib Gunung, Azure Mountain Range *(lihat `03_AZURE_MOUNTAIN_RANGE.md`)*
**Realm & Stage Awal:** Mortal Foundation (Fondasi Fana), Awal — Qi Cap: 0 *(RealmBase v3.0 — lihat `09_CULTIVATION_LAW_SYSTEM.md` §9)*
**Hukum Kultivasi Awal:** Belum ada — akan ditentukan lewat roleplay
**Law Origin (jika sudah ada Hukum):** Belum ada
**Sekte/Afiliasi Awal:** Sanxiu (tanpa sekte)

**Kondisi Awal:** HP 100/100 · Qi 0/0 · Stamina 100/100 · Satiety 100% · Kondisi Normal · Karma Netral

**Currency Awal:**
- Tael Tembaga × 50

**Equipment Awal (terpakai/digenggam):**
- Senjata: Pisau Pemotong Herba — Fan-Grade, perkakas biasa pemotong tanaman obat
- Zirah/Pelindung: Pakaian Katun Gunung — Fan-Grade, pakaian sederhana pengembara gunung
- Aksesoris: Tidak ada

**Inventory Awal (dibawa, tidak terpakai):**
- Kantong Herba Ringan — berisi beberapa tanaman obat biasa (non-spiritual)
- Bekal Makanan Sederhana × 2

**Teknik Awal:**
- Pengetahuan Obat Dasar — pemahaman medis non-kultivasi dari asuhan tabib

**Latar Belakang & Kepribadian:**
Seorang anak raja yang diculik sejak bayi dan dibesarkan oleh seorang tabib tua di pegunungan sunyi. Tumbuh dewasa tanpa mengetahui asal-usul darah bangsawan yang mengalir di tubuhnya, ia diajarkan cara meracik obat herbal dan mengenali tanaman obat oleh ayah angkatnya. Meskipun memiliki latar belakang tersembunyi, Tji An Coek memulai perjalanannya dari titik nol sebagai orang biasa tanpa basis kultivasi. Ia memiliki sifat tenang, rendah hati, dan berempati pada penderitaan orang lain, namun siap menjelajahi Jianghu untuk mencari jati dirinya.

---

### 👤 Nox

**Lokasi Awal:** Desa Xingcun, Central Plains *(lihat `02_CENTRAL_PLAINS.md`)*
**Realm & Stage Awal:** Mortal Foundation (Fondasi Fana), Awal — Qi Cap: 0 *(RealmBase v3.0 — lihat `09_CULTIVATION_LAW_SYSTEM.md` §9)*
**Hukum Kultivasi Awal:** Belum ada — akan ditentukan lewat roleplay
**Law Origin (jika sudah ada Hukum):** Belum ada
**Sekte/Afiliasi Awal:** Sanxiu (tanpa sekte)

**Kondisi Awal:** HP 100/100 · Qi 0/0 · Stamina 100/100 · Satiety 100% · Kondisi Normal · Karma Netral

**Currency Awal:**
- Tael Tembaga × 30

**Equipment Awal (terpakai/digenggam):**
- Senjata: Tidak ada
- Zirah/Pelindung: Pakaian Aneh Kusam — Fan-Grade, pakaian sisa dunia masa depan yang sudah kusam dan disesuaikan
- Aksesoris: Tidak ada

**Inventory Awal (dibawa, tidak terpakai):**
- Bekal Makanan Sederhana × 2
- Kantong Air Kulit × 1

**Teknik Awal:**
- Tidak ada

**Latar Belakang & Kepribadian:**
Seorang manusia dari masa depan yang terlempar secara misterius ke dunia kultivasi Jianghu. Tanpa ingatan masa lalu selain nama "Nox", ia terbangun di lingkungan yang asing dan sama sekali berbeda dengan dunia asal yang ia lupakan. Tanpa basis kultivasi maupun pemahaman tentang energi Qi, Nox tidak memiliki tujuan megah selain bertahan hidup hari demi hari di tengah kerasnya dunia baru ini. Sifatnya cenderung pragmatis, waspada, dan serba mengamati, berusaha memahami aturan dunia kultivator secara bertahap dari titik terendah.

---

### 👤 Ghi

**Lokasi Awal:** Desa Qingshui, Central Plains *(lihat `02_CENTRAL_PLAINS.md`)*
**Realm & Stage Awal:** Mortal Foundation (Fondasi Fana), Awal — Qi Cap: 0 *(RealmBase v3.0 — lihat `09_CULTIVATION_LAW_SYSTEM.md` §9)*
**Hukum Kultivasi Awal:** Belum ada — akan ditentukan lewat roleplay
**Law Origin (jika sudah ada Hukum):** Belum ada
**Sekte/Afiliasi Awal:** Sanxiu (tanpa sekte)

**Kondisi Awal:** HP 100/100 · Qi 0/0 · Stamina 100/100 · Satiety 100% · Kondisi Normal · Karma Netral

**Currency Awal:**
- Tael Tembaga × 50

**Equipment Awal (terpakai/digenggam):**
- Senjata: Tongkat Bambu Kasar — Fan-Grade, alat bantu jalan dan pertahanan diri sederhana
- Zirah/Pelindung: Baju Katun Desa — Fan-Grade, pakaian warga desa biasa
- Aksesoris: Tidak ada

**Inventory Awal (dibawa, tidak terpakai):**
- Bekal Makanan Sederhana × 2
- Kantong Air Kulit × 1

**Teknik Awal:**
- Tidak ada

**Latar Belakang & Kepribadian:**
Lahir sebagai manusia biasa dengan akar spiritual yang rata-rata, Ghi tumbuh dengan satu dorongan utama: ketakutan akan kematian dan keinginan kuat untuk hidup abadi. Ambisinya tidak berawal dari dendam atau kekuasaan, melainkan hasrat murni untuk bertahan hidup lebih lama hingga menjadi seorang Immortal Emperor. Memulai petualangan tanpa dukungan sekte maupun teknik warisan, Ghi bertindak dengan penuh perhitungan, gigih, dan pantang menyerah meski harus merintis segalanya dari nol.

---

### 👤 Tatsuya / Yin Zheng

**Lokasi Awal:** Kota Luoyang Kecil, Central Plains *(lihat `02_CENTRAL_PLAINS.md`)*
**Realm & Stage Awal:** Mortal Foundation (Fondasi Fana), Awal — Qi Cap: 0 *(RealmBase v3.0 — lihat `09_CULTIVATION_LAW_SYSTEM.md` §9)*
**Hukum Kultivasi Awal:** Belum ada — akan ditentukan lewat roleplay
**Law Origin (jika sudah ada Hukum):** Belum ada
**Sekte/Afiliasi Awal:** Sanxiu (mantan keturunan Keluarga Yin)

**Kondisi Awal:** HP 100/100 · Qi 0/0 · Stamina 100/100 · Satiety 100% · Kondisi Normal · Karma Netral

**Currency Awal:**
- Tael Tembaga × 100

**Equipment Awal (terpakai/digenggam):**
- Senjata: Tidak ada
- Zirah/Pelindung: Jubah Sutra Kusam — Fan-Grade, sisa peninggalan keluarga terpandang yang sudah sederhana
- Aksesoris: Tidak ada

**Inventory Awal (dibawa, tidak terpakai):**
- Catatan Murni Teori Roh & Alkimia — berisi tulisan tangan pribadi hasil studi literatur (tanpa formula/resep praktis instan)
- Bekal Makanan Sederhana × 2

**Teknik Awal:**
- Pengetahuan Teori Roh & Alkimia Dasar — pemahaman akademis dari buku-buku Keluarga Yin (tanpa penguasaan Qi)

**Latar Belakang & Kepribadian:**
Berasal dari Keluarga Yin, faksi terpandang yang memiliki pemahaman mendalam tentang Roh dan Alkemis. Nama aslinya adalah Yin Zheng, namun ia mengubah namanya menjadi Tatsuya entah kenapa. Sejak kecil ia tumbuh atas rasa penasaran mendalam terhadap dunia, sesuatu yang fana, dan hal-hal di luar akal sehat manusia, serta sangat mengagumi hewan dan fenomena roh. Meski mempelajari banyak teori dari buku-buku keluarganya sejak kecil, Tatsuya melangkah ke Jianghu dari titik nol tanpa basis Qi aktif maupun artefak instan. Sifatnya santai, penuh rasa ingin tahu, berambisi menciptakan inovasi baru yang belum pernah terpikirkan orang lain, dan menyukai hewan.

---

### 👤 Wang Zixiin

**Lokasi Awal:** Desa Luoye, Central Plains *(lihat `02_CENTRAL_PLAINS.md`)*
**Realm & Stage Awal:** Mortal Foundation (Fondasi Fana), Awal — Qi Cap: 0 *(RealmBase v3.0 — lihat `09_CULTIVATION_LAW_SYSTEM.md` §9)*
**Hukum Kultivasi Awal:** Belum ada — akan ditentukan lewat roleplay
**Law Origin (jika sudah ada Hukum):** Belum ada
**Sekte/Afiliasi Awal:** Sanxiu (tanpa sekte)

**Kondisi Awal:** HP 100/100 · Qi 0/0 · Stamina 100/100 · Satiety 100% · Kondisi Normal · Karma Netral

**Currency Awal:**
- Tael Tembaga × 0

**Equipment Awal (terpakai/digenggam):**
- Senjata: Tidak ada
- Zirah/Pelindung: Pakaian Lusuh — Fan-Grade, pakaian kasar tanpa perlindungan
- Aksesoris: Tidak ada

**Inventory Awal (dibawa, tidak terpakai):**
- Tidak ada

**Teknik Awal:**
- Tidak ada

**Latar Belakang & Kepribadian:**
Terbaring di tepi hutan bambu Desa Luoye dengan pakaian lusuh, tanpa ingatan, nama, maupun sekeping uang pun di kantongnya. Telapak tangannya yang halus menandakan ia belum pernah menyentuh senjata, menjadikannya seorang asing sejati tanpa basis kultivasi di tengah kerasnya dunia Jianghu. Wang Zixiin harus belajar bertahan hidup dari titik yang benar-benar hampa, mengandalkan insting dan kebaikan orang sekitar untuk mulai membangun pijakannya di dunia kultivator.

---

### 👤 Ying Luo

**Lokasi Awal:** Desa Qingfeng, Azure Mountain Range *(lihat `03_AZURE_MOUNTAIN_RANGE.md`)*
**Realm & Stage Awal:** Mortal Foundation (Fondasi Fana), Awal — Qi Cap: 0 *(RealmBase v3.0 — lihat `09_CULTIVATION_LAW_SYSTEM.md` §9)*
**Hukum Kultivasi Awal:** Belum ada — akan ditentukan lewat roleplay
**Law Origin (jika sudah ada Hukum):** Belum ada
**Sekte/Afiliasi Awal:** Sanxiu (tanpa sekte)

**Kondisi Awal:** HP 100/100 · Qi 0/0 · Stamina 100/100 · Satiety 100% · Kondisi Normal · Karma Netral

**Currency Awal:**
- Tael Tembaga × 20

**Equipment Awal (terpakai/digenggam):**
- Senjata: Tidak ada
- Zirah/Pelindung: Baju Desa Sederhana — Fan-Grade, pakaian kain lusuh anak desa
- Aksesoris: Pita Biru Usang — hiasan rambut sederhana dari kakeknya

**Inventory Awal (dibawa, tidak terpakai):**
- Bekal Bunga Kering & Buah Hutan × 2

**Teknik Awal:**
- Tidak ada

**Latar Belakang & Kepribadian:**
Gadis kecil bertubuh mungil dengan rambut hitam yang sering diikat dua kuncir pita biru usang. Penampilannya yang paling mencolok adalah sepasang mata berwarna biru laut yang dalam, kontras dengan rambut dan alis hitamnya. Warna matanya membuat Ying Luo sering dijauhi anak-anak desa yang menganggapnya "anak aneh" atau "keturunan iblis". Kulitnya pucat karena lebih suka duduk di bawah pohon tua mendengarkan cerita kakeknya. Ia tinggal di Desa Qingfeng, sebuah desa tersembunyi yang sangat terpencil di kaki Pegunungan Awan Tua. Sifatnya pendiam, lembut, namun menyimpan rasa penasaran pada dunia luar.

---

### 👤 神Nēru

**Lokasi Awal:** Desa Tiedao, Central Plains *(lihat `02_CENTRAL_PLAINS.md`)*
**Realm & Stage Awal:** Mortal Foundation (Fondasi Fana), Awal — Qi Cap: 0 *(RealmBase v3.0 — lihat `09_CULTIVATION_LAW_SYSTEM.md` §9)*
**Hukum Kultivasi Awal:** Belum ada — akan ditentukan lewat roleplay
**Law Origin (jika sudah ada Hukum):** Belum ada
**Sekte/Afiliasi Awal:** Sanxiu (tanpa sekte)

**Kondisi Awal:** HP 100/100 · Qi 0/0 · Stamina 100/100 · Satiety 100% · Kondisi Normal · Karma Netral

**Currency Awal:**
- Tael Tembaga × 50

**Equipment Awal (terpakai/digenggam):**
- Senjata: Tidak ada
- Zirah/Pelindung: Jubah Sederhana — Fan-Grade, pakaian biasa untuk berkelana
- Aksesoris: Tidak ada

**Inventory Awal (dibawa, tidak terpakai):**
- Bekal Makanan Sederhana × 2
- Peta Wilayah Kasar — gambaran peta tangan buatan warga lokal

**Teknik Awal:**
- Tidak ada

**Latar Belakang & Kepribadian:**
Saat terbangun tiga tahun lalu, ia mendapati dirinya berada di tempat asing tanpa mengetahui bagaimana ia bisa sampai di sana dan tanpa ingatan tentang masa lalunya. Sebagai orang luar yang belum memahami dunia Jianghu, ia lebih banyak mengamati dan mempelajari orang-orang di sekitarnya. Dengan sifat tenang dan rasa ingin tahu yang besar, ia perlahan terbiasa dengan lingkungan barunya. Kini terlihat sebaya dengan seseorang berusia 16 tahun, 神Nēru memulai perjalanannya untuk mengenal lebih banyak tentang Jianghu sekaligus mencari tahu tentang masa lalunya.

---

### 👤 Lu Qingxuan

**Lokasi Awal:** Desa Xingcun, Central Plains *(lihat `02_CENTRAL_PLAINS.md`)*
**Realm & Stage Awal:** Mortal Foundation (Fondasi Fana), Awal — Qi Cap: 0 *(RealmBase v3.0 — lihat `09_CULTIVATION_LAW_SYSTEM.md` §9)*
**Hukum Kultivasi Awal:** Belum ada — akan ditentukan lewat roleplay
**Law Origin (jika sudah ada Hukum):** Belum ada
**Sekte/Afiliasi Awal:** Sanxiu (tanpa sekte)

**Kondisi Awal:** HP 100/100 · Qi 0/0 · Stamina 100/100 · Satiety 100% · Kondisi Normal · Karma Netral

**Currency Awal:**
- Tael Tembaga × 50

**Equipment Awal (terpakai/digenggam):**
- Senjata: Tidak ada
- Zirah/Pelindung: Baju Katun Desa — Fan-Grade, pakaian sederhana warga desa
- Aksesoris: Tidak ada

**Inventory Awal (dibawa, tidak terpakai):**
- Bekal Makanan Sederhana × 2
- Kantong Air Kulit × 1

**Teknik Awal:**
- Tidak ada

**Latar Belakang & Kepribadian:**
Pemuda biasa yang lahir dari keluarga sederhana di sebuah desa kecil. Ia tidak memiliki bakat khusus, nama besar, maupun keistimewaan apa pun. Sejak kecil ia menjalani hidup sederhana, namun di dalam dirinya menyimpan keinginan kuat untuk melihat dunia yang lebih luas dan membuktikan bahwa seseorang yang memulai dari nol tetap bisa menentukan jalannya sendiri. Lu Qingxuan meninggalkan desanya dan memulai perjalanan sebagai seorang pemula, tanpa kekuatan, tanpa guru, dan tanpa tujuan pasti — hanya berbekal keberanian dan kemauan keras untuk terus melangkah di Jianghu.

---

### 👤 Paijo

**Lokasi Awal:** Kota Luoyang Kecil, Central Plains *(lihat `02_CENTRAL_PLAINS.md`)*
**Realm & Stage Awal:** Mortal Foundation (Fondasi Fana), Awal — Qi Cap: 0 *(RealmBase v3.0 — lihat `09_CULTIVATION_LAW_SYSTEM.md` §9)*
**Hukum Kultivasi Awal:** Belum ada — akan ditentukan lewat roleplay
**Law Origin (jika sudah ada Hukum):** Belum ada
**Sekte/Afiliasi Awal:** Sanxiu (tanpa sekte)

**Kondisi Awal:** HP 100/100 · Qi 0/0 · Stamina 100/100 · Satiety 100% · Kondisi Normal · Karma Netral

**Currency Awal:**
- Tael Tembaga × 30

**Equipment Awal (terpakai/digenggam):**
- Senjata: Tidak ada
- Zirah/Pelindung: Pakaian Katun Lusuh — Fan-Grade, pakaian jalanan biasa tanpa perlindungan
- Aksesoris: Tidak ada

**Inventory Awal (dibawa, tidak terpakai):**
- Bekal Makanan Sederhana × 2
- Kantong Air Kulit × 1

**Teknik Awal:**
- Tidak ada

**Latar Belakang & Kepribadian:**
Di dunia Jianghu, setiap yatim piatu biasanya memiliki masa lalu yang tragis dan mulia—orang tua mereka tewas demi membela kebenaran atau dibantai oleh sekte iblis. Tidak dengan Paijo. Kebenarannya sangat menyedihkan dan tidak heroik: Orang tuanya adalah petani miskin yang tewas bukan karena perang persilatan, melainkan karena tertimpa genteng saat para pendekar "berhati lurus" saling melempar batu bata di atas atap rumah mereka saat mengejar penjahat.

Sejak saat itu, Paijo belajar satu hal penting di jalanan: Kehormatan tidak bisa dimakan, dan keadilan hanya milik mereka yang memiliki tenaga dalam (Neigong) tingkat tinggi. Ia tumbuh di kota perdagangan yang menjadi persimpangan berbagai sekte. Menyadari bahwa ia tidak memiliki bakat martial arts, tidak memiliki garis keturunan dewa, dan tubuhnya lemah, Paijo memilih jalan bertahan hidup yang paling efektif: Menjadi parasit di tengah para raksasa. Ia belajar bahwa para pendekar besar, meskipun bisa membelah gunung dengan pedang, sangat mudah ditipu oleh rasa kasihan, keserakahan, atau ego mereka sendiri.
