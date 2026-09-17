# 📄 PRODUCT REQUIREMENT DOCUMENT (PRD)
## Official Class Website & 3D Virtual Memory Museum — XII PPLG 1 SMKN 1 Depok

---

| Dokumen | Keterangan |
| :--- | :--- |
| **Nama Produk** | Website Resmi & Virtual Memory Museum XII PPLG 1 |
| **Edisi Desain** | Pure Neobrutalism Interactive Edition |
| **Instansi / Sekolah** | SMK Negeri 1 Depok (OneDek) |
| **Program Keahlian** | Pengembangan Perangkat Lunak dan Gim (PPLG) |
| **Angkatan** | 2024 – 2027 (Masuk 2024, Target Kelulusan 2027) |
| **Versi Dokumen** | 1.2.0 (Production Ready) |
| **Tanggal Pembaruan**| September 2026 |
| **Status Dokumen** | Approved & Implemented |
| **Lisensi / Hak Cipta**| Proprietary — Hak Cipta Eksklusif Angkatan XII PPLG 1 |

---

## 1. Executive Summary & Visi Produk

### 1.1 Latar Belakang (Background)
Kelas **XII PPLG 1 SMK Negeri 1 Depok** adalah program kejuruan unggulan yang berfokus pada rekayasa perangkat lunak, pemrograman web & mobile, serta pengembangan gim dan aset 3D. Selama menempuh pendidikan dari tahun 2024 hingga 2027, banyak momen kebersamaan, arsip karya praktikum, dan kenangan autentik yang terbentuk. 

Alih-alih mendokumentasikan memori kelas melalui media sosial konvensional atau album kenangan statis, kelas berinisiatif membangun **platform digital interaktif terintegrasi**. Platform ini tidak hanya menjadi wadah arsip kenangan, tetapi juga menjadi etalase (*showcase*) kemampuan rekayasa perangkat lunak tingkat lanjut (Next.js 16, React 19, dan visualisasi 3D Three.js WebGL) yang berani tampil beda dengan filosofi desain **Neobrutalism**.

### 1.2 Pernyataan Visi (Vision Statement)
> *"Menciptakan ruang arsip digital dan museum virtual 3D interaktif yang mengabadikan 35 murid, guru, dan 57 karya kenangan XII PPLG 1 SMKN 1 Depok dengan performa tinggi, stabilitas mobile tanpa crash, serta identitas desain Neobrutalism yang tegas dan berani."*

### 1.3 Nilai Inti & Slogan Kelas
- **Slogan Angkatan:** *“Logic, Code, and Creativity — Berjuang bersama, maju bersama.”*
- **Karakter Desain:** Pure Neobrutalism — warna kuning-hitam-putih berani, *hard solid shadows*, border kontras tinggi, tipografi tegas, dan minim gradien halus.

---

## 2. Tujuan Produk & Key Performance Indicators (KPIs)

### 2.1 Tujuan Utama (Core Objectives)
1. **Representasi Otentik 35 Murid**: Menampilkan profil, meja kerja, peran, dan kutipan unik masing-masing siswa secara presisi di ruang kelas virtual 3D.
2. **Museum Kenangan 3D Generasi Baru**: Menghadirkan galeri seni virtual dengan 57 bingkai karya asli (Kelas 10 & 11), monumen laptop 3D melayang, dan dashboard telemetri kelas.
3. **Stabilitas & Aksesibilitas Mobile 100%**: Memastikan visualisasi 3D WebGL berjalan mulus pada ponsel pintar (HP Android & iOS) tanpa menyebabkan browser crash (*Out of Memory*).
4. **Dual-Mode Experience**: Memberikan fleksibilitas bagi pengguna dengan menyediakan mode Museum 3D interaktif dan mode Grid 2D konvensional berfitur live-search.

