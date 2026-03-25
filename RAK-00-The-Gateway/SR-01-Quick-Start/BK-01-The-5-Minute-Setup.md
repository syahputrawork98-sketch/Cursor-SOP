# BK-01: The 5-Minute Setup

## 📖 1. Menghubungkan SOP ke Cursor
Agar Cursor tahu bahwa Anda punya "Gudang SOP" (8-Rak ini), Anda harus "mengenalkannya".

### Langkah-langkah:
1.  Buka File `.cursorrules` di root proyek koding Anda.
2.  Tambahkan baris berikut di paling atas:
    ```markdown
    ALWAYS read the SOPs in `i:\Workspace\Workspace-Syahputrawork\08-AI-Orchestration-Hubs\Cursor-SOP\` BEFORE executing any multi-file code changes.
    Follow the DISCUSS vs EXECUTE protocol strictly.
    ```
3.  Simpan file tersebut. Selesai! Sekarang Cursor Anda sudah punya "Otak" tambahan.

## ⚙️ 2. Cara Memanggil Rak Saat Chat
Saat Anda sedang koding dan ingin AI mengikuti aturan tertentu, cukup gunakan simbol `@`:
- Ketik: `"Tolong audit kode ini sesuai @RAK-02"`
- Cursor akan membaca folder RAK-02 secara otomatis dan menyesuaikan jawabannya.

## 📊 3. Sinyal Komando (The Triggers)
Jangan bicara bertele-tele. Gunakan kata kunci ini:
- **"DISKUSI"**: Mulai merancang rencana.
- **"LAKUKAN"**: Izin resmi bagi AI untuk mulai ngetik kode.

---

### 🧪 Lab Kecil:
Coba ketik di chat Cursor Anda sekarang: 
*"Cursor, apakah kamu sudah membaca RAK-00 saya? Jelaskan singkat apa tugasmu sebagai AI di sini."*
Jika ia bisa menjawab sesuai filosofi "Mandor vs Tukang", berarti setup Anda **Berhasil!**
