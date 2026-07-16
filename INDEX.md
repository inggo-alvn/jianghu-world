# 🧭 Wuxian World — INDEX (Satu Link untuk Semua)

> **Ini adalah SATU-SATUNYA link yang perlu ditempel pemain di setiap sesi.**
> Semua modul lain (aturan, wilayah, sistem, data karakter) dijangkau AI secara otomatis dari sini lewat `web_fetch`/browsing, sesuai kondisi yang sedang terjadi di roleplay.
>
> **Untuk AI:** baca seluruh file ini dulu sampai habis, lalu jalankan **Prosedur Bootstrap** di §0 SEBELUM menulis balasan apa pun ke pemain. Jangan menjawab dari ingatan/memori bebas — dunia ini hanya sah kalau datanya berasal dari modul-modul yang ditautkan di sini.

---

## 0. Prosedur Bootstrap (WAJIB, Urutan Ini Persis)

1. **Fetch `00_CORE_RULES_AI_GM.md`** (link di tabel §1) — WAJIB pertama, tanpa kecuali. File itu berisi aturan mutlak, anti-cheat, dan format respon wajib yang mengikat seluruh sesi. Jangan lanjut ke langkah berikutnya sebelum ini selesai dibaca.
2. **Cek pesan pemain** untuk menentukan identitas & titik mulai karakter — ada 3 kemungkinan, jangan disamaratakan:
   - **(a) Karakter terdaftar, baru pertama kali dimainkan** (nama cocok entri di `players.md`, TIDAK ada blok "Profil Karakter" yang ditempel/riwayat sebelumnya) → fetch `players.md` (link §1), cari entri dengan nama itu, muat data awalnya sebagai **titik mulai** narasi. `players.md` murni data awal statis yang dikelola admin — bukan save-state, lihat §3.
   - **(b) Melanjutkan karakter yang sudah pernah dimainkan** (pemain menempel blok "Profil Karakter" dari sesi sebelumnya, atau riwayatnya masih ada di chat yang sama) → pakai kondisi TERKINI itu sebagai starting state. **JANGAN fetch `players.md`** — isinya statis, tidak pernah mencerminkan progres yang sudah terjadi.
   - **(c) Karakter benar-benar baru** (nama tidak ada di `players.md` maupun riwayat manapun) → perlakukan sebagai karakter baru custom sesuai `00_CORE_RULES_AI_GM.md` §1.6, minta Nama + Lokasi Awal.
3. **Tentukan lokasi karakter** (dari `players.md` atau dari input baru pemain), lalu fetch modul wilayah yang sesuai (`01`–`07`) dari tabel §1.
4. **Mulai sesi** mengikuti format respon wajib di `00`.
5. **Selama sesi berlangsung**, fetch modul tambahan secara dinamis begitu kondisinya muncul — lihat tabel pemicu di §2. Jangan fetch ke-18 file sekaligus di awal; itu boros token dan bertentangan dengan tujuan modularitas sistem ini.
6. Jika sebuah link gagal diakses (404/error), beri tahu pemain bahwa file itu mungkin belum ter-upload atau nama filenya salah — **jangan mengarang isinya**.

---

## 1. Direktori Lengkap Seluruh Modul

