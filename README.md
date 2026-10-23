# Pre-Reading & Persiapan Sesi: Fundamental Hermes Agent (1-on-1)

![hermes-agent-1on1-fundamental](https://andri.vip/api/covers/belajar-hermes-agent-fundamental-1on1?v=covers%2Fbelajar-hermes-agent-fundamental-1on1%2Fcover-1792593169808.webp)

Selamat datang di sesi 1-on-1 pengenalan Hermes Agent! Waktu 60 menit kita akan difokuskan pada live demo, bedah arsitektur, dan diskusi penerapan use-case pribadi Anda.

Agar kita tidak membuang waktu untuk troubleshooting teknis di hari H, mohon luangkan waktu 10-15 menit untuk membaca dan menyiapkan hal-hal di bawah ini sebelum sesi dimulai.

## 1. Spesifikasi Minimum Sistem

Agen yang akan kita bangun pada dasarnya adalah script yang berkomunikasi dengan API AI, sehingga tidak membutuhkan superkomputer kecuali Anda berniat menjalankan AI secara lokal.

**Untuk PC/Laptop (Proses Development):**

- OS: Windows 10/11 (Sangat disarankan menggunakan WSL2), macOS, atau Linux.
- Prosesor: Intel Core i3 / AMD Ryzen 3 / Apple Silicon (M1/M2/M3) atau setara.
- RAM: Minimal 8 GB (16 GB sangat direkomendasikan agar lancar membuka code editor, terminal, dan Docker secara bersamaan).

**Untuk Server / VPS (Jika ingin Self-Host 24/7 nantinya):**

- CPU: 1 - 2 vCPU.
- _Catatan Penting_: Spesifikasi ringan di atas berlaku jika agen menggunakan provider LLM eksternal (OpenAI/Anthropic via API Keys). Namun, jika Anda berencana menjalankan LLM secara lokal (misalnya menggunakan Ollama di dalam server/PC Anda sendiri), Anda akan membutuhkan RAM minimal 16 GB - 32 GB dan GPU khusus (VRAM 8GB+).

## 2. Persiapan Teknis (Wajib)

Pastikan sistem Anda sudah siap untuk menjalankan live code. Silakan siapkan:

- Code Editor: Instal [VS Code](https://code.visualstudio.com/) atau [Cursor](https://cursor.sh/).
- Environment: Pastikan [Node.js](https://nodejs.org/) (versi 20+) atau [Python](https://www.python.org/) (tergantung stack yang akan kita pakai) sudah terinstal.
- Nous Account: Buat akun [Nous Account](https://portal.nousresearch.com) dari creator Hermes Agent buat dapetin aksess free model.
- API Keys _(optional)_: Buat akun dan siapkan API Key dari provider LLM pilihan Anda (contoh: [DeepSeek Platform](https://platform.deepseek.com), [OpenAI Platform](https://platform.openai.com) atau [Anthropic Console](https://platform.claude.com/)). Simpan key ini di tempat yang mudah diakses saat sesi.

## 3. Konsep Dasar & Glosarium

Kita akan langsung terjun ke aspek teknis. Berikut adalah istilah yang akan sering muncul selama live demo:

- **Autonomous Agent vs ChatGPT Biasa**: ChatGPT pasif menunggu prompt Anda. Agent bersifat otonom; setelah diberi tujuan awal (misal: "Riset 5 kompetitor"), ia bisa merencanakan langkah, mencari di internet, menyaring data, dan menulis laporan tanpa perlu diinstruksikan setiap langkahnya.
- **SOUL / Persona**: File konfigurasi utama yang berisi system prompt untuk mengatur karakter, batas wewenang, dan gaya bahasa agen.
- **Orchestrator & Worker**: Dalam sistem multi-agent, Orchestrator bertindak sebagai manajer proyek yang memecah tugas besar, lalu membagikannya ke Worker (agen spesialis, seperti agen pencari web atau agen penulis kode).
- **Tool Calling**: Kemampuan agen untuk memicu script eksternal secara otomatis (misalnya: membaca file PDF, mengakses database, atau mengirim email) berdasarkan keputusan yang ia buat sendiri.

## 4. Agenda Sesi (60 Menit)

Kita akan berjalan dengan struktur berikut agar sesi padat dan interaktif:

- 00-05: Setup, Intro dan penyamaan baseline teknis.
- 05-15: Konsep mental model & arsitektur Hermes Agent.
- 15-35: _Live Demo!_ Bedah kode, konfigurasi, dan eksekusi agen di terminal.
- 35-55: _Deep Dive & Use-Case_. Waktu khusus untuk Anda bertanya dan membedah skenario pribadi.
- 55-60: Kesimpulan & referensi materi lanjutan.

## 5. Persiapan Use-Case (Tugas Singkat)

Bagian terbaik dari sesi 1-on-1 adalah kita bisa membedah masalah nyata Anda.

Sebelum sesi dimulai, p**ikirkan 1 proses atau rutinitas pekerjaan Anda saat ini yang manual, berulang, dan menyita waktu**.
Bawa contoh kasus tersebut besok, dan kita akan merancang blueprint bagaimana Hermes Agent bisa mengotomatisasi alur kerja tersebut.