### 2.2 Metrik Keberhasilan (Success Metrics / KPIs)
- **Zero Mobile Crash Rate**: 0% crash/tab reload di Chrome Mobile berkat sistem auto-downscaling tekstur (VRAM < 50 MB).
- **First Contentful Paint (FCP)**: < 1.2 detik menggunakan Next.js 16 App Router & Turbopack.
- **Zero-Wait 3D Transition**: Waktu perpindahan dari Mode 2D ke Mode Museum 3D sebesar 0 detik (*instant swap*) melalui sistem *background pre-rendering*.
- **Akurasi Data**: 100% data terverifikasi (35 siswa: 22 laki-laki & 13 perempuan, 57 foto tanpa duplikasi).

---

## 3. User Personas & Alur Pengguna (User Flow)

### 3.1 Target Pengguna (User Personas)
1. **Siswa & Siswi XII PPLG 1**: Mengenang perjalanan kelas, melihat meja virtual, dan membagikan tautan portofolio kelas.
2. **Guru & Wali Kelas**: Menginspeksi tata letak kelas, rekapitulasi siswa, dan memantau capaian praktikum kejuruan.
3. **Pihak Luar (Industri, Alumni, & Calon Siswa)**: Menilai kompetensi teknis siswa PPLG SMKN 1 Depok dalam ekosistem web modern dan teknologi 3D.

### 3.2 Alur Pengguna Utama (Core User Flow)
```text
Landing di Website (Hero 100dvh)
  ├── 1. Running Logo Tech Stack (15 Tools)
  ├── 2. Denah Kelas 3D Lab Komputer (35 Meja PC Siswa + Meja Guru)
  │      ├── Orbit 360° / Preset Kamera
  │      ├── Hover Meja (Glow Kuning) -> Klik Meja -> Modal Profil Siswa
  │      └── Input Pencarian Nama Siswa -> Kamera Menyorot Meja
  ├── 3. Bagan Struktur Organisasi Kelas (8 Pengurus Inti)
  ├── 4. Galeri Memori Dual-Mode:
  │      ├── [Mode Grid 2D Default]:
  │      │    ├── Filter Kategori (All / Kelas 10 / Kelas 11)
  │      │    ├── Real-Time Search Bar
  │      │    ├── Pagination Bertahap (+6 Foto)
  │      │    └── Klik Foto -> Lightbox Modal (Resolusi Penuh)
  │      └── [Klik Button: Mode Museum 3D Virtual]:
  │           └── Tampil Seketika (Foto Sudah Di-Pre-Render di Background)
  │                ├── Navigasi Bebas 360°
  │                ├── Preset Sudut Pandang (Hall, Sayap K10, Sayap K11, Laptop, Dashboard)
  │                ├── Tur Otomatis (Guided Tour Step-by-Step)
  │                ├── Sorot Pigura -> Zoom Focus & Modal Kurator
  │                └── Interaksi Layar Dashboard Statistik Kelas
  ├── 5. Dual-Directional Marquee (Nama 35 Siswa & Slogan)
  └── 6. Footer & Link Resmi Instagram (@12pplg1_)
```

---

## 4. Arsitektur Teknis & Tech Stack

### 4.1 Spesifikasi Teknologi (Technical Stack)
| Layer | Teknologi | Versi | Alasan Pemilihan |
| :--- | :--- | :--- | :--- |
| **Framework** | Next.js (App Router) | 16.3.0 | Turbopack cepat, Server-Side Optimization, Zero-config build. |
| **Core UI** | React | 19.2.8 | Lifecycle modern, hooks performa tinggi, konkurensi mulus. |
| **3D Graphics** | Three.js | 0.182+ | Standar industri WebGL, ringan, kontrol penuh atas shader & geometry. |
| **Styling** | Tailwind CSS | v4.0.0 | Desain token Neobrutalism terstandarisasi, utility classes fleksibel. |
| **Motion/Anim**| Framer Motion | v13.0 | Animasi layout springs, enter/exit lightbox modal halus. |
| **Language** | TypeScript | 5.0+ | Type safety ketat untuk mock data, Three.js vectors, dan props. |
| **Icons** | Lucide React | Latest | Ikon clean bergaris tebal (*stroke-width 2.5–3*) khas Neobrutalism. |
| **Tipografi** | Space Grotesk | Google Font | Font sans geometris berkarakter tegas dan modern. |

