# BK-01: Token Physics — Cara AI Membaca dan Mengingat

## 🌟 Gampangnya...

AI tidak membaca kata demi kata seperti manusia. Dia membaca dalam unit yang disebut **Token**. Satu token biasanya setara dengan 3-4 karakter (sekitar 3/4 kata). Bayangkan AI punya "ember ingatan" (Context Window). Setiap kali kamu bertanya atau AI menjawab, ember itu terisi token. Jika embernya penuh, AI akan mulai membuang token paling lama agar ada ruang untuk token baru. Inilah sebabnya AI bisa "lupa" instruksi di awal chat.

---

## 📖 Konteks & Sejarah

Dulu, ember ingatan AI sangat kecil (hanya 4,000 token). Sekarang, model seperti Gemini bisa menampung hingga 2,000,000 token — sebesar 10-20 novel tebal! Namun, semakin penuh embernya, semakin lambat AI berpikir dan semakin besar risiko AI menjadi "bingung" karena terlalu banyak informasi yang saling bertubrukan (*Context Poisoning*).

---

## ⚙️ Cara Kerja

### Anatomi Token

- Kata pendek (misal: "He") = 1 Token.
- Kata panjang (misal: "Antigravity") = Mungkin 2-3 Token.
- Spasi dan Tab juga dihitung sebagai Token.

**Prinsip 80/20**: Jangan berikan 100% file proyekmu jika kamu hanya sedang mengerjakan 20% kodingan. Semakin sedikit token yang tidak perlu, semakin tajam logika AI.

---

## 🗺️ Kapan Mode Ini Relevan

| Ukuran Konteks | Dampak | Tindakan |
|---|---|---|
| **Low** (< 10k token) | Sangat Cepat & Akurat. | Ideal untuk pengerjaan fitur tunggal. |
| **Medium** (10k - 50k) | Masih akurat tapi mulai lambat. | Mulai gunakan **Selective Mentions**. |
| **High** (> 100k) | Risiko "Halusinasi" meningkat. | Gunakan **Session Refresh Protocol** (RAK-06). |

---

## 🛠️ Cara Pakai

### Teknik "Economy of Tokens"

Jangan memboroskan token dengan instruksi yang berulang-ulang.
1. Cukup kirim file yang **berhubungan langsung** dengan task.
2. Gunakan ringkasan (*summary*) daripada menyalin seluruh log error yang panjangnya ribuan baris.

```markdown
# TIPS HEMAT TOKEN:
Daripada @mention seluruh folder /src, 
lebih baik @mention 2 file yang sedang kamu edit.
```

---

## 🧪 Lab Praktek

**Skenario: Melihat Dampak Context Window**

1. Buka sesi chat baru yang panjangnya sudah 50+ turn.
2. Tanya AI tentang instruksi yang kamu berikan di Turn 1.
3. Jika AI mulai ragu atau salah jawab, cek sisa token/kapasitas window (di Cursor biasanya ada indikator jika sudah mendekati limit).
4. Solusi: Gunakan **Handover** ke sesi baru untuk mengosongkan ember token.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Context Overload** | AI memberikan jawaban yang tercampur antara kode lama & baru | Lakukan **Session Refresh**. Bersihkan ember tokenmu. |
| **Missing Links** | AI tidak "melihat" hubungan antar file | Pastikan file-file "jembatan" (misal: interface/config) ikut di-@mention. |
| **Token Bloat** | Kamu mempaste file CSV besar ke chat | Simpan data besar di file fisik, lalu suruh AI membaca bagian spesifik saja. |

---

### 📖 Materi Selanjutnya
- [BK-02: Context Management Strategy](./BK-02-Context-Management.md)
