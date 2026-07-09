# 🐉 Wuxian World — Bestiarium (Monster & Spirit Beast System)

> **Modul:** 13 — Bestiary
> **Anti-Cheat Enforced — Region-Locked Encounter**
> **Rujukan silang:** `09_CULTIVATION_LAW_SYSTEM.md` (QiCap & bahan terobosan), `10_ECONOMY_SYSTEM.md` (Tier/Grade loot & Item Origin Log), `11_VITALITY_HUNGER_SYSTEM.md` (HP), `12_COMBAT_SYSTEM.md` (resolusi pertarungan), `02`–`07` (lokasi/habitat regional)

---

## 🧭 0. Filosofi Sistem

Monster di dunia ini bukan sekadar dekorasi — mereka punya HP dan Attack Power yang tunduk pada formula yang **sama** seperti kultivator (memakai `QiCap` dari `09_CULTIVATION_LAW_SYSTEM.md`), sehingga kekuatan monster selalu konsisten dan tidak bisa "dikarang" AI GM sesukanya di tengah cerita, dan tidak bisa diremehkan/dilebih-lebihkan sepihak oleh player. Sebagian monster menyerang tiba-tiba (ambush) sesuai mekanik §3 — bukan keputusan sepihak player kapan monster muncul.

### Aturan Emas Anti-Cheat Monster
- HP & Attack Power monster dihitung dari formula (§2), **tidak bisa dideklarasikan sepihak oleh player** ("monster ini pasti lemah" tanpa dasar = ditolak).
- Kemunculan monster (terutama ambush) ditentukan lewat `AmbushChance` (§3), dilempar oleh AI GM, bukan diminta/dihindari sepihak oleh player di luar konteks naratif wajar.
- Loot drop tunduk pada tabel §4 dan Item Origin Log Sistem Ekonomi — tidak ada loot yang "muncul begitu saja" tanpa monster benar-benar dikalahkan dalam roleplay.
- Monster Tier tinggi (6+) tidak bisa muncul di luar habitat resminya (§5) — mencegah "power creep" naratif berupa monster kuat muncul sembarangan di zona lemah.
- Farming/grinding berulang di titik yang sama dibatasi respawn cooldown naratif (minimum beberapa hari in-game per individu monster bernama/unik, sesuai populasi wajar wilayah tersebut).

---

## 🐾 1. Kategori Monster

Setiap monster masuk salah satu dari 6 kategori berikut, yang menentukan Multiplier HP & Attack-nya:

| Kategori | HP Multiplier | Attack Multiplier | Sifat Umum |
|---|---|---|---|
| 🐺 Spirit Beast (妖兽) | ×1,2 | ×1,0 | Hewan berkultivasi alami, seimbang, umum ditemukan di hutan/gunung |
| 👤 Bayangan/Yin Creature (阴兽) | ×0,6 | ×1,5 | Rapuh tapi mematikan di serangan pertama — spesialis ambush, aktif malam hari |
| 🔥 Elemental (元素兽) | ×1,0 | ×1,2 | Terikat elemen wilayah asal (api, es, racun, air), punya resistensi/kelemahan elemen berlawanan |
| 🗿 Ancient Guardian (远古守护兽) | ×2,0 | ×1,8 | Sangat kuat, penjaga reruntuhan/harta karun kuno, langka & bertahan lama |
| 👻 Undead/Roh (亡灵) | ×0,9 | ×0,9 | Kebal racun & efek mental, lemah terhadap teknik suci/welas asih (mis. Azure Cloud Temple) |
| 🐛 Insect/Gu Swarm (蛊虫群) | ×0,4 (per individu) | ×0,3 (per individu) | Lemah sendirian, berbahaya dalam kawanan besar (kalikan jumlah individu) |

---

## ⚔️ 2. Formula HP & Attack Power Monster

