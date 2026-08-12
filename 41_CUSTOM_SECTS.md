# 🏯 Wuxian World — Sekte, Dojo & Organisasi Kustom (Custom Sects)

> **Modul:** 41 — Custom Sects
> **Fungsi:** Tempat Admin mencatat Sekte/Dojo/Organisasi buatan pemain atau tambahan Admin.
> **Pengelolaan:** Hanya Admin (pemilik repo) yang boleh mengedit file ini. AI GM WAJIB membaca daftar ini saat pemain berinteraksi dengan sekte kustom.
> **Rujukan silang:** `14`–`37` (sekresmi), `09_CULTIVATION_LAW_SYSTEM.md` (Hukum yang digunakan)

---

## 📋 Cara Menggunakan File Ini

1. Setiap Sekte Kustom diberi **ID unik** (misal: `SECT-001`).
2. Sekte ini **bisa berasal dari**:
   - Kreasi Admin untuk memperkaya dunia.
   - Kreasi pemain yang disetujui Admin.
3. Sekte yang sudah dicatat di sini dianggap **RESMI** dan eksis di dunia.
4. AI GM WAJIB menggunakan data di sini saat berinteraksi dengan sekte tersebut.
5. Jika ada konflik dengan sekte di `14`–`37`, maka **Sekte di file ini (Custom) yang dianggap ada** untuk nama yang sama (jika duplikat).

---

## 📜 DAFTAR SEKTE/DOJO/ORGANISASI KUSTOM

### SECT-001: [Nama Sekte]
- **Tipe:** [Sekte Besar / Dojo / Organisasi Independen / Lintas Wilayah]
- **Afiliasi:** [Ortodoks / Demonic / Netral / Lainnya]
- **Wilayah:** [Wilayah utama sekte berada]
- **Lokasi Spesifik:** [Deskripsi lokasi markas]
- **Hukum Kultivasi:** [Nama Hukum — bisa dari `09` atau `40_CUSTOM_LAWS.md`]
- **Deskripsi Singkat:**
  [Sejarah, reputasi, dan karakteristik umum sekte]
- **Hierarki:**
  - [Pemimpin / Ketua]
  - [Tetua / Dewan]
  - [Murid Inti]
  - [Murid Luar]
- **Fasilitas Utama:**
  - [Fasilitas 1 — misal: Ruang Kultivasi]
  - [Fasilitas 2 — misal: Perpustakaan Teknik]
  - [Fasilitas 3]
- **Artefak/Pusaka:**
  - [Nama Artefak — efek singkat]
  - [Nama Artefak 2]
- **Kurikulum Teknik Bertingkat:**
  - **Tingkat Dasar:** [Teknik dasar]
  - **Tingkat Menengah:** [Teknik menengah]
  - **Tingkat Tinggi:** [Teknik tinggi]
- **Relasi dengan Faksi Lain:**
  - [Faksi 1]: [Hubungan — sekutu/musuh/netral]
  - [Faksi 2]: [Hubungan]
- **Rahasia Internal:**
  - [Rahasia 1]
  - [Rahasia 2]
- **NPC Utama:**

| NPC | Peran | Umur | Realm & Stage | Qi Cap | Teknik Andalan | Karakteristik |
|---|---|---|---|---|---|---|
| [Nama] | [Peran] | [Umur] | [Realm & Stage] | [Qi Cap] | [Teknik] | [Sifat] |
| [Nama] | [Peran] | [Umur] | [Realm & Stage] | [Qi Cap] | [Teknik] | [Sifat] |

- **Trigger untuk AI GM:**
  - Jika pemain berada di [lokasi], sampaikan [ciri khas sekte terlihat].
  - Jika pemain bertemu anggota sekte, NPC bersikap [sifat khas].
  - Jika pemain ingin bergabung, [syarat pendaftaran].
  - Jika pemain bermusuhan dengan sekte ini, [konsekuensi / reaksi].

---

### SECT-002: [Nama Sekte]
- **Tipe:** [Sekte Besar / Dojo / Organisasi Independen / Lintas Wilayah]
- **Afiliasi:** [Ortodoks / Demonic / Netral / Lainnya]
- **Wilayah:** [Wilayah]
- **Lokasi Spesifik:** [Deskripsi]
- **Hukum Kultivasi:** [Nama Hukum]
- **Deskripsi Singkat:**
  [Deskripsi]
- **Hierarki:**
  - [Pemimpin]
  - [Tetua]
- **Fasilitas Utama:**
  - [Fasilitas 1]
- **Artefak/Pusaka:**
  - [Artefak 1]
- **Kurikulum Teknik Bertingkat:**
  - **Tingkat Dasar:** [Teknik]
- **Relasi dengan Faksi Lain:**
  - [Faksi 1]: [Hubungan]
- **Rahasia Internal:**
  - [Rahasia 1]
- **NPC Utama:**

| NPC | Peran | Umur | Realm & Stage | Qi Cap | Teknik Andalan | Karakteristik |
|---|---|---|---|---|---|---|
| [Nama] | [Peran] | [Umur] | [Realm & Stage] | [Qi Cap] | [Teknik] | [Sifat] |

- **Trigger untuk AI GM:**
  - [Trigger 1]
  - [Trigger 2]

---

## 📝 Template Kosong untuk Admin

Salin template di bawah ini untuk menambahkan sekte baru:

```markdown
### SECT-XXX: [Nama Sekte]
- **Tipe:** [Sekte Besar / Dojo / Organisasi Independen / Lintas Wilayah]
- **Afiliasi:** [Ortodoks / Demonic / Netral / Lainnya]
- **Wilayah:** [Wilayah]
- **Lokasi Spesifik:** [Deskripsi lokasi]
- **Hukum Kultivasi:** [Nama Hukum]
- **Deskripsi Singkat:**
  [Tulis deskripsi di sini]
- **Hierarki:**
  - [Pemimpin / Ketua]
  - [Tetua / Dewan]
  - [Murid Inti]
  - [Murid Luar]
- **Fasilitas Utama:**
  - [Fasilitas 1]
  - [Fasilitas 2]
- **Artefak/Pusaka:**
  - [Nama Artefak — efek]
- **Kurikulum Teknik Bertingkat:**
  - **Tingkat Dasar:** [Teknik]
  - **Tingkat Menengah:** [Teknik]
  - **Tingkat Tinggi:** [Teknik]
- **Relasi dengan Faksi Lain:**
  - [Faksi 1]: [Hubungan]
- **Rahasia Internal:**
  - [Rahasia 1]
- **NPC Utama:**

| NPC | Peran | Umur | Realm & Stage | Qi Cap | Teknik Andalan | Karakteristik |
|---|---|---|---|---|---|---|
| [Nama] | [Peran] | [Umur] | [Realm & Stage] | [Qi Cap] | [Teknik] | [Sifat] |

- **Trigger untuk AI GM:**
  - [Trigger 1]
  - [Trigger 2]
