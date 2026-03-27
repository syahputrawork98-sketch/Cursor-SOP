# BK-01: Indexing Optimization â€” Membuat AI "Melek" Struktur Proyek Kamu

## ðŸŒŸ Gampangnya...

Kenapa AI terkadang tidak "melihat" file yang baru saja kamu tambahkan, atau tidak paham hubungan antar file-mu? Itu karena **Indexing** belum beres. Indexing adalah cara AI membaca semua file-mu dan menjadikannya database internal. Buku ini mengajarkan cara merapikan proyek agar sistem RAG (sistem pencarian AI) bisa bekerja 100% akurat dan tidak pernah salah ambil referensi.

---

## ðŸ“– Konteks & Sejarah

AI tidak membaca seluruh disk komputermu setiap kali kamu bertanya. Dia membaca **Vector Database** (index) yang dibuatnya saat pertama kali kamu membuka folder. Jika struktur foldermu berantakan atau terlalu banyak file sampah (seperti `node_modules` atau file log besar), index AI akan "kotor" dan jawaban AI pun jadi tidak akurat.

---

## âš™ï¸ Cara Kerja

### Cara Kerja Semantic Indexing

1. **Scanning**: AI memindai semua file teks.
2. **Chunking**: File besar dipecah menjadi bagian-bagian kecil (chunks).
3. **Embedding**: Chunks diubah menjadi angka koordinat (vektor) agar AI tahu file A mirip dengan file B.
4. **Retrieval**: Saat kamu bertanya, AI mengambil chunks dengan koordinat terdekat.

---

## ðŸ—ºï¸ Kapan Mode Ini Relevan

| Mode | Pengaruh Indexing |
|---|---|
| ðŸ”¬ **ANALYZE** | Sangat butuh index akurat untuk mengaudit codebase. |
| âš¡ **EXECUTE** | Memastikan AI tidak membuat file duplikat karena tidak "melihat" file asli. |
| ðŸ› **DEBUG** | Membantu AI menemukan hubungan antar file yang jauh. |

---

## ðŸ› ï¸ Cara Pakai

### Teknik 1: .cursorignore (Saringan "Sampah")

Buat file `.cursorignore` di root proyekmu untuk membuang file yang tidak berguna bagi AI:
```markdown
# Abaikan folder dependency
node_modules/
venv/
.next/
dist/

# Abaikan build logs & temp
*.log
tmp/
.temp/

# Abaikan media besar (AI gak bisa baca binary)
*.jpg
*.png
*.mp4
```

### Teknik 2: Semantic Folder Naming

Gunakan nama folder yang menjelaskan isinya secara fungsional:
```markdown
# JELEK (AI bingung)
/f1
/f2
/stuff

# BAGUS (AI paham)
/services/auth
/components/ui/buttons
/utils/validation
```

### Teknik 3: Re-indexing Manual

Jika kamu merasa AI mulai "bodoh" padahal sudah ada rules:
1. Klik Ikon Gear di Cursor (Settings).
2. Pergi ke **Features** -> **Codebase Indexing**.
3. Klik **Rescan Codebase**.

---

## ðŸ§ª Lab Praktek

**Skenario: AI Tidak Melihat File Baru**

1. Kamu baru copy file besar dari internet ke folder baru.
2. AI bilang "Saya tidak menemukan file tersebut."
3. **Langkah Perbaikan**: 
   - Cek apakah extension filenya terdaftar di `.cursorignore`.
   - Cek status indexing di pojok kanan bawah Cursor. 
   - Klik **Compute Index** atau seret file tersebut langsung ke chat dengan `@mention`.

---

## âš ï¸ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Index Bloat** | AI lama sekali merespons karena "membaca" ribuan file sampah | Bersihkan `.cursorignore` sekarang juga. |
| **File Terlalu Besar** | Satu file isinya 10,000 baris kode | Pecah file tersebut agar sistem *Chunking* bisa bekerja lebih akurat. |
| **Binary Files** | Kamu memaksa AI membaca PDF/Image besar | Deskripsikan isi file tersebut di dalam `.md` terpisah dan `@mention` file `.md`-nya. |

---

### ðŸ“– Materi Selanjutnya
- [RAK-06: The Underworld (Context & Prompting)](../../../RAK-06-The-Underworld/README.md)