### 4.2 Struktur Direktori Proyek
```text
website-kelas/
├── app/
│   ├── globals.css              # Custom styling, Tailwind v4 theme, utility neobrutalism, marquee
│   ├── layout.tsx               # Root Layout, font Space Grotesk, SEO metadata, Favicon
│   └── page.tsx                 # Entry page: perakitan modular seluruh komponen
├── public/
│   ├── asset-song/              # Lagu latar: God Bless - Rumah Kita (MP3)
│   ├── asset-techstack/         # 15 file logo teknologi & kejuruan PPLG
│   ├── Kelas 10/                # 42 foto autentik kenangan kelas 10
│   ├── Kelas 11/                # 15 foto autentik kenangan kelas 11
│   ├── logo-onedek.jpeg         # Logo resmi SMKN 1 Depok
│   └── logo pplg.jpeg           # Logo resmi jurusan PPLG
├── src/
│   ├── components/
│   │   ├── BackToTop.tsx        # Floating button kembali ke puncak halaman
│   │   ├── Classroom3D.tsx      # Denah 3D Lab Komputer 35 Meja Siswa + Meja Guru
│   │   ├── Gallery.tsx          # Wrapper Galeri Dual-Mode (Museum 3D + Grid 2D)
│   │   ├── Hero.tsx             # Header Hero Neobrutalism 100dvh
│   │   ├── MemoryMuseum3D.tsx   # Pameran 3D Museum Kenangan, Monumen Laptop, & Dashboard
│   │   ├── MusicPlayer.tsx      # Audio player cerdas dengan auto-pause lifecycle tab
│   │   ├── Navbar.tsx           # Bar navigasi sticky dengan tautan eksternal
│   │   ├── StructureTimeline.tsx# Bagan struktur organisasi 8 pengurus kelas
│   │   └── TechStackMarquee.tsx # Running marquee logo 15 teknologi PPLG
│   └── data/
│       └── mockData.ts          # Sumber kebenaran data: 35 siswa, 57 foto, 8 pengurus
├── LICENSE                      # Dokumen lisensi hukum hak cipta kepemilikan kelas
├── package.json                 # Konfigurasi dependensi dan script Next.js
├── PRD.md                       # Product Requirement Document (Dokumen Ini)
└── README.md                    # Dokumentasi umum repositori GitHub
```

---

## 5. Rincian Spesifikasi Fitur (Functional Requirements)

### FR-1: Hero & First-Fold Experience (100dvh)
- **ID:** `FEAT-HERO-01`
- **Tampilan:** Mengisi tepat tinggi satu layar perangkat (`100dvh`) saat pertama kali diakses.
- **Komponen Visual:**
  - Bar Navigasi Neobrutalism kuning ber-border hitam tebal (4px).
  - Teks header utama masif *"XII PPLG 1 // SMKN 1 DEPOK"*.
  - Kotak dekoratif sudut responsif yang berputar (*rotating badges*).
  - Tautan langsung ke Instagram resmi kelas: `@12pplg1_`.

---

