# BK-02: Mental Models — Menyamakan Frekuensi dengan AI

## 🌟 Gampangnya...

AI tidak berpikir seperti manusia. Dia tidak punya "akal sehat" (common sense), tapi dia punya "logika probabilitas" yang luar biasa. **Mental Model** adalah cara kamu memahami "cara pikir" AI tersebut. Saat kamu paham bahwa AI adalah sebuah sistem yang memprediksi kata berikutnya berdasarkan konteks, kamu tidak akan lagi marah saat dia salah — tapi kamu akan memperbaiki konteksnya.

---

## 📖 Konteks & Sejarah

Kebanyakan orang gagal menggunakan AI karena mereka memperlakukan AI seperti manusia ("Kamu tahu kan maksud saya?"). AI tidak tahu maksudmu kecuali kamu menuliskannya. Memahami konsep **Prompting as Architecture** (Prompting sebagai kegiatan membangun struktur) akan merubah hasil kerjamu dari 50% benar menjadi 99% benar.

---

## ⚙️ Cara Kerja

### 3 Mental Model Utama

1. **AI as a Library Specialist**: AI tahu semua buku di perpustakaan, tapi dia butuh kamu buat ngambilin bukunya (@file) agar dia bisa jawab spesifik.
2. **AI as an Infinite Junior**: Dia rajin luar biasa tapi butuh arahan baris demi baris. Jangan kasih instruksi abstrak.
3. **AI as a Pattern Matcher**: AI akan terus meniru pola yang ada di chat. Jika chatmu berantakan, jawaban AI akan berantakan. Jika chatmu terstruktur, AI akan jadi sangat jenius.

---

## 🗺️ Kapan Mode Ini Relevan

| Mental Model | Kapan Pakai |
|---|---|
| **Library Specialist** | Saat butuh jawaban teknis mendalam (RAK-04). |
| **Infinite Junior** | Saat proses delegasi koding (EXECUTE). |
| **Pattern Matcher** | Saat membangun standar koding (Few-Shot). |

---

## 🛠️ Cara Pakai

### Teknik "Contextual Clarity"

Jangan berasumsi AI tahu apa yang ada di kepalamu. Gunakan rumus ini:
**[Konteks (Apa/Dimana)] + [Task (Lakukan apa)] + [Batasan (Jangan apa)]**

*Contoh:*
"Di file @main.ts (Konteks), tolong bersihkan fungsi login ini (Task), tapi JANGAN ganti library auth-nya (Batasan)."

---

## 🧪 Lab Praktek

**Skenario: Memperbaiki "Miskomunikasi"**

1. Beri instruksi yang sengaja ambigu: *"Bikin fitur login yang bagus."*
2. Lihat hasilnya (pasti berantakan).
3. Gunakan Mental Model "Infinite Junior": *"Oke, saya salah perintah. Sekarang: Gunakan @auth-standard.ts, buatlah fungsi login di folder /services, gunakan JWT, dan lapor kalau sudah selesai."*
4. Lihat perubahannya. AI jadi jauh lebih tajam.

---

## ⚠️ Jebakan & Solusi

| Jebakan | Gejala | Solusi |
|---|---|---|
| **Anthropomorphism** | Kamu curhat ke AI dan berharap dia "paham" perasaanmu | Tetap teknis dan instruksional. AI tidak punya perasaan, dia cuma punya data. |
| **Assumed Knowledge** | Kamu kaget AI gak tahu file X padahal nggk kamu mention | Selalu gunakan `@` untuk memanggil file. AI tidak bisa membaca pikiranmu. |
| **Garbage-In Garbage-Out** | Chatmu penuh typo dan instruksi bertabrakan | Jika chat sudah kotor, gunakan **Session Refresh Protocol** (RAK-06). |

---

### 📖 Materi Selanjutnya
- [RAK-03: Evolution & Interfacing](../../RAK-03-Evolution-Interfacing/README.md)
