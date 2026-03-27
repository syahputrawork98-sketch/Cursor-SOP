# BK-02: The Critic Pattern — Menggunakan AI untuk Mengaudit AI

## 🌟 Gampangnya...

Dua kepala lebih baik daripada satu, bahkan di dunia AI. **The Critic Pattern** adalah teknik di mana kamu meminta satu model AI untuk membuat solusi, lalu meminta model AI kedua (atau model yang sama dengan role berbeda) untuk menjadi "kritikus" yang kejam. Tujuannya adalah untuk menghancurkan solusi pertama agar kamu bisa membangun solusi kedua yang jauh lebih kuat dan anti-peluru.

---

## 📖 Konteks & Sejarah

Bias konfirmasi (*confirmation bias*) juga terjadi pada AI. Jika AI yang sama membuat dan mengaudit kodenya sendiri dalam satu tarikan nafas, dia cenderung mengabaikan kesalahannya. Dengan memisahkan proses "Menciptakan" (Creator) dan "Mengkritik" (Critic), tingkat akurasi kode meningkat hingga 40%.

---

## ⚙️ Cara Kerja

### The Duel Protocol (Protokol Duel)

1. **The Creator**: Membuat draf kodingan.
2. **The Critic**: Mencari 5 kesalahan tersembunyi di draf tersebut.
3. **The Refiner**: Memperbaiki draf berdasarkan kritikan tadi.

---

## 🗺️ Kapan Mode Ini Relevan

| Task | Urgensi Critic |
|---|---|
| **Logic Bisnis Sensitif** | **VVIP** (Wajib audit 2 lapis). |
| **Database Migration** | Kesalahan kecil = Data loss. |
| **API Integration** | Memastikan semua edge case ditangani. |

---

## 🛠️ Cara Pakai

### Teknik "The Self-Debate" (Internal)

Dalam satu chat, suruh AI berdebat dengan dirinya sendiri:
```markdown
"1. Proposal: Buat fungsi [X].
 2. Critic: Berperanlah sebagai Senior Developer yang skeptis. 
    Kritik proposal di atas habis-habisan.
 3. Final: Gabungkan keduanya menjadi solusi yang paling aman."
```

### Teknik "Cross-Model Audit" (External)

Ini cara paling ampuh:
1. Generate kode di **Gemini Pro** (Anti-gravity).
2. Copy kodenya, buka chat baru dengan **GPT-4o** (ChatGPT).
3. Ketik: *"Saya ingin audit kode ini secara mendalam. Temukan celah logika yang dilewatkan oleh developer sebelumnya."*
4. Bandingkan hasilnya.

---

## 🧪 Lab Praktek

**Skenario: Menciptakan Algoritma yang Efisien**

1. Minta AI tulis fungsi sorting yang unik.
2. Gunakan pattern: *"Bagus, sekarang beraksi-lah sebagai Performance Auditor. Mengapa algoritma yang kamu buat tadi tidak efisien untuk data 1 juta baris?"*
3. Lihat AI "menyerang" buatannya sendiri.
4. Perintahkan: *"Sekarang perbaiki kekurangannya."*

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Soft Critic** | "Kritik" AI terlalu ramah ("Kodenya sudah bagus...") | Paksa dengan batasan: *"Sebutkan minimal 5 kesalahan fatal. JANGAN MEMUJI."* |
| **Blind Follow** | Kamu langsung ikuti kritikan AI tanpa mengevaluasi kembali | Ingat, kamu adalah Hakim-nya. AI A and AI B boleh berdebat, tapi keputusan akhir ada di tanganmu. |
| **Complexity Overload** | Perdebatan AI jadi terlalu teknis dan rumit | Suruh mereka menyederhanakan kesimpulan perdebatan ke dalam **Action Plan**. |

---

### 📖 Materi Selanjutnya
- [BK-01: Post-Execute Audit Ritual](../../SR-02-Review-Rituals/BK-01-Post-Execute-Audit-Ritual/README.md)
