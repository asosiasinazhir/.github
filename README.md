# Asosiasi Nazhir Indonesia (ANI) — `.github` Organization Profile & Governance

Repositori ini mengelola profil publik resmi organisasi GitHub [**Asosiasi Nazhir Indonesia (ANI)**](https://github.com/Asosiasi-Nazhir-Indonesia) serta standar tata kelola perangkat lunak terbuka di seluruh repositori organisasi.

## Struktur Direktori

```text
.github/
├── .github/workflows/
│   └── validate-profile.yml     # Validasi CI otomatis SVG, YAML, & dokumen wajib
├── ISSUE_TEMPLATE/
│   ├── bug_report.yml           # Formulir pelaporan bug terstruktur
│   ├── config.yml               # Tautan resmi & pengalihan isu non-kode ke ani.or.id
│   └── feature_request.yml      # Formulir usulan fitur & modul baru
├── assets/
│   ├── logo_ani.png             # Logo resmi ANI (500x500 PNG transparan)
│   ├── banner-dark.svg / light  # Kartu indikator utama ekosistem ANI
│   ├── divider-dark.svg / light # Pemisah geometris dark/light responsif
│   └── footer-dark.svg / light  # Banner visi kelembagaan dark/light responsif
├── profile/
│   └── README.md                # Halaman profil utama organisasi di GitHub
├── CODE_OF_CONDUCT.md           # Kode etik kolaborasi berbasis Amanah & Nazhir BERDAYA
├── CONTRIBUTING.md              # Panduan kontribusi kode, commit, & kepatuhan syariah
├── PULL_REQUEST_TEMPLATE.md     # Daftar periksa standar Pull Request
├── SECURITY.md                  # Kebijakan keamanan & pelaporan kerentanan privat
└── SUPPORT.md                   # Kanal bantuan & layanan anggota resmi ANI
```

## Validasi Lokal

Sebelum mengirim pembaruan, pastikan seluruh aset SVG dan konfigurasi YAML valid:

```bash
python3 - <<'EOF'
import glob, xml.etree.ElementTree as ET, yaml

for svg in sorted(glob.glob("assets/*.svg")):
    ET.parse(svg)
    print(f"OK SVG: {svg}")

for yml in sorted(glob.glob(".github/workflows/*.yml") + glob.glob("ISSUE_TEMPLATE/*.yml")):
    with open(yml, "r", encoding="utf-8") as fh:
        yaml.safe_load(fh)
    print(f"OK YAML: {yml}")
EOF
```