```
MonsterQiCap(realm, stage) = QiCap(realm, stage)   [tabel sama seperti 09_CULTIVATION_LAW_SYSTEM.md]

MonsterHP = MonsterQiCap × K_HP_Beast × CategoryHPMultiplier
K_HP_Beast = 0,5   (sedikit lebih tinggi dari kultivator K_HP=0,4 — ketahanan alami tubuh hewan/makhluk buas)

MonsterAttackPower = MonsterQiCap × 0,15 × CategoryAttackMultiplier
```

📌 **Anti-cheat:** satu serangan monster standar TIDAK BOLEH melebihi `MonsterAttackPower` yang dihitung — serangan "ultimate"/jurus andalan boleh mengeluarkan hingga ×3 Attack Power tapi hanya sekali per beberapa giliran (cooldown ditentukan GM), bukan tiap serangan.

---

## 🌙 3. Sistem Ambush & Perjumpaan Acak (Random Encounter)

```
AmbushChance = BaseAmbushChance × DangerModifier × TimeModifier
BaseAmbushChance = 5% per jam perjalanan melintasi wilayah berpenghuni monster
```

| Modifier | Nilai |
|---|---|
| DangerModifier — Wilayah Normal | ×1,0 |
| DangerModifier — Wilayah Liar/Hutan Belantara | ×2,0 |
| DangerModifier — Zona Terlarang | ×4,0 |
| TimeModifier — Siang hari | ×1,0 |
| TimeModifier — Malam hari | ×2,0 (mayoritas monster, khususnya Bayangan/Yin, lebih aktif malam) |

**Contoh:** melintasi Endless Primeval Forest (Zona Liar, ×2,0) di malam hari (×2,0): `AmbushChance = 5% × 2,0 × 2,0 = 20% per jam perjalanan`.

📌 **Anti-cheat:** AI GM yang melempar kemungkinan ambush tiap interval perjalanan — bukan player memutuskan sendiri "monster muncul" atau "tidak ada monster sama sekali" tanpa alasan naratif kuat (seperti membawa jimat pengusir/formasi pelindung tervalidasi).

---

## 💎 4. Sistem Drop Loot

`LootDropRate = BaseDropRate(rarity)` — dilempar AI GM **setelah** monster benar-benar dikalahkan dalam roleplay.

| Rarity | BaseDropRate | Contoh |
|---|---|---|
| Umum (Common) — bahan dasar tubuh monster | 70–90% | Kulit, taring, bulu, inti qi kecil |
| Jarang (Rare) — organ/inti spiritual | 20–40% | Inti elemen, kelenjar racun, sisik langka |
| Legendaris (hanya monster Ancient Guardian/boss) | 5–15%, atau 100% sekali seumur (unique kill pertama) | Pusaka/bahan Tier 7+, artefak bernama |

Semua loot mengikuti Tier & Grade Sistem Ekonomi (`10_ECONOMY_SYSTEM.md` §2) sesuai Tier monster tersebut, dan **WAJIB dicatat di Item Origin Log** sebelum bisa dijual/dipakai breakthrough (`10_ECONOMY_SYSTEM.md` §7).

---

## 📖 5. Daftar Monster per Wilayah

### Central Plains
*(lihat `02_CENTRAL_PLAINS.md`)*

