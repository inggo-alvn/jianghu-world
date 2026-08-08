# 📅 Wuxian World — Kalender Dunia & Timeline

> **Modul:** 38 — World Calendar & Timeline System
> **Tujuan:** Menetapkan titik mulai resmi kampanye dan mekanisme supaya dunia terasa hidup & terus berkembang seiring waktu in-game berjalan — bukan latar statis yang diam di tempat menunggu pemain.
> **Rujukan silang:** `00_CORE_RULES_AI_GM.md` §1.9 (Batasan Skala Waktu Aksi & checkpoint), `01`–`08` (umur NPC), `14`–`37` (Rahasia & Plot Hook tiap sekte), `10_ECONOMY_SYSTEM.md` §3.3 (Event Modifier)
> **Status:** Berlaku untuk kampanye baru mana pun mulai Agustus 2026. Kampanye yang sudah berjalan (mis. contoh Jiang Ziling di `players.md`) tetap sah — lihat §1.3 soal kompatibilitas mundur.

---

## 🗓️ 1. Titik Mulai Kampanye (Epoch)

### 1.1 Tanggal Resmi Mulai Dunia
```
Tahun 1, Kalender Tianyuan | Musim Semi | Tanggal 1 Bulan 1 | Hari Senin | Jam 06:00
```
Ini adalah **Tahun 1** — patokan waktu nol untuk SEMUA kampanye baru di Wuxian World, dinamai dari Dinasti Tianyuan yang berkuasa di Tianjing (`01_WORLD_OVERVIEW_AND_CAPITAL.md`). Setiap sesi pertama karakter baru (baik dari `players.md` maupun karakter custom, lihat `00_CORE_RULES_AI_GM.md` §1.6) dimulai persis di titik ini kecuali GM secara eksplisit menyatakan lain untuk kebutuhan cerita (mis. kampanye kedua yang sengaja dimulai di tahun berbeda).

### 1.2 Semua Umur NPC di World Bible Dihitung "Per Tahun 1"
Setiap umur NPC yang tertulis di `01`–`08` dan `14`–`37` (mis. "Kaisar Long Wei, 52 tahun") adalah umur mereka **tepat di Tahun 1, Musim Semi**. AI GM WAJIB menambah umur NPC sesuai jumlah tahun in-game yang sudah berlalu sejak Tahun 1 setiap kali NPC itu muncul kembali dalam cerita — bukan memakai umur tertulis selamanya secara statis.

```
UmurSaatIni(NPC) = UmurTahun1(NPC) + (TahunSaatIni − 1)
```

### 1.3 Kompatibilitas Mundur (Kampanye yang Sudah Berjalan)
Contoh karakter "Jiang Ziling" di `players.md` sudah memakai penanda "Tahun 1/2/3" sejak sebelum modul ini dibuat — penanda itu **otomatis kompatibel** dengan epoch resmi ini, tidak perlu diubah. Kampanye lama mana pun yang sudah memakai skema "Tahun N" sederhana bisa langsung dianggap selaras dengan §1.1 tanpa penyesuaian.

---

## 🎪 2. Peristiwa Berkala Terjadwal

AI GM WAJIB memicu peristiwa berikut secara otomatis begitu tanggal in-game mencapainya — bukan opsional, bukan menunggu pemain memintanya. Peristiwa ini terjadi di dunia terlepas dari apakah pemain terlibat langsung atau tidak (pemain hanya boleh MENYAKSIKAN/BERPARTISIPASI kalau kebetulan berada di lokasi & waktu yang tepat).

