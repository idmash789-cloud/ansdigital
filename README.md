# Ans Digital — Web Profil

Situs profil statis untuk Ans Digital, developer aplikasi Android di Google Play.

## Isi situs

- `index.html` — halaman profil (hero, Tentang, 4 kartu aplikasi, Kontak, footer)
- `style.css` — satu file CSS, tanpa framework dan tanpa build step
- `README.md` — file ini

## Aplikasi yang ditampilkan

Semua data diambil dari halaman developer Ans Digital di Google Play
(https://play.google.com/store/apps/dev?id=5549052497389775441&hl=en, dicek 8 Nov 2026).
Semua aplikasi gratis.

1. **BestSeller Book Summary** — https://play.google.com/store/apps/details?id=com.book.summary
2. **Kalkulator Weton** — https://play.google.com/store/apps/details?id=com.weton.app
3. **99 Pertanyaan Seputar Ramadhan** — https://play.google.com/store/apps/details?id=com.sembilansembilan.pertanyaanseputarramadhan
4. **Habib Umar Bin Hafidz Walpaper** — https://play.google.com/store/apps/details?id=com.AnsDigitalApp.habibumarbinhafidzwallpaper

Judul "Walpaper" ditulis persis seperti di Play Store. Jangan mengubahnya
menjadi "Wallpaper" tanpa keputusan dari pemilik akun.

Domain situs ini: https://ansdigital.techo.web.id (custom domain, diatur di dashboard Cloudflare Pages).
Kontak: sopport.offisial@gmail.com

## Menjalankan secara lokal

Buka `index.html` langsung di browser, atau jalankan server statis dari folder ini:

```bash
cd ansdigital
python3 -m http.server 8000
```

Lalu buka http://localhost:8000

## Deploy

### Cloudflare Pages (cara yang dipakai proyek lain)

1. Di Cloudflare Pages, buat proyek baru dan hubungkan repo
   `idmash789-cloud/ansdigital` (branch `main`).
2. Framework preset: **None** / situs statis. Build command: kosong.
   Output directory: `/` (root repo).
3. Deploy. Setiap push ke `main` akan ter-deploy otomatis.

   Custom domain `ansdigital.techo.web.id` dipasang di dashboard Cloudflare
   Pages (Custom domains) oleh pemilik akun, mengarah ke proyek ini.

### GitHub Pages

1. Di repo GitHub, buka **Settings → Pages**.
2. Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Simpan. Situs terbit di `https://idmash789-cloud.github.io/ansdigital/`.

## Cara update daftar aplikasi

1. Edit kartu aplikasi di `index.html` (nama, deskripsi, link Google Play).
   Tambahkan kartu baru dengan pola yang sama bila ada aplikasi baru.
2. Jangan menambahkan jumlah unduhan, rating, alamat, atau nomor kontak
   kecuali sudah terverifikasi dari sumber resmi atau diberikan langsung
   oleh pemilik akun. Email kontak saat ini: sopport.offisial@gmail.com.
3. Commit dan push ke branch `main` — deploy berjalan otomatis
   (Cloudflare Pages) atau setelah GitHub Pages membaca commit terbaru.