### FR-2: Ruang Kelas 3D Interaktif (`Classroom3D.tsx`)
- **ID:** `FEAT-CLASSROOM-02`
- **Deskripsi:** Representasi ruang laboratorium komputer SMKN 1 Depok dalam bentuk 3D WebGL.
- **Rincian Spesifikasi:**
  1. **35 Meja Komputer Siswa:**
     - 6 baris meja, terbagi atas Sayap Kiri dan Sayap Kanan.
     - Komposisi siswa: **22 Laki-laki (Cowo)** dan **13 Perempuan (Cewe)**.
     - Setiap meja memiliki PC Tower, Monitor LCD, Keyboard, Mouse, dan Kursi Ergonomis.
  2. **Meja Guru & Papan Tulis:**
     - Meja guru di bagian depan kanan panggung kelas (dipersembahkan untuk Wali Kelas: Bu Hilda Rahmawati, S.Kom).
     - Papan tulis putih (*whiteboard*) besar di dinding depan kelas.
  3. **Interaksi & Raycasting:**
     - *Hover*: Meja yang disentuh pointer/kursor menyala (*glow*) kuning Neobrutalism.
     - *Click*: Membuka modal profil popup yang berisi: Nama Siswa, Nomor Absen, Posisi Meja (Baris & Sayap), Peran Teknis (*Fullstack Developer*), dan Quote pribadi siswa.
  4. **Pencarian Siswa Instan (*Instant Live Search*):**
     - Pengguna dapat mengetikkan nama siswa pada kolom input. Kamera 3D akan meluncur halus (*lerp glide*) langsung berhadapan ke meja siswa yang dicari.
  5. **Preset Kamera:**
     - Mode 3D Bebas, Tampak Atas (2D Floorplan), Meja Guru, dan Sudut Belakang Kelas.

---

### FR-3: 🏛️ Museum Kenangan 3D Virtual Art (`MemoryMuseum3D.tsx`)
- **ID:** `FEAT-MUSEUM-03`
- **Deskripsi:** Galeri seni 3D imersif yang memajang seluruh arsip foto kenangan sekolah dalam nuansa museum kelas dunia.
- **Rincian Spesifikasi:**

#### A. Arsitektur Museum & Tata Letak Dinding
- **Dimensi Paviliun:** Lebar 28 meter, Kedalaman 28 meter, Tinggi dinding 8 meter.
- **Lantai:** Keramik slate gelap dengan grid tile Neobrutalist (`repeat 6x6`).
- **Plafon & Pencahayaan:** Chandelier pusat overhead hangat (PointLight), directional fill light, dan spotlight terarah pada tiap karya.
- **57 Bingkai Pigura Foto Autentik:**
  - *Sayap Kiri (Dinding Luar & Partisi Pameran):* 42 Foto Kenangan Kelas 10.
  - *Sayap Kanan (Dinding Luar):* 15 Foto Kenangan Kelas 11.
  - Tiap pigura memiliki frame hitam bevel tebal, trim aksen kuning emas, mat-board putih, dan pelat tembaga bertuliskan judul serta tanggal foto.

#### B. Centerpiece Monumen Laptop 3D
- Berdiri di atas pedestal tabung silinder marmer hitam di tengah aula (`x: 0, z: 0`).
- Model 3D laptop modern dengan chassis titanium abu-abu dan aksen trim kuning.
- Sudut bukaan layar ergonomis 112° (kemiringan natural 22° ke belakang).
- Logo jurusan PPLG bercahaya neon di bagian cover belakang laptop.
- Layar laptop menampilkan teks kode sumber website kelas yang aktif (`XII-PPLG-1.tsx`).
- Berputar 360° secara kontinu dan melayang lembut (*floating bobbing animation*).

