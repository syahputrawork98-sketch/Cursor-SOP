# CH-01: Chorus of Agents Workflow

## 📖 1. The Power of Many
**Chorus of Agents** adalah teknik orkestrasi di mana beberapa agen dengan persona khusus bekerja sama di bawah arahan satu agen utama (Orchestrator) atau User.

## ⚙️ 2. The Orchestration Pattern
1. **Planner**: Membedah tugas menjadi sub-tugas.
2. **Executor**: Menulis kode berdasarkan sub-tugas.
3. **Reviewer**: Memeriksa bug dan standar koding.
4. **Fixer**: Memperbaiki temuan reviewer.

## 📊 3. Collaboration Diagram
```mermaid
sequenceDiagram
    participant U as User
    participant P as Planner
    participant E as Executor
    participant R as Reviewer
    U->>P: "Add Login Feature"
    P->>E: Task 1: Create DB Schema
    E->>R: Submits Schema
    R->>E: Refactor: Add Index on Email
    E->>R: Updated Schema
    R->>U: Feature Ready
```

## ⚠️ 4. Orchestration Overhead
Semakin banyak agen, semakin besar risiko desinkronisasi. Pastikan ada "Single Source of Truth" (seperti Blueprint di RAK-02) yang bisa diakses oleh seluruh agen.
