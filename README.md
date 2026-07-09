# 🏯 Wuxian World — World Bible (Edisi Markdown Modular)

**Versi:** 2.0 (Reorganisasi dari `JIANGHU.docx` versi 1.0)
**Genre:** Xianxia · Wuxia · Kultivasi · Hardcore Realism
**Tujuan:** Roleplay kultivasi yang adil, mendalam, konsisten, dan realistis dengan AI Game Master — dioptimalkan agar AI tidak perlu memindai satu dokumen raksasa tiap giliran, dan agar dunia tetap **terkendali & konkrit** lewat rujukan file yang jelas.

Repo ini adalah pecahan dari satu World Bible besar menjadi **15 modul `.md`** yang saling terhubung. Setiap modul berdiri sendiri (bisa ditautkan satu-satu), tapi tetap konsisten satu sama lain lewat sistem rujukan silang (`lihat 09_...md §8.2`, dst).

---

## 📂 Struktur Modul

| # | File | Isi | Wajib / Situasional |
|---|---|---|---|
| — | [`README.md`](./README.md) | Peta navigasi ini | Referensi manusia (tidak perlu ditautkan ke AI) |
| 00 | [`00_CORE_RULES_AI_GM.md`](./00_CORE_RULES_AI_GM.md) | Aturan mutlak AI GM, anti-cheat, format respon wajib, cheat-sheet formula inti | ✅ **WAJIB tiap sesi** |
| 01 | [`01_WORLD_OVERVIEW_AND_CAPITAL.md`](./01_WORLD_OVERVIEW_AND_CAPITAL.md) | Peta jarak dunia, Ibu Kota Tianjing & Kekaisaran | Situasional (konteks besar / karakter di ibu kota) |
| 02 | [`02_CENTRAL_PLAINS.md`](./02_CENTRAL_PLAINS.md) | Dataran Tengah: kota, desa, sekte, bandit, NPC | Saat karakter di Central Plains |
| 03 | [`03_AZURE_MOUNTAIN_RANGE.md`](./03_AZURE_MOUNTAIN_RANGE.md) | Pegunungan Azure | Saat karakter di Azure Mountain Range |
| 04 | [`04_SOUTHERN_DEMON_DOMAIN.md`](./04_SOUTHERN_DEMON_DOMAIN.md) | Daerah Iblis Selatan | Saat karakter di Southern Demon Domain |
| 05 | [`05_EASTERN_SEA_REGION.md`](./05_EASTERN_SEA_REGION.md) | Wilayah Laut Timur | Saat karakter di Eastern Sea Region |
| 06 | [`06_NORTHERN_DESOLATE_TERRITORY.md`](./06_NORTHERN_DESOLATE_TERRITORY.md) | Wilayah Utara Gersang | Saat karakter di Northern Territory |
| 07 | [`07_WESTERN_SACRED_DESERTS.md`](./07_WESTERN_SACRED_DESERTS.md) | Gurun Suci Barat | Saat karakter di Western Deserts |
| 08 | [`08_CROSS_REGION_ORGANIZATIONS.md`](./08_CROSS_REGION_ORGANIZATIONS.md) | Info broker, pegadaian, perhimpunan tabib, pembunuh bayaran, sanxiu, kriminal mortal | Saat berurusan dengan organisasi lintas wilayah / buronan |
| 09 | [`09_CULTIVATION_LAW_SYSTEM.md`](./09_CULTIVATION_LAW_SYSTEM.md) | 9 Realm, 5 Hukum kultivasi, breakthrough, tribulasi, karma | Saat breakthrough, klaim teknik, atau hitung Qi detail |
| 10 | [`10_ECONOMY_SYSTEM.md`](./10_ECONOMY_SYSTEM.md) | Mata uang, tier/grade barang, harga jasa, aset, tawar-menawar | Saat transaksi/jual-beli |
| 11 | [`11_VITALITY_HUNGER_SYSTEM.md`](./11_VITALITY_HUNGER_SYSTEM.md) | Formula HP, status luka, regenerasi, kelaparan | Saat cek status detail / efek kelaparan |
| 12 | [`12_COMBAT_SYSTEM.md`](./12_COMBAT_SYSTEM.md) | Giliran, initiative, damage, defense, escape | Setiap kali terjadi pertarungan |
| 13 | [`13_BESTIARY.md`](./13_BESTIARY.md) | Monster & spirit beast per wilayah, ambush, loot | Perjalanan liar / hunting / ambush |

> Semua NPC, lokasi, formula, dan angka di modul-modul ini **identik** dengan `JIANGHU.docx` asli — hanya format & organisasinya yang diperbaiki (tabel dirapikan, bold yang rusak diperbaiki, ditambah rujukan silang dan "Fakta Cepat" di tiap wilayah). Tidak ada isi yang dihapus atau diubah nilainya.

---

## 🚀 Cara Setup di GitHub

1. Buat repository baru di GitHub — **harus PUBLIC** (repo privat butuh token otentikasi supaya raw link bisa diakses AI, jadi hindari kecuali kamu tahu cara handle itu).
2. Upload ke-15 file `.md` ini ke root repo (atau ke satu folder, misalnya `/world/`).
3. Setiap file punya "raw link" dengan format:
   ```
   https://raw.githubusercontent.com/USERNAME/REPO/BRANCH/NAMA_FILE.md
   ```
   Contoh: `https://raw.githubusercontent.com/namamu/wuxian-world/main/00_CORE_RULES_AI_GM.md`
4. Kumpulkan link-link yang kamu butuhkan (lihat rekomendasi "muatan" di bawah), lalu tempel di chat ke AI.

---