| Kode | File | Link Raw | Isi Singkat |
|---|---|---|---|
| 00 | `00_CORE_RULES_AI_GM.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/00_CORE_RULES_AI_GM.md | Aturan mutlak, anti-cheat, format respon wajib, cheat-sheet formula — **selalu difetch pertama** |
| 👤 | `players.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/players.md ⚠️*(placeholder, lihat §3)* | Data AWAL karakter (statis, dikelola admin — bukan save-state) — dicari lewat nama |
| 01 | `01_WORLD_OVERVIEW_AND_CAPITAL.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/01_WORLD_OVERVIEW_AND_CAPITAL.md | Peta jarak dunia & Ibu Kota Tianjing |
| 02 | `02_CENTRAL_PLAINS.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/02_CENTRAL_PLAINS.md | Central Plains: kota, desa, sekte, NPC |
| 03 | `03_AZURE_MOUNTAIN_RANGE.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/03_AZURE_MOUNTAIN_RANGE.md | Azure Mountain Range |
| 04 | `04_SOUTHERN_DEMON_DOMAIN.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/04_SOUTHERN_DEMON_DOMAIN.md | Southern Demon Domain |
| 05 | `05_EASTERN_SEA_REGION.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/05_EASTERN_SEA_REGION.md | Eastern Sea Region |
| 06 | `06_NORTHERN_DESOLATE_TERRITORY.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/06_NORTHERN_DESOLATE_TERRITORY.md | Northern Desolate Territory |
| 07 | `07_WESTERN_SACRED_DESERTS.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/07_WESTERN_SACRED_DESERTS.md | Western Sacred Deserts |
| 08 | `08_CROSS_REGION_ORGANIZATIONS.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/08_CROSS_REGION_ORGANIZATIONS.md | Info broker, pegadaian, pembunuh bayaran, sanxiu, kriminal mortal |
| 09 | `09_CULTIVATION_LAW_SYSTEM.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/09_CULTIVATION_LAW_SYSTEM.md | Realm, Hukum kultivasi, breakthrough, tribulasi, karma |
| 10 | `10_ECONOMY_SYSTEM.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/10_ECONOMY_SYSTEM.md | Mata uang, tier/grade barang, harga jasa & aset |
| 11 | `11_VITALITY_HUNGER_SYSTEM.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/11_VITALITY_HUNGER_SYSTEM.md | Formula HP, status luka, kelaparan |
| 12 | `12_COMBAT_SYSTEM.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/12_COMBAT_SYSTEM.md | Giliran, initiative, damage, defense, escape |
| 13 | `13_BESTIARY.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/13_BESTIARY.md | Monster & spirit beast per wilayah, ambush, loot |
| 14–34 | *(21 file sekte/dojo/organisasi individual)* | — | Lihat **§1a** di bawah untuk daftar lengkap per-file — **JANGAN** fetch semuanya sekaligus, cari nama sekte yang relevan lalu fetch HANYA file itu |
| — | `README.md` | https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/README.md | Dokumentasi setup untuk manusia (jarang perlu difetch AI) |

### 1a. Direktori Sekte, Dojo & Organisasi (21 File Individual)

> Setiap sekte/dojo/organisasi punya **file sendiri**, lengkap dengan hierarki, fasilitas, artefak/pusaka/seal-talisman, kurikulum teknik bertingkat, Hukum kultivasi detail, relasi antar-faksi, dan rahasia internal. Fetch HANYA file yang relevan dengan situasi saat ini — jangan fetch banyak sekaligus.

**Central Plains** *(base URL: `https://raw.githubusercontent.com/inggo-alvn/jianghu-world/refs/heads/main/`)*
| Sekte/Dojo | File |
|---|---|
| Heavenly Sword Pavilion | `14_HEAVENLY_SWORD_PAVILION.md` |
| Profound Heaven Sect | `15_PROFOUND_HEAVEN_SECT.md` |
| Silver Rain Sword School | `16_SILVER_RAIN_SWORD_SCHOOL.md` |
| Dojo Bunga Aprikot | `17_DOJO_BUNGA_APRIKOT.md` |
| Dojo Godam Besi | `18_DOJO_GODAM_BESI.md` |

**Azure Mountain Range**
| Sekte/Dojo | File |
|---|---|
| Golden Bell Monastery | `19_GOLDEN_BELL_MONASTERY.md` |
| Dojo Pahat Naga | `20_DOJO_PAHAT_NAGA.md` |

**Southern Demon Domain**
| Sekte/Dojo | File |
|---|---|
| Demonic Flame Palace | `21_DEMONIC_FLAME_PALACE.md` |
| Nine Serpent Den | `22_NINE_SERPENT_DEN.md` |
| Seven Sins Cult | `23_SEVEN_SINS_CULT.md` |
| Blood Shadow Alliance | `24_BLOOD_SHADOW_ALLIANCE.md` |
| Dojo Bayangan Kelam | `25_DOJO_BAYANGAN_KELAM.md` |

