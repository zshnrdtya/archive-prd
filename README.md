# 📦 Archive Product Requirements Document (PRD)

Kumpulan dokumen spesifikasi kebutuhan produk (*Product Requirements Document* / PRD) untuk berbagai proyek perangkat lunak yang dirancang dan dikembangkan oleh **[Raditya Rai Zeeshan](https://radityarz.my.id)**.

---

## 🧭 Struktur Repositori & Navigasi Branch

Repositori ini menggunakan strategi **Multi-Branch Isolation**, di mana branch `main` berfungsi sebagai katalog utama dan indeks dokumentasi. Dokumen PRD lengkap untuk setiap proyek disimpan secara terpisah di **branch masing-masing**.

Untuk membaca PRD dari proyek yang diinginkan, silakan beralih (*switch*) ke branch yang bersangkutan melalui dropdown branch di GitHub atau menggunakan Git CLI:

```bash
# Beralih ke branch proyek tertentu
git checkout <nama-branch>

# Atau menggunakan git switch
git switch <nama-branch>
```

---

## 📑 Daftar Proyek & Branch

| No | Proyek | Branch | Deskripsi Singkat | Tech Stack Utama |
|---|---|---|---|---|
| 1 | **Zeera AI** | [`prd-ai-zeera`](https://github.com/zshnrdtya/archive-prd/tree/prd-ai-zeera) | Asisten virtual 3D anime web real-time berbasis avatar `.vrm`, WebGL, dan Google Gemini Multimodal. | Three.js, WebGL, Gemini AI, Web Audio API, Next.js |
| 2 | **Portfolio Website v2** | [`prd-portfolio-v2`](https://github.com/zshnrdtya/archive-prd/tree/prd-portfolio-v2) | Platform portofolio interaktif full-stack bergaya Neumorphism dengan integrasi AI, nametag lanyard 3D, dan guestbook dinamis. | Next.js 16, React 19, Tailwind CSS v4, Prisma v7, PostgreSQL |
| 3 | **BOA Futsal Arena** | [`prd-web-sport`](https://github.com/zshnrdtya/archive-prd/tree/prd-web-sport) | Platform digital booking arena futsal dan manajemen olahraga terintegrasi dengan WhatsApp Gateway & Sport Type Switcher. | Laravel 12, Blade, Tailwind CSS 3.x, Alpine.js, MySQL, Fonnte API |
| 4 | **FinanceTrack** | [`prd-website-finance-tracker`](https://github.com/zshnrdtya/archive-prd/tree/prd-website-finance-tracker) | Aplikasi pencatat dan pelacak arus kas keuangan pribadi & keluarga yang cepat, aman, dan visual. | Next.js 16, React 19, TypeScript, Tailwind CSS v4, Supabase |
| 5 | **XII PPLG 1 Class Website** | [`prd-website-kelas`](https://github.com/zshnrdtya/archive-prd/tree/prd-website-kelas) | Website resmi kelas & museum memori virtual 3D interaktif angkatan 2024–2027 dengan estetika Neobrutalism. | Next.js 16, React 19, Three.js WebGL, Tailwind CSS |

---

## 🚀 Cara Akses Dokumen PRD

### Melalui GitHub Web UI
1. Klik dropdown selector branch di bagian kiri atas (bertuliskan `main`).
2. Pilih branch proyek yang ingin dibaca (misalnya `prd-ai-zeera`).
3. File PRD terkait akan langsung terlihat dan dapat dibaca.

### Melalui Terminal / CLI
```bash
# Clone repositori
git clone https://github.com/zshnrdtya/archive-prd.git
cd archive-prd

# Melihat semua branch yang tersedia di remote
git branch -r

# Berpindah ke branch tertentu
git checkout prd-ai-zeera
```

---

## 👤 Pengembang & Hak Cipta

* **Author:** Raditya Rai Zeeshan (*Founder Z - Project* • SMKN 1 Depok)
* **Website / Portofolio:** [radityarz.my.id](https://radityarz.my.id)
* **GitHub:** [@zshnrdtya](https://github.com/zshnrdtya)
