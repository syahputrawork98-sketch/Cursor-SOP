# BK-01: Technique of Drafting — Seni Membuat Blueprint yang Tajam

## 🌟 Gampangnya...

**Blueprint** itu seperti gambar teknik sebelum membangun gedung. Kalau kamu langsung nyuruh AI koding fitur tanpa blueprint, rasanya seperti membangun rumah tanpa denah — hasilnya bisa miring atau roboh di tengah jalan. **Technique of Drafting** adalah cara membuat kerangka kerja tertulis yang menjelaskan *apa* yang akan diubah, *file* mana yang disentuh, dan *logika* apa yang dipakai.

---

## 📖 Konteks & Sejarah

Dalam kolaborasi Human-AI, blueprint adalah **Kontrak Kerja**. Banyak user mengeluh AI "ngaco" padahal masalahnya ada di instruksi yang tidak punya kerangka. Sejarah penggunaan AI membuktikan bahwa blueprint mengurangi bug hingga 60% karena kesalahan logika ditemukan *sebelum* satu baris kode pun ditulis.

---

## ⚙️ Cara Kerja

### Anatomi Blueprint yang Sempurna

Sebuah blueprint harus mengandung 3 elemen "S":
1. **Specific Files**: Daftar file `@` yang akan dimodifikasi.
2. **Step-by-Step Logic**: Alur data (Input → Proses → Output).
3. **Safety Check**: Apa yang tidak boleh diubah agar tidak merusak sistem lain.

---

## 🗺️ Kapan Mode Ini Relevan

| Mode | Kebutuhan Blueprint |
|---|---|
| 📐 **BLUEPRINT** | **Wajib** (Sesuai namanya). |
| ♻️ **REFACTOR** | **Sangat Tinggi** (Cek efek domino). |
| 🐛 **DEBUG** | **Tinggi** (Rangkuman temuan sebelum diperbaiki). |

---

## 🛠️ Cara Pakai

### Template: The "Drafting" Prompt

Ketik ini saat AI menawarkan bantuan untuk tugas besar:
```markdown
"Tahan! Buatkan Blueprint-nya dulu. 
 Gunakan format:
 1. File Utama (@): [List file]
 2. Logic Flow: [Penjelasan alur]
 3. Risks & Dependencies: [Hal yang perlu diperhatikan]
 Tunggu OK dari saya baru koding."
```

---

## 🧪 Lab Praktek

**Skenario: Membuat Fitur Sorting Data**

1. Minta AI membuat fitur sorting.
2. Saat AI memberikan blueprint, coba cari celahnya: *"Apa yang terjadi kalau datanya kosong? Apa blueprintmu sudah mencakup itu?"*
3. Lihatlah bagaimana AI mengupdate blueprint-nya. 
4. **Hasil**: Kamu menyelamatkan waktu 30 menit karena tidak perlu memperbaiki kode yang lupa menghandle data kosong.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Vague Blueprint** | Blueprint cuma bilang "Saya akan update kodenya" | **TOLAK.** Minta detail fungsi dan baris file yang spesifik. |
| **Logic Loop** | AI buat blueprint yang muter-muter | Gunakan teknik **CoT** (RAK-06) di dalam blueprint. |
| **Blueprint Fatigue** | Kamu lelah baca blueprint panjang | Suruh AI meringkas poin kuncinya di bagian atas (Summary). |

---

### 📖 Materi Selanjutnya
- [BK-02: Validation Protocols](./BK-02-Validation-Protocols.md)
