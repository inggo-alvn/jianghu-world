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
**Realm & Stage Awal:** Foundation Establishment (Pembentukan Fondasi), Menengah — Qi Cap: 3.750 *(2.500 × 1,5)*
**Hukum Kultivasi Awal:** Dao Abadi (varian pedang ringan, gaya Dojo Bunga Aprikot)
**Law Origin:** Jalur Guru — diajarkan oleh **Guru Li Xingchun**, Kepala Dojo Bunga Aprikot, sejak usia 14 tahun. Teknik yang sudah dikuasai: *Jurus Pedang Bunga Gugur* (tingkat dasar).
**Sekte/Afiliasi Awal:** Dojo Bunga Aprikot (Desa Xingcun) — murid biasa, belum murid inti

**Kondisi Awal:** HP 1.500/1.500 · Qi 3.750/3.750 · Stamina 100/100 · Satiety 70% · Kondisi Normal · Karma Netral (belum ada catatan Merit/Sin)

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

*(Admin menambahkan blok karakter baru di bawah ini dengan menyalin Template Kosong §3, lalu memperbarui Daftar Karakter §1.)*
