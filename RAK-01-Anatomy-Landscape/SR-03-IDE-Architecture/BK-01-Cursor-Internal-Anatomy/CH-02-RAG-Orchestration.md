# CH-02: RAG Orchestration

## 📖 1. Beyond Token Prediction
**RAG (Retrieval-Augmented Generation)** adalah jantung dari fitur `@codebase`. Ia menghubungkan kreativitas model bahasa dengan akurasi data lokal Anda.

## ⚙️ 2. The Retrieval Process
- **Chunking**: Kode Anda dipecah menjadi bagian-bagian kecil bermakna.
- **Vectorization**: Setiap chunk diubah menjadi vektor 1536-dimensi (atau sesuai model).
- **Ranking**: Saat Anda bertanya, Cursor membandingkan kueri Anda dengan ribuan vektor dan mengambil 10-20 potong kode yang paling "mirip".

## 📊 3. RAG vs Training
| Aspect | Model Training | RAG Orchestration |
| :--- | :--- | :--- |
| **Knowledge** | Static (Fixed Date) | Dynamic (Real-time) |
| **Cost** | High | Low |
| **Accuracy** | High (General) | High (Domain Specific) |

## 🧪 4. Practical Insight
Gunakan `@codebase` hanya saat Anda butuh visibilitas seluruh proyek. Jika Anda sudah tahu file mana yang relevan, menunjuk file secara spesifik (`@filename`) akan memberikan hasil yang jauh lebih akurat karena meminimalisir "derau" (noise) dari file yang tidak relevan.
