# BK-02: Constraint-Based Prompting — Memasang "Pagar Betis" Instruksi

## 🌟 Gampangnya...

Pernahkah kamu minta AI buat koding tapi bilang *"Jangan pakai library X"* tapi dia malah tetap pakai? Itu karena instruksi laranganmu (constraints) kurang kuat. **Constraint-Based Prompting** adalah teknik untuk memasang "pagar betis" yang kokoh agar AI tidak bisa keluar jalur. Kuncinya bukan cuma bilang "jangan", tapi memberikan **batasan yang sangat spesifik** dan **konsekuensi logis**.

---

## 📖 Konteks & Sejarah

Dalam *Prompt Engineering*, ditemukan bahwa AI lebih merespon pada instruksi positif ("lakukan X") daripada instruksi negatif ("jangan lakukan Y"). Namun, dalam koding, kita sering butuh batasan keras (misal: "jangan ganti variable Z"). Teknik Constraint-Based dikembangkan untuk memperkuat instruksi negatif ini agar tidak kalah kuat dari instruksi positifnya.

---

## ⚙️ Cara Kerja

### Struktur Constraint yang Kuat

Sebuah batasan yang baik terdiri dari 3 elemen:
1. **Forbidden Action**: Apa yang dilarang.
2. **Acceptable Alternative**: Apa yang boleh dilakukan sebagai ganti.
3. **Validation Rule**: Bagaimana AI harus mengecek dirinya sendiri sebelum menjawab.

---

## 🗺️ Kapan Mode Ini Relevan

| Task | Jenis Constraint | Urgensi |
|---|---|---|
| **Legacy Code** | "DILARANG gunakan syntax ES6" | **VVIP** (Kode lama harus tetap jalan). |
| **Security** | "DILARANG simpan password di log" | **Tinggi** (Kepatuhan keamanan). |
| **Naming** | "DILARANG gunakan inisial 1 huruf" | **Medium** (Gaya koding). |

---

## 🛠️ Cara Pakai

### Teknik 1: The "NOT" Hammering

Gunakan kata-kata penegas yang sangat keras:
```markdown
"Task: Buat fungsi fetch.
 CONSTRAINT:
 - DILARANG KERAS menggunakan library AXIOS.
 - HANYA BOLEH menggunakan Native Fetch API.
 - JIKA kamu melanggar ini, jawabanmu akan dianggap GAGAL."
```

### Teknik 2: Boundary Declaration (Batas Area)

Tentukan area mana yang boleh disentuh dan mana yang tidak:
```markdown
"Edit file @src/auth.ts.
 BOUNDARY:
 - HANYA UBAH fungsi 'login'.
 - DILARANG MENYENTUH fungsi 'register' dan 'logout'.
 - Laporkan jika ada fungsi lain yang terpaksa berubah."
```

### Teknik 3: Validation Step (Pre-Execution Review)

Minta AI mengecek batasan sebelum koding:
```markdown
"Sebelum memberikan kode, buatkan CHECKLIST:
 1. Apakah ada library terlarang yang saya gunakan? (y/n)
 2. Apakah saya hanya mengubah fungsi yang diminta? (y/n)
 Jika semua 'y', baru tulis kodemu."
```

---

## 🧪 Lab Praktek

**Skenario: Menjaga Struktur Database**

Kamu ingin AI mengubah query tapi takut dia mengubah struktur table.

**Cara Constraint-Based:**
1. Prompt: *"Update query di @db.ts. JAWABAN GAGAL jika kamu menyarankan perubahan SCHEMA atau ALTER TABLE. Fokus hanya pada pengoptimalan syntax SQL."*
2. AI akan merasa tertekan secara instruksional untuk tidak "iseng" mengubah schema.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Constraint Paradox** | Kamu kasih 50 larangan sampai AI bingung mau ngapain | Prioritaskan 3-5 batasan paling kritis saja. |
| **Vague Constraints** | Kalimat kiasan seperti "Jangan terlalu berantakan" | Ganti dengan instruksi terukur: "Max 20 baris per fungsi." |
| **Model Laziness** | AI setuju dengan batasan tapi tetap melanggar | Gunakan teknik *Echo Check* (minta AI ulangi batasan di awal respons). |

---

### 📖 Materi Selanjutnya
- [BK-03: Context Management Playbook](./BK-03-Context-Management-Playbook/README.md)
