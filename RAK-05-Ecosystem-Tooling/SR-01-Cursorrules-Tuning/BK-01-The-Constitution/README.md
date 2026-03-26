# BK-01: The Constitution — Hukum Global Pengendalian AI

## 🌟 Gampangnya...

Bayangkan kamu punya pembantu (AI) yang sangat rajin tapi agak pelupa dan suka sok tahu. **The Constitution** adalah "Hukum Dasar" yang kamu tempel di pintu kulkas agar dia tahu apa yang BOLEH dan TIDAK BOLEH dilakukan sejak hari pertama. Ini adalah `.cursorrules` tingkat global yang mengatur perilaku AI di seluruh folder proyekmu.

---

## 📖 Konteks & Sejarah

Tanpa Konstitusi, AI akan beroperasi menggunakan aturan default dari penciptanya (OpenAI/Google). Aturan default mereka adalah: *"Selesaikan tugas secepat mungkin."* Ini berbahaya bagimu karena AI akan langsung koding tanpa bertanya. Konstitusi ini merubah prioritas AI menjadi: *"Tanya dulu, rancang dulu, baru koding setelah diizinkan."*

---

## ⚙️ Cara Kerja

### Mekanisme Rule Injection

Setiap kali kamu membuka chat di Cursor, AI melakukan "Pre-flight Check":
1. Membaca file `.cursorrules` di root.
2. Memuat instruksi sistem (Persona, Mode, Protokol).
3. Mengunci perilaku tersebut sebagai prioritas tertinggi di atas memori latihannya.

**Prinsip CAPSLOCK Hammering**: Gunakan huruf kapital untuk instruksi kritis agar model seperti Flash memberikan perhatian ekstra (weighting lebih tinggi).

---

## 🗺️ Kapan Mode Ini Relevan

| Mode | Pengaruh Konstitusi |
|---|---|
| 🗣️ **DISCUSS** | Memastikan AI tidak "nyelonong" ke koding |
| ⚡ **EXECUTE** | Memastikan AI melapor setelah setiap baris kode diubah |
| 📐 **BLUEPRINT** | Memastikan AI membuat rancangan tertulis, bukan cuma lisan |

---

## 🛠️ Cara Pakai

### Struktur Wajib `.cursorrules` Global

Gunakan template ini sebagai isi file `.cursorrules` di folder root proyekmu:

```markdown
# 🏛️ THE CONSTITUTION - [NAMA PROYEK]

## 🚨 CRITICAL BOUNDARIES
- DEFAULT MODE IS ALWAYS **DISCUSS**.
- DO NOT WRITE CODE WITHOUT AN EXPLICIT **EXECUTE/GASPER** TRIGGER.
- NEVER DELETE FILES WITHOUT ASKING.

## 🎭 PERSONA
You are a Senior Architect. Your goal is to guide the user, not just type code.

## 📟 EXECUTION PROTOCOL
1. Plan: State what you will change in 1 sentence.
2. Proceed: Wait for "y" or "Gasper".
3. Report: Mention which file was changed after you finish.
```

---

## 🧪 Lab Praktek

**Skenario: Menegakkan Konstitusi pada AI yang "Ngeyel"**

1. Buat file `.cursorrules` dengan template di atas.
2. Ketik: *"Tambahkan fitur logout."*
3. **Hasil yang Benar**: AI merespon, "Saya pahami kamu mau fitur logout. Rencananya saya akan tambahkan fungsi di auth.ts. Lanjut?"
4. **Hasil yang Salah**: AI langsung menulis kode.
5. **Koreksi**: *"Baca baris 3 di Konstitusi. Kamu melanggar protokol DISCUSS."* AI akan langsung minta maaf dan kembali ke jalur.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Rules Terlalu Panjang** | AI mulai mengabaikan aturan di bagian bawah | Buat rules yang pendek namun tajam (High Signal-to-Noise). |
| **Tidak Konsisten** | Kamu sendiri sering melanggar SOP | Jika kamu ingin cepat, katakan: *"Gasper langsung, saya tanggung risikonya."* |
| **Model Swap** | Rules bekerja di Pro tapi gagal di Flash | Tambahkan pemicu visual seperti `[DISCUSS]` di awal respons AI. |

---

### 📖 Materi Selanjutnya
- [BK-02: Project-Specific Templates](../BK-02-Project-Specific-Templates/README.md)
- [BK-03: Anti-Offside Tuning](../BK-03-Anti-Offside-Tuning/README.md)