| Monster | Kategori | Tier (Realm Setara) | HP | Attack Power | Kemampuan & Deskripsi | Loot Drop |
|---|---|---|---|---|---|---|
| Roh Prajurit Gugur | 👻 Undead | 3, Awal | 1.125 | 337 | Muncul dari Ancient Battlefield of Gods, mengembara membawa tombak karatan, menyerang siapa pun yang dianggap "musuh lama"-nya yang sudah lama mati. Kebal senjata fisik biasa, hanya bisa dilukai qi. | Umum: Serpihan Baju Zirah Kuno (Tier 2) — Jarang: Inti Roh Prajurit (Tier 4, bahan Hukum Roh Hantu) |
| Naga Sungai Kecil | 🐺 Spirit Beast | 2, Menengah | 450 | 112 | Menghuni Sungai Emas & Golden River Basin, menyerang perahu kecil yang lewat malam hari, gemar mengoleksi barang mengkilap yang jatuh ke sungai. | Umum: Sisik Naga Sungai (Tier 1) — Jarang: Mutiara Sungai Kecil (Tier 3) |
| Macan Gunung Tri-Sect | 🐺 Spirit Beast | 3, Menengah | 2.250 | 562 | Sangat teritorial di lereng Tri-Sect Mountain, sering jadi alasan sekte-sekte menghindari area tertentu gunung ini selain sengketa klaim wilayah. | Umum: Kulit Macan Gunung (Tier 2) — Jarang: Taring Macan Bertuah (Tier 3) |

### Azure Mountain Range
*(lihat `03_AZURE_MOUNTAIN_RANGE.md`)*

| Monster | Kategori | Tier (Realm Setara) | HP | Attack Power | Kemampuan & Deskripsi | Loot Drop |
|---|---|---|---|---|---|---|
| Kabut Pemakan Arah | 👤 Bayangan/Yin | 5, Awal | 18.750 | 14.062 | Menghuni Void Mist Forest, tak berwujud jelas — hanya kabut tebal yang membingungkan indra arah korban hingga tersesat selamanya. Menyerang dari segala arah sekaligus tanpa peringatan. | Umum: Esens Kabut Sesat (Tier 4) — Jarang: Inti Disorientasi (Tier 5, bahan formasi ilusi) |
| Ular Salju Lembah Bunga | 🔥 Elemental (Es/Racun) | 2, Awal | 250 | 90 | Menjaga Lembah Bunga Salju secara alami, bisanya justru jadi bahan penawar racun langka yang diperebutkan Whitecloud Medicine Hall & Nine Serpent Den. | Umum: Bisa Ular Salju (Tier 1) — Jarang: Kelenjar Penawar Langka (Tier 3) |
| Burung Guntur Puncak | 🔥 Elemental (Petir) | 4, Menengah | 9.375 | 3.375 | Bersarang di Heaven Reaching Peak, menyerang dengan sambaran petir kecil saat merasa sarangnya terancam, sangat sensitif pada pendaki yang berisik. | Umum: Bulu Berlistrik (Tier 3) — Jarang: Inti Guntur Kecil (Tier 4, bahan formasi petir) |

### Southern Demon Domain
*(lihat `04_SOUTHERN_DEMON_DOMAIN.md`)*

| Monster | Kategori | Tier (Realm Setara) | HP | Attack Power | Kemampuan & Deskripsi | Loot Drop |
|---|---|---|---|---|---|---|
| Serigala Api Neraka | 🔥 Elemental (Api) | 4, Awal | 6.250 | 2.250 | Penghuni asli Hellfire Island, sengaja dipakai Demonic Flame Palace sebagai "makhluk uji" murid Zona Luar & Tengah pulau ujian. Kulitnya membara terus-menerus. | Umum: Bulu Api Abadi (Tier 3) — Jarang: Inti Api Serigala (Tier 4, bahan Hukum Qi Naga Api) |
| Ular Berbisa Liar Rawa | 🔥 Elemental (Racun) | 3, Awal | 1.250 | 450 | Berkeliaran liar di Thousand Poison Marsh, tidak berafiliasi dengan Nine Serpent Den, kadang malah diburu sekte tersebut untuk diambil bisanya. | Umum: Bisa Ular Rawa (Tier 2) — Jarang: Kulit Ular Kebal Racun (Tier 3) |
| Kutu Iblis Pemakan Qi | 🐛 Insect/Gu Swarm | 1, Puncak (per individu) | 40 (×20–50 individu) | 9 (per individu, menumpuk) | Menghuni Endless Primeval Forest dalam kawanan besar, tiap gigitan menyedot sedikit Qi korban — berbahaya bukan karena kuat sendiri, tapi karena jumlahnya. | Umum: Cangkang Kutu Iblis (Tier 1, dijual per kilo) — Jarang: Inti Kawanan (Tier 2, hanya drop dari kutu ratu) |
| Mayat Hidup Rawa Jiwa Tenggelam | 👻 Undead | 5, Menengah | 42.187 | 12.656 | Penghuni Rawa Jiwa Tenggelam, ditakuti bahkan oleh Ghost Valley Sect sendiri. Bergerak lambat tapi cengkeramannya menyerap vitalitas korban perlahan. | Umum: Daging Membusuk Bertuah (Tier 4) — Jarang: Inti Jiwa Tenggelam (Tier 5, bahan Hukum Roh Hantu langka) |
| Kalajengking Raksasa Abu Vulkanik | 🐺 Spirit Beast | 3, Puncak | 3.000 | 750 | Menghuni Perbukitan Abu Vulkanik, kulitnya tahan panas ekstrem, sengatannya melumpuhkan sementara. | Umum: Cangkang Kalajengking (Tier 2) — Jarang: Racun Sengat Vulkanik (Tier 3) |