#### C. Master Command Center & Layar Statistik Kelas
- Layar raksasa ultra-HD tunggal di dinding belakang sayap kanan (`x: 9.0, y: 2.4, z: -13.75`, lebar 5.3m, tinggi 2.7m).
- Terpisah aman tanpa bertabrakan dengan spanduk museum (*clear gap* > 1 meter).
- **Konten Layar Terpadu (Canvas 1536 × 768 px):**
  1. *Header Bar:* Logo status aktif *All Systems Nominal* dan identitas SMKN 1 Depok.
  2. *Hero Metrics:*
     - **35** Total Murid (22 Cowo • 13 Cewe)
     - **2024** Tahun Masuk SMKN 1 Depok
     - **2027** Tahun Target Kelulusan (Angkatan 2024–2027)
     - **57** Foto Memori (42 Kelas 10 • 15 Kelas 11)
  3. *15 Tech Stack Badges PPLG:* HTML5, CSS3, JavaScript, PHP, Laravel, MySQL, Java, Android, Unity, Blender, VS Code, Figma, GitHub, Laragon, phpMyAdmin.
  4. *Log Praktikum Kejuruan:* Rekap praktikum PBO & Logika, Web Dinamis, Backend Laravel, MySQL Server, serta Game Unity & Blender 3D.
  5. *Activity Commit Heatmap:* Grafik matriks commit hijau/emas ala GitHub yang mencerminkan intensitas koding kelas.
  6. *Roadmap Angkatan 3 Fase:* Fase 1 Kelas 10 (Fondasi), Fase 2 Kelas 11 (Eksplorasi), dan Fase 3 Kelas 12 (Kelulusan).

#### D. Engine Stabilitas Mobile & Anti-Crash
- **Masalah Sebelumnya:** 57 foto beresolusi mentah kamera (hingga 3456×3456 px) menghabiskan VRAM GPU sebesar 2,6 GB, menyebabkan Chrome di ponsel crash/reload.
- **Solusi Rekayasa:**
  1. **Auto-Downscaling Tekstur WebGL:** Fungsi `loadDownscaledTexture` otomatis mengecilkan foto secara proporsional ke dimensi maksimal **512px** menggunakan offscreen canvas dan `img.decoding = "async"`.
  2. **Pengurangan Memori VRAM:** Pemakaian VRAM turun dari **2.600 MB menjadi hanya ~45 MB** (penurunan beban > 98%). Ponsel RAM 2GB/3GB dapat membuka pameran tanpa kendala.
  3. **Shared Placeholder Texture:** 57 pigura menggunakan 1 tekstur placeholder terpadu saat inisialisasi, menghemat 56 alokasi elemen canvas di RAM.
  4. **Background Pre-Rendering:** Komponen 3D di-mount dan memproses antrean tekstur di latar belakang sejak pengguna berada di Mode 2D. Pergantian ke Mode 3D berlangsung **0 detik seketika**.
  5. **Throttled Inactive Loop:** Saat pengguna berada di Mode 2D, animasi loop 3D museum ditahan agar tidak membebani baterai dan suhu ponsel tetap dingin.

---

### FR-4: Running Logo Tech Stack Interaktif (`TechStackMarquee.tsx`)
- **ID:** `FEAT-STACK-04`
- **Deskripsi:** Running strip logo 15 teknologi dan perangkat lunak yang dipelajari di program kejuruan PPLG SMKN 1 Depok.
- **Daftar Aset:** `HTML5`, `CSS3`, `JavaScript`, `PHP`, `Laravel`, `MySQL`, `Java`, `Android`, `Unity`, `Blender`, `VS Code`, `Figma`, `GitHub`, `Laragon`, `phpMyAdmin`.
- **Perilaku:** Bergerak mulus (*seamless infinite loop*), berhenti sejenak saat kursor diarahkan (*pause on hover*).

---

### FR-5: Galeri Memori Dual-Mode (`Gallery.tsx`)
- **ID:** `FEAT-GALLERY-05`
- **Deskripsi:** Pengontrol pusat dokumentasi foto yang memungkinkan pengguna memilih antara pengalaman 3D Virtual Art atau Grid 2D Klasik.
- **Fitur Mode Grid 2D:**
  - Layout kartu Neobrutalism ber-aspect ratio asli (*anti-cropping*).
  - Filter kategori cepat: *All*, *Kelas 10*, *Kelas 11*.
  - Real-time search box (mencari berdasarkan judul, deskripsi, folder, atau tanggal).
  - Pagination bertahap (+6 item per muat) dan tombol *Tampilkan Semua Foto*.
  - Lightbox modal resolusi tinggi dengan navigasi keyboard (`Panah Kiri`, `Panah Kanan`, `Escape`).

