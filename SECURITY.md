# Kebijakan Keamanan & Pelaporan Kerentanan (Security Policy)

Asosiasi Nazhir Indonesia (ANI) menjaga integritas, kerahasiaan, dan ketersediaan seluruh infrastruktur digital wakaf nasional, data keanggotaan, serta sistem sertifikasi kompetensi.

## Ruang Lingkup (Scope)

Kebijakan ini berlaku untuk seluruh aset digital dan repositori di bawah organisasi `asosiasinazhir`, termasuk namun tidak terbatas pada:
- Portal resmi keanggotaan, direktori CWC™, dan e-Sekretariat (`https://www.ani.or.id`)
- Dashboard Wakaf Nasional (`https://nazhir.id`)
- Seluruh repositori open-source (`waqf-chain`, `waqf-odoo-modules`, `waqf-odoo-docker`, `waqf-agentic-workflow`, `nazhir-reach`, `nazhir.id`, dan `.github`)

## Cara Melaporkan Kerentanan (Responsible Disclosure)

**JANGAN** membuka GitHub Issue publik atau diskusi terbuka untuk melaporkan celah keamanan, kebocoran data, atau kredensial yang terekspos.

Silakan kirim laporan secara privat melalui salah satu kanal resmi berikut:
- **Email Keamanan & Teknis**: `info@ani.or.id` dan `sekretariat@ani.or.id` (subjek: `[SECURITY] <Nama Sistem/Repo> — <Ringkasan Singkat>`)
- **GitHub Private Vulnerability Reporting**: Gunakan fitur *Report a vulnerability* pada tab *Security* di repositori terkait apabila tersedia.

Sertakan informasi berikut agar tim teknis dapat menindaklanjuti dengan cepat:
1. Deskripsi kerentanan dan dampak potensial.
2. Langkah reproduksi (*Proof of Concept* / endpoint / payload non-destruktif).
3. Perkiraan tingkat keparahan dan saran mitigasi bila ada.

Kami menargetkan konfirmasi penerimaan laporan dalam **2×24 jam** hari kerja dan koordinasi perbaikan sebelum pengungkapan publik.

## Aturan Keras Perlindungan Data & Kredensial

Seluruh kontributor dan pengelola repositori **DILARANG KERAS** melakukan commit atau mempublikasikan:
1. **Data Pribadi (PII)**: NIK, foto KTP, nomor telepon pribadi, data sertifikat privat, atau *database dump* mentah anggota.
2. **Kunci Kriptografi & Konfigurasi Server**: `ANI_SEK_KEY`, `wp-config.php`, kunci API payment gateway/WhatsApp gateway, OAuth token, atau private key wallet produksi.
3. **Log Operasional Mentah**: Berkas log server yang memuat sesi autentikasi, token header, atau payload webhook produksi.