### Eastern Sea Region
*(lihat `05_EASTERN_SEA_REGION.md`)*

| Monster | Kategori | Tier (Realm Setara) | HP | Attack Power | Kemampuan & Deskripsi | Loot Drop |
|---|---|---|---|---|---|---|
| Kraken Muda Laut Timur | 🔥 Elemental (Air) | 5, Puncak | 62.500 | 22.500 | Menghuni perairan dalam Eastern Sea, menyerang kapal besar yang berlayar terlalu jauh dari jalur aman, tentakelnya bisa menghancurkan lambung kapal kecil dalam sekali lilitan. | Umum: Tentakel Kraken (Tier 4) — Jarang: Inti Air Dalam (Tier 5, bahan Hukum Dao Abadi varian Air) |
| Siput Mutiara Iblis | 🐺 Spirit Beast | 2, Awal | 300 | 75 | Bersembunyi di dasar laut dekat Desa Zhenzhu, cangkangnya berisi mutiara spiritual palsu yang bisa meledak jadi racun jika dipaksa dibuka tanpa teknik yang benar. | Umum: Cangkang Siput (Tier 1) — Jarang: Mutiara Semu (Tier 2, bisa dimurnikan jadi Mutiara Spiritual asli oleh tabib ahli) |
| Hiu Sentinel Liar | 🐺 Spirit Beast | 3, Menengah | 2.250 | 562 | Varian liar dari hiu yang biasa dijinakkan Jade Purity Palace, agresif pada siapa pun yang bukan anggota sekte tersebut. | Umum: Kulit Hiu Sentinel (Tier 2) — Jarang: Gigi Hiu Bertuah (Tier 3) |
| Kawanan Camar Badai | 🐛 Insect/Gu Swarm (setara) | 1, Awal (per individu) | 20 (×10–30 ekor) | 4,5 (per individu) | Berkerumun di sekitar Floating Cloud Archipelago saat badai, lebih mengganggu daripada mematikan, tapi bisa membutakan pandangan pelaut dalam jumlah besar. | Umum: Bulu Camar (Tier 1, dijual per ikat) |

### Northern Desolate Territory
*(lihat `06_NORTHERN_DESOLATE_TERRITORY.md`)*

