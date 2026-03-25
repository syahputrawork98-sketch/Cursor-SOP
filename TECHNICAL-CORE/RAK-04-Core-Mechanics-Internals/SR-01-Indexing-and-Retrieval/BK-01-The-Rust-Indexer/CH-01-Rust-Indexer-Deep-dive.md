# CH-01: Rust Indexer Deep-dive

## 📖 1. Why Rust?
Kecepatan adalah segalanya dalam indexing. Rust dipilih karena performa memori yang aman dan konkurensi tingkat tinggi yang memungkinkan pemindaian jutaan baris kode tanpa lag di UI.

## ⚙️ 2. Core Components
- **Tree-sitter Integration**: Untuk parsing sintaks kode secara akurat di berbagai bahasa.
- **File Watcher**: Mendeteksi perubahan file di tingkat OS dan melakukan re-indexing instan.
- **Compression Logic**: Mengompresi AST (Abstract Syntax Tree) agar tidak memakan banyak RAM.

## 📊 3. Performance Metrics
| Method | Speed | Accuracy |
| :--- | :--- | :--- |
| Simple Grep | 🐢 Slow | Low (Keyword only) |
| Standard AST | 🚗 Medium | High (Contextual) |
| Rust-Optimized | 🚀 Blazing | Ultra High (Semantic) |

## ⚠️ 4. Limitation
Indexer Rust sangat bergantung pada integritas file `.cursorignore`. Jika file biner atau `node_modules` masuk ke indeks, performa akan turun drastis.
