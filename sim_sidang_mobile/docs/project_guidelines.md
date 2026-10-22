# Project Guidelines — Application Flutter & PHP Native (XAMPP)

Panduan ini berisi standar arsitektur, aturan pengkodean, dan workflow Git yang wajib dipatuhi oleh seluruh anggota tim.

---

## 1. Arsitektur & Struktur Proyek

Proyek ini menerapkan pemisahan tanggung jawab (*Separation of Concerns*) antara Frontend (Flutter) dan Backend (PHP Native XAMPP).

### Struktur Folder Flutter
```text
lib/
├── core/           # Konfigurasi global, tema, konstanta API endpoint
├── models/         # Data class & parsing JSON (fromJson, toJson)
├── providers/      # HTTP Client / Services (Koneksi langsung ke API PHP XAMPP)
├── repositories/   # Data Layer (Menghubungkan Provider dengan Controller)
├── controllers/    # Logic & State Management UI
└── views/          # Tampilan UI (screens & reusable widgets)