| Monster | Kategori | Tier (Realm Setara) | HP | Attack Power | Kemampuan & Deskripsi | Loot Drop |
|---|---|---|---|---|---|---|
| Serigala Es Abadi | 🗿 Ancient Guardian | 6, Awal | 312.500 | 84.375 | Penghuni legendaris Eternal Frost Peak, dipercaya sudah hidup ratusan tahun, auranya bisa membekukan darah dari jarak jauh. Sangat jarang terlihat langsung. | Umum: Bulu Es Abadi (Tier 5) — Legendaris: Inti Es Purba (Tier 7, bahan Tribulasi Realm 7→8 varian es) |
| Roh Beku Bukit Tulang | 👻 Undead | 4, Awal | 5.625 | 1.687 | Menghuni Bukit Tulang Beku, sisa jenderal-jenderal kuno yang gugur, mengembara mencari "pasukan" untuk direkrut kembali — berbahaya bagi yang lewat sendirian di malam hari. | Umum: Serpihan Tulang Beku (Tier 3) — Jarang: Inti Roh Jenderal (Tier 4) |
| Beruang Salju Raksasa | 🐺 Spirit Beast | 3, Menengah | 2.250 | 562 | Menghuni sekitar Desa Xueying, biasanya tidak menyerang kecuali sarangnya terancam atau musim dingin ekstrem membuatnya kelaparan. | Umum: Kulit Beruang Salju (Tier 2) — Jarang: Cakar Beruang Bertuah (Tier 3) |
| Angin Menjerit Berwujud | 🔥 Elemental (Angin/Suara) | 4, Menengah | 9.375 | 3.375 | Menghuni Lembah Angin Menjerit, berwujud pusaran angin yang mengeluarkan suara mirip jeritan manusia, bisa merobek kulit tanpa perlindungan Qi. | Umum: Esens Angin Menjerit (Tier 3) — Jarang: Inti Suara Ganas (Tier 4, bahan formasi suara) |
| Rubah Es Berekor Sembilan | 🐺 Spirit Beast (Langka) | 6, Menengah | 281.250 | 70.312 | Sangat jarang terlihat, dipercaya sebagai pertanda keberuntungan atau bencana tergantung sikap yang menemuinya. Berkelana bebas di seluruh Northern Territory. | Umum: Bulu Ekor Rubah (Tier 5) — Legendaris: Inti Rubah Sembilan Ekor (Tier 6, sangat diburu alkemis) |

### Western Sacred Deserts
*(lihat `07_WESTERN_SACRED_DESERTS.md`)*

| Monster | Kategori | Tier (Realm Setara) | HP | Attack Power | Kemampuan & Deskripsi | Loot Drop |
|---|---|---|---|---|---|---|
| Cacing Pasir Raksasa | 🐺 Spirit Beast | 5, Awal | 37.500 | 9.375 | Bersembunyi di bawah Bukit Pasir Menyanyi dan sekitarnya, menyerang dari bawah tanah tanpa peringatan — alasan utama kafilah selalu bergerak berkelompok dan tak pernah berjalan sendirian di gurun terbuka. | Umum: Kulit Cacing Pasir (Tier 4) — Jarang: Inti Getaran Bawah Tanah (Tier 5) |
| Elang Pasir Iblis | 🐺 Spirit Beast | 3, Awal | 1.500 | 375 | Menyambar dari udara di sekitar Reruntuhan Gushatta, sering mengincar barang mengkilap yang dibawa penjelajah. | Umum: Bulu Elang Pasir (Tier 2) — Jarang: Cakar Elang Bertuah (Tier 3) |
| Skorpion Emas Legendaris | 🗿 Ancient Guardian | 6, Puncak | 625.000 | 168.750 | Penjaga tak resmi Formasi Batu Buddha Tidur, konon terikat sumpah kuno menjaga reruntuhan biara — hanya menyerang mereka yang mencoba merusak formasi, damai pada peziarah biasa. | Umum: Cangkang Skorpion Emas (Tier 5) — Legendaris: Racun Emas Purba (Tier 7, bahan langka Hukum Gu Karma) |

### Monster Langka Lintas Wilayah (Rare/Boss Tier)
*Bisa muncul di beberapa zona terlarang, tidak terikat satu wilayah saja.*