| Peristiwa | Lokasi | Siklus | Kejadian Berikutnya |
|---|---|---|---|
| **Turnamen Besar Lima Tahunan** | Danau Cermin, Central Plains (dijaga Heavenly Sword Pavilion & Profound Heaven Sect — lihat `02_CENTRAL_PLAINS.md`) | Tiap 5 tahun | Tahun 5, 10, 15, 20 dst. (tidak terjadi di Tahun 1) |
| **Turnamen Terbuka Immortal Peach Island** | Immortal Peach Island, Eastern Sea (`05_EASTERN_SEA_REGION.md`) | Tiap 60 tahun | Siklus terakhir jatuh di Tahun -46 (46 tahun sebelum Tahun 1) — kejadian berikutnya **Tahun 14** |
| 🆕 **Ujian Rekrutmen Tahunan** | Bergantian di sekte-sekte besar yang buka pendaftaran terbuka (Profound Heaven Sect, Silver Rain Sword School, Demonic Flame Palace Zona Luar, dll — lihat modul sekte masing-masing di `14`–`37`) | Tiap tahun, biasanya Musim Semi | Tiap Tahun N, Musim Semi |
| 🆕 **Musim Dagang Besar Pelabuhan Haiyun** | Kota Haiyun, Eastern Sea Region (`05_EASTERN_SEA_REGION.md`) | Tiap tahun, Musim Panas | Menaikkan `DemandIndex` & `EventModifier` (`10_ECONOMY_SYSTEM.md` §3.2–3.3) untuk barang impor selama musim berlangsung |
| 🆕 **Sensus & Pajak Kekaisaran** | Seluruh Central Plains, dikoordinasi dari Tianjing (`01_WORLD_OVERVIEW_AND_CAPITAL.md`) | Tiap tahun, Musim Gugur | Bisa memicu ketegangan lokal (pajak naik, korupsi pejabat kecil) sebagai hook cerita opsional bagi GM |

📌 **Anti-cheat:** Pemain tidak bisa memaksa peristiwa ini terjadi lebih awal/mundur lewat klaim sepihak — jadwalnya tetap terhadap kalender dunia, hanya AI GM yang boleh menyesuaikan narasi presisi tanggalnya (mis. "beberapa hari lebih awal karena cuaca") tanpa mengubah tahun siklusnya.

---

## ⏳ 3. Sistem Penuaan & Siklus Hidup NPC

### 3.1 Filosofi
Kultivator hidup jauh lebih lama sejalan realm mereka — trope klasik xianxia. Tabel di bawah ini **perkiraan umum**, bukan batas mati matematis, memberi AI GM pegangan realistis tanpa mengunci setiap NPC ke angka pasti.

| Realm | Perkiraan Rentang Usia Hidup |
|---|---|
| Non-Kultivator / Mortal Foundation | ~60–90 tahun (setara manusia biasa) |
| Qi Refining | ~80–120 tahun |
| Foundation Establishment | ~120–180 tahun |
| Core Formation | ~180–280 tahun |
| Nascent Soul | ~280–400 tahun |
| Soul Transformation | ~400–600 tahun |
| Void Severing | ~600–900 tahun |
| Tribulation Crossing | ~900–1.500 tahun |
| Immortal Ascension | Efektif nyaris abadi (ribuan tahun+) |

### 3.2 Aturan Wajib untuk AI GM
1. **Breakthrough memperpanjang usia** — begitu NPC/karakter breakthrough ke realm baru, "sisa umur"-nya otomatis mengikuti rentang realm barunya, bukan realm lama. Ini alasan mekanik kenapa kultivator mengejar breakthrough bukan cuma soal kekuatan.
2. **NPC yang mendekati batas atas rentang realm-nya boleh mengalami penurunan kondisi alami** (tenaga berkurang, lebih jarang bertindak langsung) sebagai bumbu naratif — TIDAK otomatis mati, kematian karena usia tua tetap keputusan naratif AI GM, bukan dadu otomatis.
3. **Kematian alami NPC penting** (bukan dibunuh, tapi wafat karena usia) boleh dipakai AI GM sebagai pemicu suksesi/pergantian kekuasaan di sekte terkait — beberapa "Rahasia & Plot Hook" di modul `14`–`37` (mis. Demonic Flame Palace §Rahasia soal Yan Wushen yang berusia 210 tahun tanpa penerus resmi) secara eksplisit dirancang untuk berkembang lewat mekanisme ini.
4. **Murid muda tumbuh dewasa** — NPC yang di Tahun 1 masih anak-anak/remaja (mis. Murid Baru Kecil Dawa, 14 tahun di Golden Bell Monastery) akan naik ke kategori dewasa muda dalam beberapa tahun in-game, membuka kemungkinan mereka naik tingkat hierarki di sekte masing-masing (lihat tabel Hierarki di file sekte terkait, `14`–`37`).

---

## 🌍 4. Evolusi Dunia Seiring Waktu (Mekanisme Inti)

