---
name: antigravity-anti-slop-ai
description: "Enforces human-crafted UI/UX design, clean code architecture, natural copywriting, and eliminates AI slop across frontend, backend, and documentation whenever the user asks for anti-slop or says 'Jangan AI Slop dong' or 'anti ai slop'."
author: "Asharuu"
version: 1.1.0
---

# Antigravity Anti-Slop AI

[Bahasa Indonesia](#bahasa-indonesia) | [English](#english)

---

<a name="bahasa-indonesia"></a>
## Bahasa Indonesia

Pedoman ketat untuk memastikan seluruh kode, antarmuka web, arsitektur, dan teks (*copywriting*) terasa **asli dirancang oleh manusia profesional (*human-crafted*)**, berjiwa fungsional, dan bebas dari kebiasaan buruk bawaan AI (*Anti-AI Slop*).

---

### 🏛️ 4 Pilar Anti-AI Slop

### 1. Desain UI/UX & Tata Letak (Visual & Layout)
* **Kesesuaian Karakter & Konteks**: Jangan memaksakan estetika neon cyberpunk/poster festival musik ke aplikasi kasir (POS), dashboard inventaris, atau sistem finansial. Rancang sesuai kebutuhan nyata pengguna.
* **Keseimbangan Grid & Ritme Tata Letak**: Hindari layout canggung dengan kartu atau tombol "kesepian" (misal: 4 kolom di atas, lalu 1 elemen terisolasi di bawah). Gunakan grid modular yang seimbang (misal: grid responsif 2-4 kolom atau 3-3).
* **Ruang Bernapas (White Space)**: Berikan *padding* dan *margin* yang lapang di setiap kartu dan kontainer. Desain yang terlalu padat membuat mata pengguna cepat lelah.
* **Typographic Restraint**: Dilarang membuat semua judul dan tombol menjadi **HURUF KAPITAL TEBAL (ALL-CAPS)**. Gunakan hierarki tipografi alami (*Title Case* untuk judul, *Sentence Case* untuk teks penjelas).

---

### 2. Teks & Antarmuka (Interface Copywriting)
* **Dilarang Membocorkan 'Plumbing' Teknis ke Pengguna Publik**:
  - ❌ *"PostgreSQL pool node-01 connected · JWT HS256 active · User table indexed"*
  - ❌ *"Executing query: SELECT * FROM items WHERE stock < 5"*
  - ❌ *"Demo accounts loaded from seeds/01_users.sql"*
  - ✅ *"Masuk ke Portal Manajemen Inventaris"*
  - ✅ *"5 barang hampir habis dan memerlukan pemesanan ulang."*
  - ✅ *"Pilih Profil Uji Coba"*
* **Singkirkan Gimmick & Basa-Basi AI**:
  - **Dilarang pasang running ticker / marquee** pada halaman yang memerlukan fokus pengguna (Login, Form Kasir, Checkout).
  - **Hentikan taburan emoji & simbol berlebihan**: Jangan menaruh `✱`, `❋`, `⚡`, `◆`, `🚀` di setiap judul dan tombol.
  - **Hindari kata-kata hampa makna**: Hapus jargon robotik seperti *"Leveraging seamless next-gen paradigms to empower workflow"*. Gunakan bahasa yang jelas dan to-the-point.

---

### 3. Arsitektur & Kualitas Kode (Code Quality)
* **Anti Over-Engineering**: Jangan membuat 5 layer abstraksi (*Factory, Repository, Adapter, Strategy*) untuk fungsi utilitas atau CRUD sederhana. Buatlah sesederhana mungkin (*KISS & YAGNI*).
* **Hapus Komentar Malas / Gema (Echo Comments)**:
  - ❌ `// Function to calculate total` di atas `function calculateTotal()`
  - ❌ `// Return result` di atas `return result;`
  - ✅ Tulis komentar hanya jika menjelaskan alasan/konteks bisnis (*why*), bukan mengulang baris kode (*what*).
* **Dependensi Ramping (Lean Dependencies)**: Utamakan fitur bawaan bahasa/framework (native Web API, native Array methods) daripada menginstal package raksasa hanya untuk fungsi 1 baris.

---

### 4. Komunikasi & Dokumentasi (Git & Docs)
* **Pesan Commit yang Ringkas & Jelas**: Tulis commit format conventional (`feat: ...`, `fix: ...`) yang padat tanpa basa-basi robotik.
* **Dokumentasi yang Berbobot**: Dokumentasikan cara menjalankan, konfigurasi environment, dan arsitektur tanpa kata pengantar AI bertele-tele.

---

### ⚡ Kondisi Pemicu (Trigger Conditions)

Aktifkan pedoman ini secara otomatis ketika:
1. Pengguna berkata: *"Jangan AI Slop dong"*, *"anti ai slop"*, *"jangan kayak AI"*, *"bikin lebih manusiawi"*, *"bikin yang profesional"*.
2. Membangun, mengaudit, atau merombak antarmuka frontend, arsitektur backend, dan copywriting proyek.

---

<a name="english"></a>
## English

Strict guidelines to ensure all generated code, user interfaces, architecture, and copy feel **authentically human-crafted**, functionally grounded, and free from standard AI generation vices (*Anti-AI Slop*).

---

### 🏛️ The 4 Pillars of Anti-AI Slop

### 1. UI/UX & Layout Discipline
* **Contextual Appropriateness**: Do not apply cyberpunk neon aesthetics to an inventory dashboard, hospital portal, or ERP system. Match the domain and real user workflows.
* **Balanced Human Layout**: Avoid awkward layout orphans (e.g. 4 cards on row one, 1 isolated card on row two). Design balanced responsive grids.
* **Generous White Space**: Provide clear margins and padding. Dense, cramped interfaces cause cognitive fatigue.
* **Typographic Restraint**: Never format every title and label in **BOLD ALL-CAPS**. Maintain clear typographic scales.

---

### 2. Interface Copywriting Discipline
* **Never Leak Technical Plumbing into User Copy**:
  - ❌ *"PostgreSQL pool node-01 connected · JWT HS256 active · User table indexed"*
  - ❌ *"Executing query: SELECT * FROM items WHERE stock < 5"*
  - ❌ *"Demo accounts loaded from seeds/01_users.sql"*
  - ✅ *"Sign in to Inventory Portal"*
  - ✅ *"5 items are running low on stock."*
  - ✅ *"Select Demo Profile"*
* **Zero Gimmicks & Filler**:
  - **No marquee tickers** on high-focus screens (Login, Checkout, Forms).
  - **Stop emoji spam**: Eliminate excessive `✱`, `❋`, `⚡`, `◆`, `🚀` on every button.
  - **Cut corporate buzzword soup**: Replace *"Leveraging next-gen paradigms to empower productivity"* with crisp, direct instructions.

---

### 3. Code Quality & Architecture Discipline
* **Zero Over-Engineering**: Do not build 5 abstract layers (*Factory, Facade, Repository, Adapter*) for a simple utility function or basic CRUD endpoint. Follow KISS and YAGNI.
* **No Echo Comments**:
  - ❌ `// Function to calculate total` above `function calculateTotal()`
  - ❌ `// Return result` above `return result;`
  - ✅ Document the *why* (business constraints, edge cases), not the obvious *what*.
* **Lean Dependencies**: Rely on native platform APIs instead of installing heavy external packages for trivial tasks.

---

### 4. Git Commits & Documentation Discipline
* **Concise Conventional Commits**: Write crisp, meaningful commit messages (`feat: ...`, `fix: ...`) without robotic preamble.
* **Pragmatic Documentation**: Focus on setup steps, environment flags, and architectural decisions without generic LLM introductory fluff.

---

### ⚡ Trigger Conditions

Automatically activate this skill when:
1. The user explicitly requests: *"Jangan AI Slop dong"*, *"anti ai slop"*, *"don't make it look like AI"*, *"make it human-crafted"*, *"clean professional UI"*.
2. Generating, auditing, or refactoring frontend UIs, backend services, or project documentation.