| Monster | Kategori | Tier (Realm Setara) | HP | Attack Power | Kemampuan & Deskripsi | Loot Drop |
|---|---|---|---|---|---|---|
| Bayangan Tanpa Wujud | 👤 Bayangan/Yin | 5, Menengah | 28.125 | 21.093 | Berkelana acak di zona-zona gelap seluruh dunia (hutan malam, reruntuhan, lembah berkabut) — tak punya habitat tetap, muncul lalu menghilang tanpa jejak begitu kehilangan lebih dari 50% HP-nya, membuatnya nyaris mustahil dikalahkan sepenuhnya. | Umum: Esens Bayangan (Tier 4) — hanya drop jika berhasil dipojokkan sampai HP 0% sekaligus (sangat sulit) |
| Naga Kabut Purba | 🗿 Ancient Guardian (Boss Langka) | 8, Awal | 7.812.500 | 2.109.375 | Legenda hidup yang konon menjaga rahasia Immortal Peach Island & Ancient Battlefield of Gods secara bergantian, hanya muncul saat formasi kuno terganggu serius. Pertarungan dengannya setara peristiwa besar dalam cerita, bukan encounter biasa. | Legendaris (100% sekali kill pertama): Sisik Naga Purba (Tier 8, bahan Tribulasi Realm 8→9) + Insight Point otomatis untuk semua yang terlibat pertarungan |

---

## ⚖️ 6. Checklist Anti-Cheat Monster

- [ ] HP & Attack Power monster dihitung dari formula §2, bukan klaim sepihak?
- [ ] Kemunculan (terutama ambush) dilempar via `AmbushChance` §3 oleh AI GM, bukan diatur sepihak player?
- [ ] Monster Tier 6+ hanya muncul di habitat resminya (§5), tidak di zona tak sesuai?
- [ ] Loot hanya didapat setelah monster benar-benar dikalahkan dalam roleplay, dicatat di Item Origin Log?
- [ ] Serangan "ultimate" monster (>×1 Attack Power normal) dibatasi cooldown, tidak dipakai tiap giliran?
- [ ] Respawn monster unik/bernama dibatasi cooldown naratif wajar, tidak di-farming berulang dalam waktu singkat?

Jika salah satu poin gagal → encounter/loot DITOLAK atau dikoreksi AI GM.

---

## 🗺️ 7. Integrasi dengan Sistem Lain

- **Dengan Sistem Hukum Kultivasi** (`09_CULTIVATION_LAW_SYSTEM.md`): `MonsterQiCap` memakai tabel QiCap yang sama, dan loot monster tertentu langsung dipetakan ke Bahan Terobosan per Hukum (mis. Serigala Api Neraka → bahan Hukum Qi Naga Api, Mayat Hidup Rawa Jiwa Tenggelam → bahan Hukum Roh Hantu) sesuai §8.5 file tersebut.
- **Dengan Sistem Ekonomi** (`10_ECONOMY_SYSTEM.md`): semua loot tunduk Tier & Grade serta `FinalPrice` formula saat dijual, dan WAJIB Item Origin Log sebelum ditransaksikan.
- **Dengan Sistem HP** (`11_VITALITY_HUNGER_SYSTEM.md`): HP monster & player dihitung dari formula yang sama (basis QiCap), sehingga pertarungan tetap seimbang dan bisa diprediksi tanpa power creep sepihak dari kedua sisi.
- **Dengan Sistem Pertempuran** (`12_COMBAT_SYSTEM.md`): MonsterAttackPower & MonsterHP langsung dipakai tanpa konversi tambahan — monster dan kultivator bertarung dengan sistem identik.
- **Dengan modul regional** (`01`–`07`): tiap monster terkunci ke habitat spesifik yang sudah ditetapkan (Void Mist Forest, Hellfire Island, Rawa Jiwa Tenggelam, dsb) — mencegah monster tingkat tinggi muncul di zona yang seharusnya aman seperti Kota Fengyang atau Floating Cloud Archipelago (pasar netral).