## 🎯 Rekomendasi "Muatan" per Sesi

Supaya hemat token tapi tetap konkrit, kamu tidak perlu menempel ke-13 modul tiap kali chat. Pakai pola ini:

| Situasi | Link yang Ditempel |
|---|---|
| **Selalu** (tiap sesi baru / ganti chat) | `00_CORE_RULES_AI_GM.md` + modul wilayah tempat karaktermu berada saat ini |
| Karakter pindah wilayah | Ganti link modul wilayah ke wilayah tujuan |
| Mau breakthrough / klaim teknik baru | + `09_CULTIVATION_LAW_SYSTEM.md` |
| Mau berdagang / lihat harga | + `10_ECONOMY_SYSTEM.md` |
| Pertarungan serius (bukan sekadar deskripsi kalah/menang cepat) | + `12_COMBAT_SYSTEM.md` (dan `13_BESTIARY.md` jika lawan monster) |
| Bertemu pembunuh bayaran/info broker/buronan lintas wilayah | + `08_CROSS_REGION_ORGANIZATIONS.md` |
| Cek detail status HP/lapar yang rumit | + `11_VITALITY_HUNGER_SYSTEM.md` |

`00_CORE_RULES_AI_GM.md` sudah memuat ringkasan formula inti (§3), jadi untuk adegan ringan (dialog, eksplorasi tanpa combat/transaksi berat), **00 + modul wilayah saja sudah cukup**.

---

## 💬 Template Pesan Pembuka Sesi

### Sesi Pertama (Karakter Baru)

```
Kamu akan jadi AI Game Master untuk roleplay Wuxian World. Ikuti SELURUH aturan di link berikut secara ketat, terutama bagian anti-cheat dan format respon wajib:

1. Aturan Inti: https://raw.githubusercontent.com/USERNAME/REPO/main/00_CORE_RULES_AI_GM.md
2. Wilayah awal: https://raw.githubusercontent.com/USERNAME/REPO/main/0X_NAMA_WILAYAH.md

Data karakterku:
- Nama: [nama karaktermu]
- Lokasi awal: [pilih dari daftar lokasi di modul wilayah]

Mulai sesi dari sini, ikuti format respon wajib di setiap balasan.
```

### Sesi Lanjutan

```
Lanjutkan roleplay Wuxian World sebagai AI GM, ikuti aturan ketat di:
1. https://raw.githubusercontent.com/USERNAME/REPO/main/00_CORE_RULES_AI_GM.md
2. https://raw.githubusercontent.com/USERNAME/REPO/main/0X_NAMA_WILAYAH.md
(tambahkan link modul lain di sini jika relevan dengan situasi saat ini — combat/ekonomi/kultivasi/dsb)

Status karakterku terakhir:
[tempel blok "Profil Karakter" terakhir dari sesi sebelumnya]

Lanjutkan dari sini.
```

> Ganti `USERNAME/REPO/main` dengan path repo GitHub-mu sendiri. Simpan template ini di suatu tempat (Notes, dsb.) supaya tinggal copy-paste tiap mulai sesi baru.

---

## 🌏 Dunia dalam Angka (ringkasan — detail penuh di `01_WORLD_OVERVIEW_AND_CAPITAL.md`)

- **Luas total:** ± 48 juta li² · **Populasi:** ± 280 juta jiwa · **Kekayaan total:** ± 3,2 miliar Tael Perak
- **7 wilayah besar:** Central Plains (ibu kota di sini), Azure Mountain Range, Southern Demon Domain, Eastern Sea Region, Northern Desolate Territory, Western Sacred Deserts, plus organisasi lintas wilayah
- **9 Major Realm × 3 Stage** kultivasi, **5 Hukum kultivasi** berbeda (Raga Sejati, Qi Naga Api, Dao Abadi, Gu Karma, Custom)
- **85,7% populasi** adalah mortal biasa tanpa kultivasi — kekerasan jianghu sehari-hari justru paling sering datang dari kalangan ini, bukan dari kultivator elite

---

## 🛠️ Riwayat Perubahan dari Dokumen Asli

- Sumber: `JIANGHU.docx` v1.0 (Wuxian World + Sistem Hukum Kultivasi + Sistem Ekonomi + Sistem Vitalitas & Kelaparan + Sistem Pertempuran + Bestiarium, semuanya jadi satu file Word).
- Dipecah menjadi 15 file `.md` bertopik agar AI hanya perlu memuat modul yang relevan per giliran.
- Semua tabel dirapikan ke format Markdown standar (tabel asli di docx banyak mengalami artefak bold `****` akibat konversi — sudah dibersihkan tanpa mengubah data).
- Ditambahkan: blok "Fakta Cepat" di tiap modul wilayah (Qi Density Modifier, monster khas, dsb.), tag Hukum kultivasi tiap sekte langsung di deskripsinya, dan rujukan silang antar modul (`lihat 09_...md §8.2`) supaya AI/pemain tidak perlu menghafal semua di kepala.
- **Tidak ada NPC, lokasi, angka, atau formula yang dihapus atau diubah nilainya** dari dokumen asli — murni reorganisasi & pembersihan format.

---

## ✅ Checklist Sebelum Main

- [ ] Repo GitHub sudah publik & ke-15 file sudah ter-upload
- [ ] Link raw sudah dites bisa dibuka di browser (harus menampilkan teks mentah markdown, bukan 404)
- [ ] Template pesan pembuka sudah disiapkan dengan username/repo yang benar
- [ ] Tahu karaktermu mulai dari lokasi mana (cek daftar lokasi di modul wilayah terkait sebelum sesi pertama)

Selamat berkelana di Jianghu. 🗡️