---

### FR-6: Dual-Directional Running Marquee
- **ID:** `FEAT-MARQUEE-06`
- **Jalur 1 (Ke Kanan):** Menampilkan seluruh 35 nama siswa/i angkatan XII PPLG 1.
- **Jalur 2 (Ke Kiri):** Menampilkan slogan kebanggaan kelas: *"Logic, Code, and Creativity — Berjuang bersama, maju bersama."*

---

### FR-7: Struktur Organisasi Kelas (`StructureTimeline.tsx`)
- **ID:** `FEAT-STRUCT-07`
- **Deskripsi:** Bagan kepengurusan kelas resmi dengan kartu profil Neobrutalism.
- **Data Jabatan (8 Peran Inti):**
  1. Kepala Program Keahlian: Heri Sri Purnomo, S.Kom
  2. Wali Kelas: Hilda Rahmawati, S.Kom
  3. Ketua Kelas: Jonni
  4. Wakil Ketua Kelas: Jian
  5. Sekretaris 1: Marfa
  6. Sekretaris 2: Zilfa
  7. Bendahara 1: Jasmine
  8. Bendahara 2: Nakita

---

### FR-8: Smart Background Music Player (`MusicPlayer.tsx`)
- **ID:** `FEAT-AUDIO-08`
- **Audio Track:** Lagu legendaris *"Rumah Kita - God Bless"* (format MP3).
- **Fitur Cerdas:**
  - *Smooth Volume Fade-in:* Suara naik perlahan dari 0.0 ke 0.45 agar tidak mengejutkan pengunjung.
  - *Smart Tab Lifecycle Auto-Pause:* Otomatis mem-pause lagu seketika saat pengunjung meminimalisir browser, berpindah tab, atau kembali ke home HP, dan otomatis melanjutkan lagu saat tab aktif kembali.
  - Widget kontrol di pojok kiri bawah dengan indikator animasi equalizer audio Neobrutalism.

---

### FR-9: Komponen Pelengkap & Navigasi
- **ID:** `FEAT-NAV-09`
- **Floating Back-to-Top:** Tombol melayang di pojok kanan bawah yang muncul otomatis saat halaman di-scroll melewati 400px.
- **Responsive Navbar:** Menu sticky dengan tautan pintas ke section Ruang Kelas 3D, Struktur, Galeri, dan Instagram resmi.

---

## 6. Persyaratan Non-Fungsional (Non-Functional Requirements)

### 6.1 Performa & Alokasi Memori (Performance & Memory Budget)
| Parameter | Standar / Batas Maksimal | Realisasi Produk |
| :--- | :--- | :--- |
| **VRAM GPU per Tekstur** | < 2 MB | ~0.8 MB (Capped 512px) |
| **Total VRAM Museum 3D** | < 100 MB | ~45 MB (Bebas OOM di HP) |
| **Frame Rate (FPS)** | 60 FPS (Desktop), > 45 FPS (Mobile) | 60 FPS stabil |
| **Ukuran Bundle JS** | < 250 KB (First Load JS) | Memenuhi standar Next.js Turbopack |
| **Animasi Rendering saat Inaktif** | 0 FPS (Idle / Paused) | 1 frame/detik saat di background |

### 6.2 Kompatibilitas Perangkat & Browser (Cross-Platform Compatibility)
- **Desktop:** Google Chrome, Mozilla Firefox, Microsoft Edge, Apple Safari, Opera.
- **Mobile:** Chrome for Android, Safari iOS, Samsung Internet, Mi Browser.
- **Dukungan Sentuh (*Touch & Gestures*):** Mendukung gesture satu jari untuk rotasi orbit 3D dan sentuhan tap untuk memilih meja/pigura.

