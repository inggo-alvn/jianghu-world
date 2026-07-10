# 🏯 Wuxian World — World Bible (Edisi Markdown Modular)

**Versi:** 2.0 (Reorganisasi dari `JIANGHU.docx` versi 1.0)
**Genre:** Xianxia · Wuxia · Kultivasi · Hardcore Realism
**Tujuan:** Roleplay kultivasi yang adil, mendalam, konsisten, dan realistis dengan AI Game Master — dioptimalkan agar AI tidak perlu memindai satu dokumen raksasa tiap giliran, dan agar dunia tetap **terkendali & konkrit** lewat rujukan file yang jelas.

Repo ini adalah pecahan dari satu World Bible besar menjadi **17 file `.md`** yang saling terhubung: 15 modul lore/sistem, plus `INDEX.md` (hub navigasi) dan `players.md` (katalog **data awal** karakter, dikelola admin). Setiap modul berdiri sendiri (bisa ditautkan satu-satu), tapi tetap konsisten satu sama lain lewat sistem rujukan silang (`lihat 09_...md §8.2`, dst).

> 🧭 **Cara tercepat mulai main:** tempel **satu link saja** — raw link `INDEX.md` — lalu sebutkan nama karaktermu (atau nama + lokasi awal kalau karakter baru). AI akan menjelajah sendiri ke modul lain sesuai kebutuhan cerita. Lihat bagian "💬 Cara Main" di bawah.

---

## 📂 Struktur Modul

| # | File | Isi | Wajib / Situasional |
|---|---|---|---|
| 🧭 | [`INDEX.md`](./INDEX.md) | **Hub navigasi tunggal** — seluruh link + logika kapan fetch modul apa | ✅ **Inilah yang ditempel ke AI, bukan link lain** |
| 📇 | [`players.md`](./players.md) | Katalog **data awal** karakter — admin-only, read-only bagi AI, BUKAN save system | Difetch otomatis lewat `INDEX.md` HANYA saat karakter dimainkan pertama kali |
| — | [`README.md`](./README.md) | Peta navigasi & dokumentasi ini | Referensi manusia (tidak perlu ditautkan ke AI) |
| 00 | [`00_CORE_RULES_AI_GM.md`](./00_CORE_RULES_AI_GM.md) | Aturan mutlak AI GM, anti-cheat, format respon wajib, cheat-sheet formula inti | ✅ **WAJIB tiap sesi** (difetch otomatis lewat `INDEX.md`) |
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
2. Upload ke-17 file `.md` ini ke root repo (atau ke satu folder, misalnya `/world/`) — termasuk `INDEX.md` dan `players.md`.
3. Setiap file punya "raw link" dengan format:
   ```
   https://raw.githubusercontent.com/USERNAME/REPO/BRANCH/NAMA_FILE.md
   ```
   atau `.../refs/heads/BRANCH/NAMA_FILE.md` — keduanya format resmi GitHub yang valid.
4. Buka `INDEX.md` §1, pastikan seluruh link di tabel sudah cocok dengan username/repo-mu sendiri.
5. Isi `players.md` dengan karaktermu sendiri (lihat contoh "Jiang Ziling" di dalamnya sebagai referensi format), lalu perbarui link `players.md` di `INDEX.md` §1 dari placeholder ke link raw yang sebenarnya.
6. Setelah itu, **kamu hanya perlu menempel SATU link** — raw link `INDEX.md` — di setiap sesi baru. Lihat "💬 Cara Main" di bawah.

---

## 💬 Cara Main — Metode Utama (Satu Link)

Sejak ada `INDEX.md`, kamu tidak perlu lagi mengumpulkan link satu-satu tiap sesi. `INDEX.md` sudah memuat seluruh direktori link + logika "kondisi apa → fetch modul apa" (lihat `INDEX.md` §2), jadi AI yang bisa browsing/fetch link (mis. Claude dengan web search/fetch aktif) akan menjelajah sendiri.

Pilih salah satu dari tiga template di bawah sesuai situasimu. `players.md` **hanya** relevan untuk Template A (katalog data awal, admin-only) — ia bukan save system, jadi Template C (melanjutkan karakter) tidak pernah menyentuhnya.

### A. Mulai Karakter dari Katalog `players.md` (Pertama Kali Dimainkan)
```
Kamu akan jadi AI Game Master untuk roleplay Wuxian World. Baca dan ikuti seluruh isi link berikut sebagai satu-satunya sumber kebenaran (link itu sendiri berisi instruksi cara menjelajah ke modul lain sesuai kondisi cerita):

https://raw.githubusercontent.com/USERNAME/REPO/refs/heads/main/INDEX.md

Aku mau mulai main sebagai: [nama karakter — harus persis sama dengan heading di players.md]
(Ini kali pertama karakter ini dimainkan.)
```

### B. Karakter Custom Baru (Belum Terdaftar di `players.md`)
```
Kamu akan jadi AI Game Master untuk roleplay Wuxian World. Baca dan ikuti seluruh isi link berikut sebagai satu-satunya sumber kebenaran:

https://raw.githubusercontent.com/USERNAME/REPO/refs/heads/main/INDEX.md

Data karakterku (karakter baru, belum terdaftar di players.md):
- Nama: [nama karaktermu]
- Lokasi awal: [pilih dari daftar lokasi di modul wilayah yang sesuai]
```

