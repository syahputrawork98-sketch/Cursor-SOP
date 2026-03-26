# BK-01: Centralized SOP Management — Satu Aturan untuk Semua

## 🌟 Gampangnya...

Saat kamu punya 20+ proyek (hub), mengupdate aturan di setiap proyek satu per satu adalah mimpi buruk. **Centralized SOP Management** adalah teknik di mana kamu menjadikan satu tempat (yakni repo **Cursor-SOP** ini) sebagai "Pusat Komando". Proyek-proyek lain hanya tinggal merujuk atau menyalin potongan kode dari sini. Dengan cara ini, jika kamu mengubah aturan koding, semua proyekmu bisa ikut terupdate dengan cepat.

---

## 📖 Konteks & Sejarah

Developer yang mengelola banyak repo sering mengalami **"Entropy"** — di mana satu repo punya aturan A, repo lain punya aturan B, dan akhirnya AI bingung saat pindah-pindah proyek. Memusatkan SOP (Standard Operating Procedure) adalah satu-satunya cara untuk menjaga kualitas output AI tetap tinggi di seluruh ekosistem kerjamu.

---

## ⚙️ Cara Kerja

### The "Hub-and-Spoke" Model

1. **The Hub (Source of Truth)**: Repo `Cursor-SOP` yang menampung semua template `.cursorrules` terbaru.
2. **The Spokes (Active Projects)**: Repo-repo kerjamu yang berisi `.cursorrules` hasil copy-paste dari Hub.
3. **The Audit**: Secara berkala, AI dicek apakah dia masih mengikuti SOP yang ada di Hub.

---

## 🗺️ Kapan Mode Ini Relevan

| Jumlah Proyek | Rekomendasi |
|---|---|
| 1 - 2 Proyek | Kelola manual masih oke. |
| 5 - 10 Proyek | Mulai gunakan template terpusat. |
| **> 10 Proyek** | **WAJIB** pakai Centralized SOP (RAK-08). |

---

## 🛠️ Cara Pakai

### Teknik: Versioned Snippets

Jangan copy-paste seluruh file. Simpan snippet logic di RAK-08 dan beri versi:
```markdown
# Snippet: Discuss-First-Policy v2.1
"JANGAN koding sebelum blueprint disetujui. Aturan ini berlaku untuk semua repo."
```

Setiap kali kamu mulai proyek baru, panggil AI:
```markdown
"Baca @Cursor-SOP/RAK-08. Ambil snippet standar .cursorrules terbaru dan pasang di proyek ini."
```

---

## 🧪 Lab Praktek

**Skenario: Update aturan di seluruh proyek**

1. Kamu mengubah standar penamaan folder di `Cursor-SOP`.
2. Buka proyek aktifmu yang lain.
3. Ketik: *"Audit .cursorrules saya dibandingkan dengan standar terbaru di @Cursor-SOP. Update bagian yang sudah out-of-date."*
4. **Hasil**: Proyekmu sinkron kembali dalam hitungan detik.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **SOP Bloat** | SOP terpusatmu jadi terlalu panjang sampai AI bingung | Pisahkan SOP menjadi beberapa modul kecil (RAK-01 s/d RAK-09). |
| **Stale Rules** | Kamu update Hub tapi lupa update Spokes | Gunakan ritual **"Monthly Matrix Sync"** (cek semua proyek sebulan sekali). |
| **Local Overrides** | Ada satu proyek yang butuh aturan khusus | Izinkan "Local Override" di bawah bagian `# LOCAL RULES` di `.cursorrules`. |

---

### 📖 Materi Selanjutnya
- [BK-02: Sync Protocols](./BK-02-Sync-Protocols.md)
