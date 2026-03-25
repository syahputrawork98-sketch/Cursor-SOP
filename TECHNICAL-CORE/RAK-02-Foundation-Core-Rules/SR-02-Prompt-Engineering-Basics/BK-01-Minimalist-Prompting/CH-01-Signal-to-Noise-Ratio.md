# CH-01: Signal-to-Noise Ratio

## 📖 1. The Quality of Instruction
Dalam Prompt Engineering, **Signal** adalah instruksi yang berguna, sedangkan **Noise** adalah kata-kata basa-basi atau ambigu yang mengaburkan tujuan.

## ⚙️ 2. Increasing Signal
- **Be Specific**: Ganti "Buat kode yang bagus" dengan "Gunakan arsitektur modular dengan clean code principle".
- **Use Constraints**: Berikan batasan apa yang *tidak* boleh dilakukan (misal: "Jangan gunakan library eksternal").
- **Direct Commands**: Gunakan kata kerja imperatif (Buat, Hapus, Perbaiki, Audit).

## 📊 3. Prompt Audit
| Prompt | Quality | Reason |
| :--- | :--- | :--- |
| "Tolong bantu saya buat fitur login" | 🔴 Low Signal | Terlalu umum, tidak ada detail teknis. |
| "Buat fungsi login di `auth.py` pakai JWT" | 🟡 Medium Signal | Lebih spesifik tapi minim error handling. |
| "Implementasikan JWT Login di `auth.py` sesuai RAK-02" | 🟢 High Signal | Sangat spesifik dan merujuk pada standar SOP. |

## 📐 4. The Golden Rule
Gunakan sesedikit mungkin kata untuk mendapatkan sebanyak mungkin hasil. AI yang cerdas tidak butuh esai panjang; ia butuh konteks yang tepat.
