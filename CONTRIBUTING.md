# Panduan Kontribusi (Contributing Guidelines)

Terima kasih telah berkontribusi pada infrastruktur terbuka **Asosiasi Nazhir Indonesia (ANI)** menuju **Smart Nazhir Ecosystem 2030**.

## Alur Kerja Kontribusi

1. **Fork & Branch**: Buat fork dari repositori tujuan, lalu kerjakan perubahan pada branch fitur/perbaikan baru (`feat/<topik>` atau `fix/<topik>`), bukan langsung di `main`.
2. **Conventional Commits**: Gunakan format pesan commit standar:
   - `feat:` fitur atau modul baru
   - `fix:` perbaikan bug atau celah keamanan
   - `docs:` pembaruan dokumentasi
   - `refactor:` perapihan struktur kode tanpa mengubah perilaku
   - `chore:` konfigurasi, dependensi, atau pemeliharaan rutin
3. **Pull Request**: Sertakan penjelasan jelas, bukti pengujian lokal/linting, dan lengkapi seluruh checklist pada templat PR.

## Prinsip Integritas Syariah, Regulasi & Keamanan Data

Setiap perubahan kode pada sistem finansial, ERP, maupun ledger ANI wajib mematuhi aturan dasar berikut:

1. **Keutuhan Pokok Wakaf (100% Intact Principal)**:
   - Untuk transaksi wakaf uang, pokok wakaf **tidak boleh berkurang sepeser pun** akibat biaya administrasi, *MDR fee* payment gateway, atau pembulatan. Potongan biaya wajib ditanggung atau ditalangi dari pos operasional/infak terpisah.
2. **Pemisahan Akun Akad (`PSAK 112` & `PSAK 412`)**:
   - Pencatatan dana wakaf abadi, hasil pengelolaan bersih (termasuk hak imbalan nazhir maks. 10% sesuai UU No. 41/2004 Pasal 12), infak/sedekah, dan dana operasional harus terpisah secara ketat pada tingkat skema data dan jurnal akuntansi.
3. **Sanitasi Data Pribadi & Kredensial**:
   - Gunakan data sintetis/dummy untuk pengujian (*unit test* & *fixture*). Jangan pernah menyertakan NIK asli, data anggota produksi, atau rahasia konfigurasi (`.env`, API key, encryption key) dalam commit maupun deskripsi PR.
4. **Kualitas & Pemeriksaan Sebelum Push**:
   - Pastikan linter, *type-check*, *unit test*, dan validasi markup/YAML/SVG berjalan bersih sebelum mengajukan Pull Request.
