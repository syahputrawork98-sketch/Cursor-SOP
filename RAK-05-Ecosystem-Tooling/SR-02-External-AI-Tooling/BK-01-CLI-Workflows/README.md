# BK-01: CLI for Agentic Workflows — Menjalankan AI dari Terminal

## 🌟 Gampangnya...

Kenapa harus bolak-balik buka aplikasi Cursor kalau kamu bisa menyuruh AI bekerja langsung dari terminal (Command Prompt/PowerShell)? **CLI for Agentic Workflows** adalah cara menggunakan perintah teks untuk memicu aksi AI yang otomatis, seperti melakukan git commit, melakukan audit kode, atau bahkan membuat draft PR (Pull Request) tanpa kamu harus ngetik satu-satu.

---

## 📖 Konteks & Sejarah

Era koding modern bergeser dari "Chat-based" ke "Terminal-based". Với adanya CLI (Command Line Interface) seperti `cursor` atau integrasi agent di terminal, kamu bisa menggabungkan kekuatan AI dengan skrip otomasi. Ini adalah dasar dari workflow "Senior Engineer" yang efisien: biarkan skrip yang memanggil AI untuk pekerjaan rutin.

---

## ⚙️ Cara Kerja

### AI-Terminal Synergy

1. **Trigger**: Kamu mengetik perintah di terminal (misal: `npm run audit-ai`).
2. **Context Passing**: Skrip terminal mengambil file yang relevan dan mengirimkannya ke AI.
3. **Action**: AI melakukan tugasnya (analisis/edit) dan mengembalikan hasilnya ke terminal atau langsung ke file.

---

## 🗺️ Kapan Mode Ini Relevan

| Task | Alat / Command | Keuntungan |
|---|---|---|
| **Bulk Refactor** | Shell Script + Cursor CLI | Ubah 50 file sekaligus dengan pola yang sama. |
| **Auto-Commit** | AI-Git Scrip | Membuat pesan commit yang deskriptif secara otomatis. |
| **Env Setup** | CLI Wizard | Setup lingkungan proyek baru hanya dengan satu perintah. |

---

## 🛠️ Cara Pakai

### Teknik 1: Shortcut Cursor CLI

Gunakan terminal untuk membuka file atau folder langsung di Cursor:
```bash
# Buka folder saat ini di Cursor
cursor .

# Buka file spesifik
cursor src/main.ts
```

### Teknik 2: Menciptakan "Agentic Aliases"

Tambahkan ini ke profil terminalmu (misal: `.zshrc` atau PowerShell Profile) untuk memicu AI dengan cepat:

```powershell
# Contoh Alias untuk Audit Kode (Logic-only)
function audit-ai {
    cursor --command "ANALYZE this file for security vulnerabilities and logic flaws" $args[0]
}
```

---

## 🧪 Lab Praktek

**Skenario: Membuat Pesan Commit AI**

Daripada ngetik `git commit -m "fix"`, gunakan workflow ini:
1. Ketik: `git diff > diff.txt`
2. Buka `diff.txt` di Cursor.
3. Gunakan prompt: *"Berdasar @diff.txt, buatkan pesan commit yang rapi sesuai standar Conventional Commits."*
4. Copy hasilnya ke terminal. (Atau gunakan plugin AI-Git jika sudah terpasang).

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Terminal Overhead** | Terlalu banyak alias malah bikin bingung | Hanya buat alias untuk task yang kamu lakukan > 10x sehari. |
| **Lost Context** | CLI tidak membawa konteks chat sebelumnya | Selalu sertakan file referensi (`@file`) saat memanggil command CLI. |
| **Command Injection** | Menjalankan script AI yang tidak kamu mengerti | **SELALU** review command yang dihasilkan AI sebelum menekan Enter di terminal. |

---

### 📖 Materi Selanjutnya
- [BK-02: Automated Testing Integrations](./BK-02-Automated-Testing.md)
