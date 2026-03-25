# BK-01: The Rust Indexer

> [!NOTE]
> This documentation follows the **PPM V4 Gold Standard**.

## 🔗 1. Source Link
- [Why we rewrite the indexer in Rust (Cursor Blog)](https://cursor.sh/blog/rust-indexer)
- [Fast local code search](https://github.com/BloopAI/bloop)

## 📖 2. Brief & Detailed Explanation
### Brief
Memahami teknologi di balik kecepatan pencarian kode Cursor: Indexer berbasis Rust.

### Detailed
Pencarian kode tradisional (seperti `grep`) terlalu lambat untuk alur kerja AI real-time. Cursor menggunakan **Custom Indexer** yang ditulis dalam **Rust** untuk melakukan sinkronisasi file lokal secara instan. Indexer ini membangun representasi struktural dari kode Anda (AST - Abstract Syntax Tree) dan menyimpannya dalam basis data vektor lokal agar AI dapat menemukan konteks yang tepat dalam milidetik, bahkan pada repositori dengan jutaan baris kode.

## 💡 3. Analogy
Indexer Rust adalah seperti **X-Ray Scanner** di bandara. Ia tidak hanya melihat permukaan koper (nama file), tapi bisa melihat semua isi di dalamnya secara bersamaan dan instan tanpa harus membongkarnya satu per satu.

## 📊 4. Mermaid Diagram
```mermaid
graph LR
    Disk[Local Disk] -->|Watch Events| Indexer[Rust Core]
    Indexer -->|AST Parsing| Features[Semantic Features]
    Features -->|Vectorize| LocalDB[Vector Database]
    LocalDB -->|Query| retrieval[Context Retrieval]
```

## ⚙️ 5. Under-the-hood Mechanics
Menjelaskan sinkronisasi incremental: Indexer hanya memproses bagian file yang berubah (diffs) untuk meminimalisir beban CPU dan memori pada mesin pengguna.

## 📐 9. Chapter List
1. [CH-01: Rust Indexer Deep-dive](./CH-01-Rust-Indexer-Deep-dive.md)
2. [CH-02: Vector Search](./CH-02-Vector-Search.md)

## ⚠️ 7. Pitfalls & Anti-Patterns
- **Ignoring .cursorignore**: Membiarkan file besar (seperti `node_modules` atau `build/`) terindeks, yang menyebabkan "polusi" pada hasil pencarian konteks.
- **Large Binary Files**: Menaruh dataset raksasa di dalam repo koding yang bisa memperlambat performa indexer.
