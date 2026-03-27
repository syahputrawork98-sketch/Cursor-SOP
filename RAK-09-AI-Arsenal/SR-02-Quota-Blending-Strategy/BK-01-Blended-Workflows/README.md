# BK-01: Blended Workflows — Strategi "Tipping Point"

## 🌟 Gampangnya...

Apa yang kamu lakukan saat kuota Gemini Pro kamu habis di tengah deadline yang mepet? Jangan panik! **Blended Workflows** adalah teknik "mencampur" kekuatan model AI agar kamu tetap bisa bekerja dengan kualitas Pro meskipun hanya menggunakan model Flash. Rahasianya bukan di AI-nya, tapi di **cara kamu memberikan instruksi** yang jauh lebih ketat (High-Rigor) saat menggunakan model yang lebih lemah.

---

## 📖 Konteks & Sejarah

Teknik ini lahir dari kebutuhan user (seperti kamu) yang butuh performa tinggi 24/7 tapi terbentur batasan kuota. "Tipping Point" adalah titik di mana kamu secara sadar mengubah gaya komunikasimu dari "Sanitasi" (santai) ke "Militer" (kaku & detail) agar model Flash tidak berani "offside".

---

## ⚙️ Cara Kerja

### The "High-Rigor" Boost for Flash

Saat menggunakan model Low-tier (Flash), kamu harus memberikan "Kruk" (alat bantu) tambahan:
1. **Chain-of-Thought (CoT)**: Paksa AI menulis langkahnya satu per satu.
2. **Constraint-Based**: Berikan daftar "DILARANG" yang sangat spesifik.
3. **Double Verification**: Suruh AI mengecek ulang pekerjaannya sebelum submit.

---

## 🗺️ Kapan Mode Ini Relevan

| Kondisi Kuota | Gaya Komunikasi |
|---|---|
| **Pro > 50%** | Diskusi santai, AI yang banyak mikir. |
| **Pro < 10%** | **Blended Workflow Starts.** Kamu yang banyak mikir & mendikte. |
| **Pro = 0 (Flash Only)** | **Full High-Rigor.** Gunakan CAPSLOCK dan aturan ketat. |

---

## 🛠️ Cara Pakai

### Teknik "The Tipping Point" Prompting

Jika terpaksa pakai Flash untuk tugas sulit, gunakan awalan ini:
```markdown
"DIKARENAKAN SAYA MENGGUNAKAN MODEL FLASH:
 1. BACALAH SELURUH KONTEKS @file SECARA PERLAHAN.
 2. GUNAKAN CHAIN-OF-THOUGHT. TULIS LOGIKA SEBELUM KODING.
 3. JANGAN MENGHAPUS KODE YANG SUDAH ADA.
 4. KERJAKAN PER 5 BARIS DAN LAPOR."
```

---

## 🧪 Lab Praktek

**Skenario: Memperbaiki Logic dengan Flash**

1. Pilih fitur yang gagal diperbaiki Flash sebelumnya.
2. Berikan instruksi dengan teknik "High-Rigor" di atas.
3. Perhatikan: Flash tidak akan lagi menghapus kode sembarangan karena dia "diikat" oleh aturanmu.
4. **Insight**: Flash jadi pintar bukan karena updatenya, tapi karena instruksimu yang "Galak".

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Instruction Fatigue** | Kamu malas ngetik instruksi panjang saat pakai Flash | Simpan instruksi "High-Rigor" tadi sebagai **Cursor Snippet** agar tinggal panggil. |
| **False Confidence** | Kamu pikir Flash sudah pintar sendiri tanpa instruksi ketat | Selalu asumsikan Flash akan blunder. Jangan lepaskan kontrol. |
| **Context Poisoning in Flash** | Flash makin ngaco saat chat makin panjang | Gunakan **Session Refresh Protocol** (RAK-06) lebih sering (tiap 5-8 turn). |

---

### 📖 Materi Selanjutnya
- [BK-02: Fallback Protocols](../BK-02-Fallback-Protocols/README.md)
