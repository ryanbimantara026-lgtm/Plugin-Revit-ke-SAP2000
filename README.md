REVIT 2026 -> SAP2000 v22 | BALOK DAN KOLOM
RevitToSAP 0.1.0 (ekstensi pyRevit)

1. Pasang pyRevit yang mendukung Revit 2026 dan pembaruan Revit kamu:
   https://github.com/pyrevitlabs/pyRevit/releases
   Ekstensi ini memakai mesin IronPython bawaan pyRevit.
2. Tutup Revit dan ekstrak seluruh paket ini.
3. Tekan Win+R dan buka: %APPDATA%\pyRevit\Extensions
4. Salin folder RevitToSAP.extension beserta semua isinya ke sana.
5. Buka Revit 2026. Cari tab Revit to SAP.

TOMBOL:
- Revit ke SAP22: baca garis Analytical Model balok/kolom dari proyek.
- Excel CSV ke SAP22: konversi CSV/TXT/XLSX (sheet Members) ke S2K.

HASIL:
Folder baru berisi model.s2k, members.csv, joints.csv, frames.csv dan laporan.
Impor model.s2k di SAP2000: File > Import > SAP2000 .s2k Text File.

CAKUPAN:
S2K hanya geometri. Profil, material, rotasi lokal, tumpuan, beban, release,
offset dan kombinasi harus ditetapkan/diperiksa di SAP2000 sebelum analisis.
Model analitis harus tersedia; plugin tidak menebak sumbu dari geometri solid.

UJI AWAL:
Coba examples\hasil_portal\model.s2k: bentang 6 m, tinggi 3 m,
4 joint dan 3 frame. Konverter telah diuji otomatis, tetapi belum diuji
langsung pada Revit 2026 atau SAP2000 v22 di lingkungan pembuat paket.

Panduan lengkap: README.md
Contoh Excel: examples\Contoh_Excel_SAP22.xlsx
Hapus plugin: tutup Revit lalu hapus folder RevitToSAP.extension tadi.