Ini bagian paling penting: **semakin lama karakter pemain hidup/bermain, dunia tidak boleh terasa diam.** AI GM WAJIB menjalankan checklist berikut setiap kali terjadi **checkpoint waktu signifikan** (lompatan kultivasi berhari-hari/berminggu per `00_CORE_RULES_AI_GM.md` §1.9, pergantian musim, atau minimal sekali per Tahun in-game yang berlalu):

### 4.1 Checklist Perkembangan Dunia per Checkpoint
- [ ] **Peristiwa berkala** (§2) — apakah ada yang jatuh tempo sejak checkpoint terakhir? Jika ya, narasikan (minimal sebagai kabar/gosip yang didengar karakter, meski tak hadir langsung).
- [ ] **Penuaan NPC signifikan** (§3) — apakah NPC kunci yang relevan dengan cerita sudah lama tidak disebut dan seharusnya sudah menua/breakthrough/wafat secara wajar?
- [ ] **Progres "Rahasia & Plot Hook"** — pilih **1–2 rahasia internal sekte** (dari `14`–`37`, biasanya yang relevan dengan wilayah/sekte yang pernah disinggung cerita) dan majukan sedikit di latar belakang, meski karakter tidak terlibat langsung. Contoh: ketegangan suksesi di Profound Heaven Sect (Bai Lu vs Yu Cang) boleh diam-diam memburuk; rumor alumnus legendaris Dojo Bunga Aprikot boleh muncul lagi lewat NPC baru.
- [ ] **Drift ekonomi** — `DemandIndex` & `RegionScarcity` (`10_ECONOMY_SYSTEM.md` §3) boleh bergeser wajar akibat waktu berlalu (panen, perang kecil, musim dagang) — tidak perlu derajat presisi tinggi, cukup make sense secara naratif.
- [ ] **Konsekuensi tindakan pemain sebelumnya** — apakah ada aksi besar pemain (membunuh tokoh penting, membantu sekte tertentu, dll — sesuai `00_CORE_RULES_AI_GM.md` §1.4 & §1.8) yang cukup waktu untuk menimbulkan efek riak lanjutan (balas dendam, ucapan terima kasih, perubahan reputasi)?

### 4.2 Prinsip Show, Don't Dump
AI GM **tidak perlu** membacakan checklist di atas secara harfiah ke pemain — cukup selipkan hasilnya secara alami dalam narasi (kabar dari pedagang lewat, gosip di kedai teh, surat dari kenalan lama, perubahan kecil di kota yang disinggahi ulang). Tujuannya dunia terasa berjalan sendiri, bukan sekadar panggung statis menunggu aksi pemain.

### 4.3 Contoh Penerapan
> *Karakter kembali ke Kota Luoyang Kecil setelah 3 tahun in-game berkelana. AI GM: memeriksa checklist §4.1 → Turnamen Besar Lima Tahunan baru saja lewat (Tahun 5) → murid-murid sekte yang dulu remaja kini sudah naik tingkat → harga barang impor sedikit naik karena Musim Dagang Haiyun tahun itu kurang ramai → NPC Kepala Serikat Wang Fu (55 tahun di Tahun 1) kini 58 tahun, mulai mendelegasikan urusan ke asisten mudanya. Semua ini diselipkan lewat dialog & deskripsi singkat, bukan info-dump.*

---

## 🛡️ 5. Checklist Integrasi AI GM

- [ ] Sesi baru (karakter benar-benar baru) dimulai dari Tahun 1 kecuali GM menyatakan lain secara eksplisit?
- [ ] Umur NPC yang disebut kembali dalam cerita disesuaikan dengan Tahun berjalan (§1.2), bukan angka statis dari file sumber?
- [ ] Peristiwa berkala (§2) dipicu tepat waktu, tidak dilewatkan maupun dimajukan sepihak oleh klaim pemain?
- [ ] Checkpoint waktu signifikan memicu peninjauan checklist §4.1, minimal sekali per Tahun in-game yang terlewati?
- [ ] Perubahan dunia diselipkan naratif (§4.2), bukan dibacakan sebagai daftar mentah ke pemain?

Jika salah satu poin di atas terlewat dalam sesi panjang, AI GM boleh "mengejar ketertinggalan" secara retroaktif di checkpoint berikutnya — dunia yang sedikit terlambat berkembang lebih baik daripada dunia yang sama sekali tidak berkembang.
