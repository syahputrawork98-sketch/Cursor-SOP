# BK-01: Role Switching Patterns — Teknik Ganti "Topi" AI

## 🌟 Gampangnya...

AI secara default adalah seorang "Asisten Umum". Tapi di tengah jalan, kamu mungkin butuh dia menjadi "Security Expert", "UX Designer", atau "Senior Arsitek". **Role Switching** adalah teknik memerintahkan AI untuk berganti kepribadian secara eksplisit dalam satu sesi chat. Dengan berganti "topi", AI akan fokus pada sudut pandang yang berbeda dan memberikan saran yang jauh lebih tajam daripada sekadar asisten umum.

---

## 📖 Konteks & Sejarah

Model LLM dilatih dengan role yang sangat luas. Namun, jika kita tidak menyempitkan fokusnya, AI cenderung memberikan jawaban "rata-rata" (average). Dengan teknik switching, kita mengaktifkan bagian dari memori AI yang memiliki keahlian spesifik. Ini adalah rahasia untuk mendapatkan saran tingkat jenderal dari AI yang tadinya terlihat seperti prajurit biasa.

---

## ⚙️ Cara Kerja

### Mekanisme "System Override"

Saat kamu memerintahkan switch role, AI akan melakukan re-prioritisasi terhadap aturannya sendiri. 
- **Asisten Umum**: Fokus pada menyelesaikan task dengan cepat.
- **Security Auditor**: Fokus pada mencari kerentanan, mengabaikan kecepatan.
- **Performance Engineer**: Fokus pada efisiensi memori dan waktu eksekusi.

---

## 🗺️ Kapan Mode Ini Relevan

| Saat Bekerja | Role yang Harus Dipanggil |
|---|---|
| Baru mau mulai fitur | **Senior Architect** (Desain sistem). |
| Selesai ngetik kode | **Cruel Code Reviewer** (Cari kesalahan). |
| Aplikasi terasa lambat | **Performance Optimizer** (Cari bottleneck). |
| Menangani data sensitif | **Cybersecurity Expert** (Enkripsi & Sanitasi). |

---

## 🛠️ Cara Pakai

### Teknik "Explicit Switch"

Gunakan kalimat perintah beralih role secara formal:
```markdown
"HENTIKAN mode asisten. Sekarang, masuk ke mode SENIOR DEVOPS ENGINEER. 
 Audit file @docker-compose.yml ini. 
 Jangan memuji kode saya, fokuslah mencari celah konfigurasinya."
```

### Teknik "Role-based Prompting" dalam .cursorrules

Tanamkan trigger di rules:
```markdown
# TRIGGER: AUDIT
"Jika saya mengetik AUDIT, kamu otomatis berganti role menjadi 
 QA Engineer Senior yang sangat cerewet."
```

---

## 🧪 Lab Praktek

**Skenario: Mencari celah keamanan**

1. Tunjukkan kode login sederhana ke AI.
2. Pertama, tanya sebagai asisten: *"Apakah kodingan ini oke?"* (Jawabannya pasti: "Ya, oke...").
3. Kedua, paksa switch: *"Sekarang beraktinglah sebagai Hacker Topi Hitam (Black Hat) yang ingin menjebol sistem ini. Di mana letak kelemahannya?"*
4. **Hasil**: AI akan menemukan 3-4 celah yang tadi tidak ia sadari.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Role Drift** | Setelah beberapa turn, AI kembali ke kepribadian lamanya | Gunakan **Context Anchoring** (RAK-06) untuk mengunci role tersebut secara berkala. |
| **Conflicting Roles** | Kamu memanggil 2 role bertabrakan sekaligus | Gunakan satu-satu. Satu turn = Satu role. |
| **Persona Overacting** | AI jadi terlalu cerewet sampai tidak memberikan solusi | Gunakan instruksi: *"Be a critic, but also give the fix."* |

---

### 📖 Materi Selanjutnya
- [BK-02: The Critic Pattern](../BK-02-The-Critic-Pattern/README.md)
