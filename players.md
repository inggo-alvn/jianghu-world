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

```
### 👤 [Inggo]

**Lokasi Awal:** [02]
**Realm & Stage Awal:** [Mortal] — Qi Cap: [0]
**Hukum Kultivasi Awal:** [none]
**Law Origin (jika sudah ada Hukum): none
**Sekte/Afiliasi Awal:** [none]

**Kondisi Awal:** HP X/Y · Qi X/Y · Stamina X/100 · Satiety X% · Kondisi Normal · Karma Netral

**Currency Awal:** [none]

**Inventory Awal:**
- [Item 1 — none]
- [Item 2 — none]

**Teknik Awal:**
- [none]

**Latar Belakang & Kepribadian:**
[1–2 paragraf: seorang mortal biasa tanpa memiliki apapun tiba di daera ini]
```
---

## 2. Skema Field (Penjelasan Singkat)

| Field | Isi |
|---|---|
| **Lokasi Awal** | Nama lokasi persis sesuai modul `01`–`07` |
| **Realm & Stage Awal** + **Qi Cap** | Sesuai `09_CULTIVATION_LAW_SYSTEM.md` §2 — `QiCap = RealmBase × StageMultiplier` |
| **Hukum Kultivasi Awal** + **Law Origin** | Kalau karakter sudah punya Hukum sejak cerita dimulai, wajib sertakan asal-usulnya (Guru/Manual/Pencerahan) sesuai `09` §3.0 |
| **Sekte/Afiliasi Awal** | Nama sekte + peran, atau "Sanxiu (tanpa sekte)" |
| **Kondisi Awal** | HP/Qi/Stamina/Satiety/Karma **di titik cerita dimulai** — nilai tetap, bukan yang di-update |
| **Currency & Inventory Awal** | Kepemilikan saat cerita dimulai |
| **Teknik Awal** | Harus konsisten dengan Law Origin |
| **Latar Belakang & Kepribadian** | Bio singkat: sifat, motivasi, relasi NPC yang relevan — fakta lore tetap, bukan log yang terus bertambah |