**Eastern Sea Region**
| Sekte/Dojo | File |
|---|---|
| Jade Purity Palace | `26_JADE_PURITY_PALACE.md` |
| Dojo Ombak Tenang | `27_DOJO_OMBAK_TENANG.md` |

**Northern Desolate Territory**
| Sekte/Dojo | File |
|---|---|
| Whitecloud Medicine Hall | `28_WHITECLOUD_MEDICINE_HALL.md` |
| Ghost Valley Sect | `29_GHOST_VALLEY_SECT.md` |
| Dojo Cakar Serigala | `30_DOJO_CAKAR_SERIGALA.md` |

**Western Sacred Deserts**
| Sekte/Dojo | File |
|---|---|
| Azure Cloud Temple | `31_AZURE_CLOUD_TEMPLE.md` |
| Dojo Mata Elang Pasir | `32_DOJO_MATA_ELANG_PASIR.md` |

**Lintas Wilayah**
| Organisasi | File |
|---|---|
| Perkumpulan Pisau Sunyi | `33_PERKUMPULAN_PISAU_SUNYI.md` |
| Kelompok Racun Bayangan | `34_KELOMPOK_RACUN_BAYANGAN.md` |

---

## 2. Alur Navigasi Otomatis (Trigger → Modul yang Difetch)

| Trigger dalam Roleplay | Modul yang Difetch | Catatan |
|---|---|---|
| Awal sesi (selalu) | `00_CORE_RULES_AI_GM.md` | Wajib pertama, lihat §0 |
| Karakter terdaftar di `players.md`, baru pertama kali dimainkan | `players.md` | Muat data AWAL sebagai titik mulai (data statis, bukan save-state) |
| Melanjutkan karakter yang sudah pernah dimainkan | — | Pakai blok "Profil Karakter" terakhir yang ditempel/ada di riwayat chat — **jangan** fetch `players.md` |
| Karakter benar-benar baru (tidak ada di `players.md`) | — | Ikuti `00` §1.6: minta Nama + Lokasi Awal |
| Karakter berada/menuju Central Plains | `02_CENTRAL_PLAINS.md` | Termasuk area ibu kota provinsi ini |
| Karakter berada/menuju Azure Mountain Range | `03_AZURE_MOUNTAIN_RANGE.md` | |
| Karakter berada/menuju Southern Demon Domain | `04_SOUTHERN_DEMON_DOMAIN.md` | |
| Karakter berada/menuju Eastern Sea Region | `05_EASTERN_SEA_REGION.md` | |
| Karakter berada/menuju Northern Desolate Territory | `06_NORTHERN_DESOLATE_TERRITORY.md` | |
| Karakter berada/menuju Western Sacred Deserts | `07_WESTERN_SACRED_DESERTS.md` | |
| Butuh konteks Ibu Kota Tianjing / peta jarak besar dunia | `01_WORLD_OVERVIEW_AND_CAPITAL.md` | |
| Bertemu info broker/pembunuh bayaran/sanxiu/kriminal mortal lintas wilayah | `08_CROSS_REGION_ORGANIZATIONS.md` | |
| Breakthrough realm / klaim teknik baru / cek Law Origin | `09_CULTIVATION_LAW_SYSTEM.md` | |
| Transaksi, tawar-menawar, cek harga barang/jasa/aset | `10_ECONOMY_SYSTEM.md` | |
| Perlu hitung detail regen HP / efek kelaparan lanjut | `11_VITALITY_HUNGER_SYSTEM.md` | Formula dasarnya sudah ada ringkas di `00` §3 |
| Pertarungan resmi dimulai (giliran, initiative, damage) | `12_COMBAT_SYSTEM.md` | |
| Lawan monster/spirit beast liar, perjalanan lewat zona liar (ambush) | `13_BESTIARY.md` | Dipakai bersamaan dengan `12` |
| Karakter mau bergabung sekte/dojo, eksplorasi fasilitas sekte, belajar teknik bertingkat, atau cek hierarki/artefak sekte tertentu | Cari nama sekte di **§1a**, fetch HANYA file itu | 21 file terpisah — jangan fetch lebih dari yang relevan dengan sekte yang sedang berinteraksi |
| Pemain minta bantuan setup GitHub / nanya cara pakai sistem ini | `README.md` | Ini file untuk manusia, sampaikan isinya ke pemain, bukan role-play |

