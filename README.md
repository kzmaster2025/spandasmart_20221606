# Website SMP Negeri 2 Kota Sukabumi (SPANDA)

React + Vite + Tailwind CSS. Data disimpan di localStorage browser (bukan database).

## Jalankan di komputer
```bash
npm install
npm run dev        # buka alamat yang tampil, biasanya http://localhost:5173
npm run build      # uji build produksi
npm run preview
```

## Publish ke GitHub Pages
1. Buat repository baru di GitHub (nama bebas, misal `web-spanda`), kosong tanpa README.
2. Di folder project:
   ```bash
   git init
   git add .
   git commit -m "Website SPANDA"
   git branch -M main
   git remote add origin https://github.com/USERNAME/NAMA-REPO.git
   git push -u origin main
   ```
3. Di GitHub: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
4. Buka tab **Actions**, tunggu workflow "Deploy ke GitHub Pages" hijau.
5. Alamat: `https://USERNAME.github.io/NAMA-REPO/`

Setiap `git push` ke branch `main` otomatis memperbarui website.

## Yang perlu diganti sebelum online
- `src/App.jsx` bagian atas: `KEPSEK` (foto), `PASSWORDS`, `EXTRAS` (harga), dan data `INITIAL` (guru, agenda, prestasi, ekskul).
- Ganti foto Unsplash dengan foto asli sekolah (simpan di `public/`).
- Logo: `LOGO_ID` (Google Drive, harus "Anyone with the link"); cadangan lokal ada di `public/logo-spanda.png`.
- Perubahan lewat CMS hanya tersimpan di browser pengubah. Untuk mengubah isi bagi semua pengunjung, edit `INITIAL` lalu push.
- Password di kode bisa dibaca siapa saja. Jangan simpan data pribadi asli.
