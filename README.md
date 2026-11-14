# Dashboard Produktiviti Buruh Malaysia

Laman web statik bagi prestasi produktiviti buruh Malaysia: Ringkasan Eksekutif, peta negeri, 14 Nexus Produktiviti, sasaran RMK-13, definisi dan formula, serta penjana **Kertas Lembaga Pengarah (Word .docx)**.

Disediakan oleh Seksyen Prestasi Produktiviti dan Ekonomi (SPPE), Perbadanan Produktiviti Malaysia.

> **Perhatian klasifikasi data.** Laman ini mengandungi data 14 Nexus DOSM yang ditanda *rujukan dalaman sahaja, bukan untuk edaran*, dan sasaran Laporan Interim yang *belum muktamad*. Laman GitHub Pages boleh dibuka oleh sesiapa yang tahu pautannya, walaupun repositori ditetapkan *private* (kecuali GitHub Enterprise Cloud dengan kawalan akses). Dapatkan kelulusan SPPE sebelum menerbitkan, atau gunakan pelayan dalaman MPC.

## Kandungan repositori

| Fail | Keterangan |
|---|---|
| `index.html` | Keseluruhan laman, termasuk data dan logo (satu fail). |
| `.nojekyll` | Memastikan GitHub Pages menyiarkan fail apa adanya. |
| `README.md` | Panduan ini. |

Laman ini memuatkan pustaka dari CDN: d3 (cdnjs), docx (jsDelivr) dan fon Plus Jakarta Sans (Google Fonts). Pengguna memerlukan sambungan internet.

## Cara deploy ke GitHub Pages (tanpa arahan baris)

1. Log masuk ke [github.com](https://github.com) dan klik **New repository**.
2. Namakan repositori, contohnya `dashboard-produktiviti-buruh-malaysia`. Pilih **Public**, atau **Private** jika akaun organisasi anda menyokong Pages untuk repositori private.
3. Klik **Create repository**, kemudian **uploading an existing file**.
4. Seret `index.html`, `README.md` dan `.nojekyll` ke halaman itu, kemudian klik **Commit changes**.
   - Jika `.nojekyll` tersembunyi dalam folder anda, langkau sahaja; laman tetap berfungsi.
5. Buka **Settings → Pages**. Di bawah **Build and deployment**, pilih **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**, kemudian **Save**.
6. Tunggu 1–2 minit. Pautan laman dipaparkan di bahagian atas halaman Pages, biasanya:
   `https://NAMA-PENGGUNA.github.io/dashboard-produktiviti-buruh-malaysia/`

## Cara deploy menggunakan Git (pilihan)

```bash
git init
git add index.html README.md .nojekyll
git commit -m "Dashboard Produktiviti Buruh Malaysia"
git branch -M main
git remote add origin https://github.com/NAMA-PENGGUNA/dashboard-produktiviti-buruh-malaysia.git
git push -u origin main
```

Kemudian aktifkan Pages seperti langkah 5 di atas.

## Mengemas kini laman

Muat naik `index.html` baharu ke repositori yang sama (gantikan fail lama). GitHub Pages akan mengemas kini laman dalam beberapa minit. Data disimpan di dalam `index.html`, jadi setiap kemas kini data memerlukan fail baharu.

## Penjana Kertas BOD

Halaman **Jana Kertas BOD** menjana fail Word (.docx) mengikut Templat Nota/Kertas BOD MPC dan memuat turunnya terus ke komputer pengguna. Tiada data dihantar ke pelayan; semua pengiraan dibuat dalam pelayar.

## Sumber data

- DOSM: Produktiviti Buruh mengikut Negeri (Jadual 1–4.5), 2015–2025.
- DOSM/MPC: Jadual Produktiviti Buruh Suku Kedua 2026, 14 Nexus (rujukan dalaman).
- MPC: Laporan Interim Kajian Kerangka dan Pelan Hala Tuju Produktiviti Nasional 2035 (sasaran, trajektori, kluster; belum muktamad).
- Sempadan negeri: Natural Earth 1:10m (domain awam).
