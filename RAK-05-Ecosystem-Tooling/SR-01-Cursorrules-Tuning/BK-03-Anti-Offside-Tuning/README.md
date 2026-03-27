# BK-03: Anti-Offside Tuning â€” Menjinakkan AI yang "Sok Tahu"

## ðŸŒŸ Gampangnya...

Pernahkah kamu minta AI untuk "cuma buat rencana", tapi dia malah langsung menulis 200 baris kode yang merusak struktur? Itu namanya **Offside** (melewati batas). Fenomena ini sering terjadi pada model yang cepat seperti Gemini Flash. Buku ini mengajarkan teknik khusus untuk memasang "pagar betis" agar AI tidak bisa nyelonong sembarangan sebelum kamu beri izin.

---

## ðŸ“– Konteks & Sejarah

Model AI seperti Flash dilatih untuk menjadi asisten yang sangat responsif. Dalam "pikirannya", cara terbaik membantu user adalah dengan memberikan kode secepat mungkin. Masalahnya, dia sering melompati fase diskusi yang krusial. Teknik **Anti-Offside Tuning** dikembangkan untuk meredam agresivitas ini tanpa mengurangi kecerdasan AI-nya.

---

## âš™ï¸ Cara Kerja

### Mekanisme "Mental Brake"

Kita menanamkan instruksi yang memaksa AI melakukan jeda (pause) sebelum melakukan aksi modifikasi. Teknik ini bekerja pada lapisan sistem instruksi (system prompt) yang lebih diprioritaskan oleh model daripada instruksi di tengah diskusi.

---

## ðŸ—ºï¸ Kapan Mode Ini Relevan

| Situasi | Mode | Kenapa Perlu Tuning? |
|---|---|---|
| **Eksplorasi Ide** | ðŸ—£ï¸ **DISCUSS** | Agar AI tidak langsung buat file dummy. |
| **Mulai Proyek** | ðŸ“ **BLUEPRINT** | Agar AI tidak langsung "Gasper" tanpa gambar teknik. |
| **Debug Sulit** | ðŸ”¬ **ANALYZE** | Agar AI tidak tebak-tebak berhadiah dengan kode. |

---

## ðŸ› ï¸ Cara Pakai

### Teknik 1: CAPSLOCK Hammering (Untuk Isu Mendesak)

Gunakan huruf kapital untuk perintah yang sangat krusial. Model Flash merespon "bobot" kata caps lebih tinggi:
```markdown
# WRONG (terlalu lembut):
"Please discuss first before coding."

# RIGHT (CAPSLOCK Hammering):
"CRITICAL: DO NOT WRITE CODE WITHOUT AN EXPLICIT 'GASPER' TRIGGER FROM THE USER. 
 FAILURE TO DO SO IS AN ARCHITECTURAL INTEGRITY FAILURE."
```

### Teknik 2: The Echo Check (Pengecekan Gema)

Minta AI untuk mengulangi instruksimu sebelum mulai:
```markdown
# Tambah ke .cursorrules:
"Before starting ANY task, summarize the requirement in 1 sentence 
 and say: 'Shall we proceed to BLUEPRINT?'"
```

### Teknik 3: Negative Constraint with Examples (Anti-Offside Layer)

Berikan perbandingan agar AI paham bedanya:
```markdown
## ðŸš¨ ANTI-OFFSIDE PROTOCOL
Example of WRONG behavior:
User: "Add login page"
AI: [Starts coding login.tsx] âŒ WRONG!

Example of RIGHT behavior:
User: "Add login page"
AI: "I understand you want a login page. Here is the plan: [...] 
     Should we move to BLUEPRINT?" âœ… RIGHT!
```

---

## ðŸ§ª Lab Praktek

**Skenario: Menghukum Flash yang Kebablasan**

1. Kamu pakai Gemini Flash. Kamu minta analisis fitur X.
2. Flash langsung buat file `feature-x.ts`.
3. **Konsekuensi**: Jangan biarkan! Ketik: *"Kamu baru saja OFFSIDE. Baca .cursorrules baris 10. Hapus file itu dan kembali ke DISCUSS."*
4. Ini melatih AI (dan sistem indexing) bahwa batasannya sangat keras.

---

## âš ï¸ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Ambiguous Trigger** | Kamu bilang "Oke" tapi maksudnya "Oke lanjut diskusi" | Gunakan kata kunci unik seperti **"GASPER"** atau **"EXECUTE"** sebagai satu-satunya kunci koding. |
| **Rules Ditinggal** | AI mengikuti rules di awal, tapi setelah 20 turn dia lupa | Gunakan teknik *Context Anchoring* dari RAK-06. |
| **Over-strict Rules** | AI jadi terlalu kaku dan tidak mau gerak | Berikan jalur cepat: "For simple fixes, you may EXECUTE directly." |

---

### ðŸ“– Materi Selanjutnya
- [RAK-05/SR-02: IDE Fine-Tuning](../../SR-02-IDE-Fine-Tuning/BK-01-Indexing-Optimization/README.md)

