# BK-02: Context Management — Teknik "Selective Mentions"

## 🌟 Gampangnya...

Jangan berikan AI seluruh perpustakaan kalau kamu cuma mau dia memperbaiki satu halaman buku. **Context Management** adalah seni memilih file, folder, dan informasi mana yang benar-benar dibutuhkan AI untuk menyelesaikan tugas saat ini. Menggunakan `@mention` yang terlalu banyak justru akan membuat AI "pusing" dan melakukan kesalahan (*Context Poisoning*).

---

## 📖 Konteks & Sejarah

Model LLM modern memiliki fitur "Long Context", tapi riset menunjukkan adanya fenomena **"Lost in the Middle"** — AI sangat ingat bagian depan dan belakang chat, tapi sering lupa detail di bagian tengah. Dengan manajemen konteks yang ketat, kita memastikan informasi terpenting selalu berada di posisi yang "terlihat" jelas oleh AI.

---

## ⚙️ Cara Kerja

### Teknik "Selective Context"

Hanya panggil file yang masuk dalam 3 kategori ini:
1. **Target File**: File yang akan diubah.
2. **Dependency File**: File yang dipanggil oleh Target (Imports).
3. **Template/Example File**: File yang dijadikan standar gaya koding.

---

## 🗺️ Kapan Mode Ini Relevan

| Task | Apa yang Harus di-@mention? |
|---|---|
| **UI Styling** | `Target.tsx`, `index.css`, `design-tokens.json` |
| **API Fix** | `Controller.ts`, `Service.ts`, `Model.ts` |
| **Bug Hunting** | `ErrorLine.ts`, `LastWorkingVersion.ts` |

---

## 🛠️ Cara Pakai

### "The 3-File Rule"

Biasakan hanya me-mention maksimal 3 file utama per instruksi. Jika butuh lebih, tanyakan dulu pada dirimu: *"Apakah file ke-4 ini benar-benar kritis untuk logika saat ini?"*

### Protokol "Context Poisoning" Prevention

Jika chat terasa sudah berat dan AI mulai melantur:
1. Ketik: `"Analisis konteks saat ini. Sebutkan file mana yang menurutmu sudah tidak relevan lagi untuk diskusi kita."`
2. Suruh AI untuk mengabaikan file-file tersebut atau buka sesi baru.

---

## 🧪 Lab Praktek

**Skenario: Refactor yang Bersih**

1. Kamu mau refactor fungsi di `A.ts`.
2. Jangan @mention seluruh folder `src/`.
3. Gunakan: `@A.ts @A.test.ts @Interface-A.ts`.
4. Perhatikan betapa cepat dan presisinya jawaban AI dibandingkan saat dia harus "membaca" ribuan file lain yang tidak relevan.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Folder Mentions** | Mencoba `@src` atau `@root` sekaligus | **SANGAT TIDAK DISARANKAN.** Gunakan hanya untuk mode **ANALYZE** awal. |
| **Blind Spot** | AI tidak tahu kalau file B terpengaruh oleh file A | Gunakan `Codebase Indexing` atau mention file B secara manual. |
| **Stale Context** | Kamu sudah ganti tugas tapi file dari tugas lama masih "nempel" di memori AI | Tutup chat lama, buka chat baru (**Session Refresh**). |

---

### 📖 Materi Selanjutnya
- [RAK-04/SR-02: The Archives (RAG)](../SR-02-The-Archives/README.md)