### 6.3 Aspek Hukum, Hak Cipta, & Privasi (Legal & Proprietary Compliance)
- **Perlindungan Hak Cipta:** Mematuhi **UU No. 28 Tahun 2014 tentang Hak Cipta** dan **UU ITE**.
- **Larangan Kloning (*No-Fork / No-Clone Policy*):** Melarang keras pihak ketiga, sekolah lain, atau individu menyalin kode, mengklaim desain, atau menggunakan foto murid tanpa izin tertulis dari angkatan XII PPLG 1 SMKN 1 Depok.
- **Proteksi Privasi Siswa:** Foto siswa di folder `public/Kelas 10` dan `Kelas 11` dilindungi secara hukum sebagai arsip autentik internal kelas.

---

## 7. Skema Data (Data Dictionary)

### 7.1 Interface `ClassroomStudent` (Data Denah Meja Kelas)
```typescript
export interface ClassroomStudent {
  absen: number;          // Nomor urut absen (1 - 35)
  name: string;           // Nama panggilan siswa
  gender: "cowo" | "cewe";// Jenis kelamin (22 cowo, 13 cewe)
  row: number;            // Baris posisi meja (1 - 6)
  col: number;            // Kolom posisi meja (1 - 6)
  wing: "Kiri" | "Kanan"; // Posisi sayap lab komputer
  role: string;           // Keahlian teknis (contoh: Fullstack Developer)
  quote: string;          // Kutipan personal siswa
}
```

### 7.2 Interface `MemoryItem` (Data Foto Galeri & Museum)
```typescript
export interface MemoryItem {
  id: string | number;    // ID unik karya foto
  title: string;          // Judul momen dokumentasi
  src: string;            // Lokasi path file foto (/Kelas 10/... atau /Kelas 11/...)
  category: string;       // Kategori ("Kelas 10" atau "Kelas 11")
  folder?: string;        // Nama sub-folder arsip
  date?: string;          // Tanggal pengambilan foto
  description?: string;   // Deskripsi cerita di balik foto
}
```

---

## 8. Panduan Rilis & Deployment (Release & CI/CD Pipeline)

1. **Local Development:**
   ```bash
   npm install
   npm run dev    # Menjalankan server lokal di http://localhost:3000
   ```
2. **Kompilasi Produksi (Production Build):**
   ```bash
   npm run build  # Memastikan zero typescript errors & prerendered static pages
   ```
3. **Deployment Otomatis:**
   - Terintegrasi dengan repositori GitHub: `https://github.com/zshnrdtya/website-kelas.git`.
   - Branch `main` terhubung otomatis ke platform hosting (seperti Vercel / Netlify) dengan pipeline CI/CD instan pada setiap `git push`.

---

## 9. Rencana Pengembangan Masa Depan (Future Roadmap)

| Fase | Fitur Rencana | Estimasi | Deskripsi Singkat |
| :--- | :--- | :--- | :--- |
| **Fase 1** | Retro Arcade Cabinet 3D | Q4 2026 | Menaruh mesin dingdong 3D di sudut museum yang bisa memainkan mini-game 8-bit buatan siswa PPLG. |
| **Fase 2** | Virtual Guestbook 3D | Q1 2027 | Fitur buku tamu interaktif bagi pengunjung untuk meninggalkan pesan bagi angkatan 2024–2027. |
| **Fase 3** | UKK Portfolio Showcase | Q2 2027 | Halaman khusus yang menyematkan tautan proyek Uji Kompetensi Keahlian (UKK) masing-masing siswa. |

---

<div align="center">
  <br />
  <strong>DOKUMEN SPESIFIKASI RESMI PRODUK (PRD)</strong><br />
  <strong>XII PPLG 1 — SMK NEGERI 1 DEPOK</strong><br />
  <i>Angkatan 2024 – 2027 • "Logic, Code, and Creativity"</i>
</div>
