# CH-02: Prompt Compression

## 📖 1. The Efficiency of Context
Setiap word dalam prompt Anda memakan **Token Context Window**. Mengompresi prompt berarti memberikan instruksi maksimal dengan penggunaan token minimal.

## ⚙️ 2. Compression Techniques
- **Referential Prompting**: Gunakan simbol `@` atau `#` untuk merujuk ke file/dokumen (misal: "Gunakan pola di `@BK-01`").
- **Eliminating Politeness**: Hapus kata-kata seperti "Tolong", "Terima kasih", "Bisa tidak ya". AI adalah mesin; ia lebih mengerti instruksi langsung.
- **Shorthand Standards**: Gunakan istilah teknis yang sudah kita sepakati di SOP (misal: "Apply PPM V4 to this BK").

## 📊 3. Before vs After
**Before (Long-winded):**
"Halo Cursor, bisakah kamu membantu saya merapikan kode ini agar terlihat lebih profesional dan tolong ikuti standar yang sudah kita buat sebelumnya ya."

**After (Compressed):**
"Refactor file ini sesuai standar PPM V4 di `@RAK-01`. Pastikan clean code."

## 🚀 4. Benefit
Prompt yang ringkas mengurangi risiko AI mengalami kebingungan (*Instruction Forgetting*) di tengah jalan karena terlalu banyak teks yang tidak relevan.
