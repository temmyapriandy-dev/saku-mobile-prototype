# SAKU Mobile Prototype V4 — Account Linking, Monthly Budget & AI QR Payment

Paket prototype HTML end-to-end untuk demo produk di HP dan presentasi investor melalui laptop/proyektor.

## File utama

- `START_HERE.html` — halaman pemilih mode.
- `index.html` — versi aplikasi mobile full-screen untuk dibuka di HP.
- `presentation.html` — versi presentasi investor dengan phone frame dan panel walkthrough.
- `vercel.json` — konfigurasi deployment sederhana ke Vercel.

## Perubahan V4

### 1. Fitur tambah akun / wallet kembali tersedia

Akses melalui:

- Dashboard → **Kelola / Tambah** pada bagian “Dompet & rekening kamu”.
- Kartu **Tambah akun** di ujung daftar wallet.
- Profil → **Akun Tersambung**.

Flow end-to-end:

`Dashboard → Akun & Wallet → Tambah Akun Baru → Pilih bank/e-wallet → Simulasi authorization read-only → Sinkronisasi → Akun berhasil ditambahkan → Saldo masuk dashboard → Atur budget akun baru.`

Sumber baru yang tersedia untuk demo:

- ShopeePay
- Mandiri
- BRI
- blu
- SeaBank

Setelah akun baru ditambahkan, prototype otomatis memperbarui:

- total saldo;
- safe-to-spend;
- jumlah akun aktif;
- budget keseluruhan;
- pilihan sumber dana pada AI QR recommendation;
- halaman pengaturan budget per wallet.

### 2. Smart Monthly Budget

User dapat mengatur:

- batas pengeluaran total seluruh akun per bulan;
- batas pengeluaran masing-masing wallet/rekening;
- dana minimum yang tidak boleh digunakan;
- warning pada 80%;
- penurunan prioritas AI ketika budget mencapai/melewati 100%;
- override setelah konfirmasi risiko.

### 3. Scan QR & AI Payment Decision

AI mempertimbangkan:

1. saldo cukup;
2. sisa budget total;
3. sisa budget per wallet;
4. dana minimum;
5. promo dan cashback;
6. biaya;
7. merchant dan eligibility.

### 4. Versi presentasi investor

Buka `presentation.html`. Panel kanan menyediakan urutan walkthrough:

1. Problem & Value
2. Trust Gateway
3. Account & Budget Control
4. Scan QR & AI Decision
5. Daily Habit
6. Revenue & Moat

Gunakan `Alt + Arrow Right/Left` untuk berpindah cepat antartahap walkthrough.

## Urutan demo yang direkomendasikan

1. Buka `presentation.html` saat presentasi di laptop.
2. Klik **Account & Budget Control**.
3. Dari layar Akun & Wallet, pilih **Tambah Akun Baru**.
4. Hubungkan ShopeePay atau Mandiri.
5. Atur budget akun baru.
6. Kembali ke dashboard dan perlihatkan total saldo yang berubah.
7. Scan QR dan lihat AI memilih sumber dana berdasarkan saldo, budget, serta promo.
8. Lanjutkan hingga pembayaran berhasil dan saldo/budget diperbarui.

## Membuka di HP

Buka `index.html` melalui browser HP atau deploy folder ini ke Vercel, Netlify, atau GitHub Pages. Layout tampil full-screen dan tidak membutuhkan dependency eksternal.

## Catatan

Seluruh saldo, integrasi, promo, eligibility, QRIS, attribution, dan revenue event merupakan data simulasi prototype. Belum terhubung ke bank, e-wallet, aggregator, atau payment gateway aktual.