### C. Melanjutkan Karakter yang Sudah Pernah Dimainkan
```
Lanjutkan roleplay Wuxian World sebagai AI GM. Ikuti seluruh isi link berikut sebagai satu-satunya sumber kebenaran:

https://raw.githubusercontent.com/USERNAME/REPO/refs/heads/main/INDEX.md

Status karakterku terakhir (lanjutkan dari sini):
[tempel ulang blok "Profil Karakter" terakhir dari sesi sebelumnya]
```

> Ganti `USERNAME/REPO` dengan path repo GitHub-mu sendiri (untuk repo `inggo-alvn/jianghu-world`, link `INDEX.md`-nya adalah `https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/INDEX.md`). `players.md` tidak pernah menyimpan progres — untuk Template C kamu sendiri yang menyimpan blok "Profil Karakter" terakhir (copy-paste dari balasan AI di sesi sebelumnya) dan menempelkannya kembali. Kecuali AI-mu tidak bisa membuka link secara mandiri, lihat metode manual di bawah.

---

## 🎯 Metode Manual (Fallback, Jika AI Tidak Bisa Fetch Link)

Kalau AI yang kamu pakai tidak punya kemampuan membuka link sendiri, kamu masih bisa menempel modul satu-satu secara manual. Pakai pola ini supaya hemat token — tidak perlu menempel ke-15 modul tiap kali chat:

| Situasi | Link yang Ditempel |
|---|---|
| **Selalu** (tiap sesi baru / ganti chat) | `00_CORE_RULES_AI_GM.md` + modul wilayah tempat karaktermu berada saat ini |
| Mulai karakter dari katalog `players.md` (pertama kali) | + `players.md` |
| Melanjutkan karakter yang sudah pernah main | Tempel manual blok "Profil Karakter" terakhir (**bukan** `players.md`) |
| Karakter pindah wilayah | Ganti link modul wilayah ke wilayah tujuan |
| Mau breakthrough / klaim teknik baru | + `09_CULTIVATION_LAW_SYSTEM.md` |
| Mau berdagang / lihat harga | + `10_ECONOMY_SYSTEM.md` |
| Pertarungan serius (bukan sekadar deskripsi kalah/menang cepat) | + `12_COMBAT_SYSTEM.md` (dan `13_BESTIARY.md` jika lawan monster) |
| Bertemu pembunuh bayaran/info broker/buronan lintas wilayah | + `08_CROSS_REGION_ORGANIZATIONS.md` |
| Cek detail status HP/lapar yang rumit | + `11_VITALITY_HUNGER_SYSTEM.md` |

`00_CORE_RULES_AI_GM.md` sudah memuat ringkasan formula inti (§3), jadi untuk adegan ringan (dialog, eksplorasi tanpa combat/transaksi berat), **00 + modul wilayah saja sudah cukup**. Logika lengkap trigger→modul yang sama juga dipakai otomatis oleh AI lewat `INDEX.md` §2.

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

**v2.1 — Update Navigasi Satu-Link:**
- Ditambahkan `INDEX.md` sebagai hub navigasi tunggal — pemain sekarang cukup menempel satu link, AI menjelajah ke modul lain secara otomatis sesuai kondisi cerita (lihat `INDEX.md` §2 untuk logika lengkapnya).
- Ditambahkan `players.md` sebagai katalog data awal karakter berformat konsisten (realm, Hukum & Law Origin, sekte, kondisi awal, currency, inventory, teknik, latar belakang) — lengkap dengan satu contoh terisi ("Jiang Ziling") sebagai referensi format.

**v2.2 — Klarifikasi: `players.md` Bukan Sistem Save:**
- `players.md` ditegaskan sebagai katalog **data awal** yang read-only bagi AI dan hanya diedit admin — bukan save/checkpoint. Semua bahasa "save data"/"save state"/"riwayat breakthrough berjalan" dari v2.1 sudah diperbaiki di seluruh modul (`INDEX.md`, `00_CORE_RULES_AI_GM.md`, `README.md`, `players.md`).
- Ditambahkan aturan eksplisit `00_CORE_RULES_AI_GM.md` §1.10 dan jalur input awal ketiga di §1.6 (mulai dari katalog / karakter custom baru / melanjutkan karakter via paste "Profil Karakter") supaya AI tidak keliru mengira `players.md` menyimpan progres.

---

## ✅ Checklist Sebelum Main

- [ ] Repo GitHub sudah publik & ke-17 file (termasuk `INDEX.md` & `players.md`) sudah ter-upload
- [ ] Link raw `INDEX.md` sudah dites bisa dibuka di browser (harus menampilkan teks mentah markdown, bukan 404)
- [ ] Semua link di dalam `INDEX.md` §1 sudah dicek cocok dengan username/repo-mu sendiri
- [ ] Link `players.md` di `INDEX.md` §1 sudah diganti dari placeholder ke link raw yang sebenarnya setelah file itu di-upload
- [ ] `players.md` sudah diisi dengan karaktermu sendiri (atau pakai dulu contoh "Jiang Ziling" untuk coba sistemnya)
- [ ] Tahu karaktermu mulai dari lokasi mana (cek daftar lokasi di modul wilayah terkait sebelum sesi pertama)

Selamat berkelana di Jianghu. 🗡️