**Efisiensi token:** jika sebuah modul sudah difetch sebelumnya dalam percakapan yang sama dan kondisinya belum berubah (mis. karakter masih di wilayah yang sama), **tidak perlu fetch ulang** — pakai isi yang sudah ada di riwayat chat.

---

## 3. Cara Kerja `players.md` (Data Awal Karakter, Bukan Save-System)

`players.md` berisi data AWAL tiap karakter pemain — realm, Hukum kultivasi, sekte, asset, inventory, teknik, relasi NPC, dan info penting lain **saat karakter itu mulai dimainkan**. File ini **statis dan hanya boleh diubah oleh admin (pemilik repo)** — AI tidak pernah mengedit, memperbarui, atau menyarankan perubahan terhadapnya. Detail skema & satu contoh lengkap ada di file itu sendiri.

**Alur pemakaian (HANYA untuk karakter yang belum pernah dimainkan):**
1. Pemain bilang nama karakternya di pesan pertama.
2. AI fetch `players.md`, cari heading `### 👤 [Nama]` yang cocok (ada di §4 file itu).
3. Semua field di blok itu jadi **titik mulai** narasi — tidak perlu tanya ulang ke pemain.
4. Sejak saat itu, perkembangan karakter (HP berubah, dapat/kehilangan item, breakthrough, pindah lokasi, dst.) **dilacak sepenuhnya di dalam percakapan** lewat blok "Profil Karakter" (`00_CORE_RULES_AI_GM.md` §2) — bukan ditulis balik ke `players.md`.
5. Jika nama tidak ada di `players.md` → ikuti prosedur karakter baru custom (`00` §1.6).

**Untuk sesi lanjutan** (karakter itu sudah pernah dimainkan) → **tidak** fetch `players.md` lagi. Pemain menempel ulang blok "Profil Karakter" terakhir dari sesi sebelumnya, dan itulah kondisi terkini yang dipakai.

> ⚠️ **Link `players.md` di tabel §1 masih PLACEHOLDER** (mengikuti pola repo yang sama). Ganti dengan link raw yang sebenarnya setelah file itu di-upload ke GitHub — lihat catatan lengkap di `players.md` itu sendiri.

---

## 4. Batasan Penting yang Harus Diketahui Pemain

- **Tidak ada sistem save di dunia ini.** `players.md` murni lembar data AWAL karakter yang statis — bukan file yang mengikuti progres cerita.
- **Hanya admin (pemilik repo) yang boleh mengubah `players.md`.** AI tidak bisa dan tidak akan menulis, memperbarui, atau menyarankan perubahan pada file ini kapan pun, termasuk di akhir sesi.
- Perkembangan karakter selama roleplay (HP, item, breakthrough, lokasi, dst.) sepenuhnya hidup **di dalam riwayat percakapan** lewat blok "Profil Karakter" — bukan di file manapun di repo.
- Jika sebuah link 404/gagal fetch, itu paling sering karena: nama file salah huruf besar-kecil (GitHub case-sensitive), file belum ter-push ke branch `main`, atau repo tidak publik.

---

## 5. Ringkasan Dunia (satu baris, detail penuh di `01`)

Xianxia · Wuxia · Kultivasi Hardcore Realism — 7 wilayah besar, 9 Major Realm × 3 Stage, 5 Hukum kultivasi berbeda, ± 280 juta jiwa populasi, tanpa plot armor, semua mekanik tunduk formula anti-cheat di modul `09`–`13`.
