# Modul Odoo: Ruangan dan Pemesanan

## Deskripsi

Modul ini dirancang untuk memudahkan pengelolaan master ruangan dan pemesanan ruangan dalam sistem Odoo. Dengan modul ini, pengguna dapat membuat dan mengelola daftar ruangan, serta melakukan pemesanan ruangan secara efisien.

## Fitur Utama

1. **Master Ruangan**
   - Menyimpan informasi tentang ruangan yang tersedia.
   - Informasi mencakup nama, tipe, lokasi, foto, kapasitas, dan keterangan.

2. **Pemesanan Ruangan**
   - Mengelola pemesanan ruangan dengan detail seperti nomor pemesanan, nama pemesan, tanggal, dan status pemesanan.
   - Validasi untuk mencegah pemesanan yang sama pada waktu yang sama.

3. **Tampilan**
   - Tampilan grid/list untuk melihat master ruangan dan pemesanan.
   - Tombol untuk mengubah status pemesanan.

4. **Validasi**
   - Memastikan nama ruangan dan pemesanan tidak duplikat.
   - Memastikan tidak ada pemesanan yang bertabrakan pada tanggal yang sama.

## Instalasi

### Prasyarat
- Odoo 14 atau versi lebih baru.
- Akses ke server Odoo.
- Keterampilan dasar dalam pengembangan Odoo (Python dan XML).

### Langkah-langkah Instalasi

1. **Unduh atau Clone Modul**
   - Download atau clone repositori ini ke dalam direktori `addons` Odoo Anda.
   - Struktur folder harus menjadi seperti ini:
     ```
     odoo/addons/ruangan_pemesanan/
     ```

2. **Buat Struktur Folder**
   - Pastikan struktur folder di dalam `ruangan_pemesanan` adalah sebagai berikut:
     ```
     ruangan_pemesanan/
     ├── __init__.py
     ├── __manifest__.py
     ├── models/
     │   ├── __init__.py
     │   ├── master_ruangan.py
     │   └── pemesanan_ruangan.py
     └── views/
         ├── master_ruangan_views.xml
         └── pemesanan_ruangan_views.xml
     ```

3. **Restart Odoo**
   - Restart Odoo untuk memuat modul baru.

4. **Instal Modul**
   - Masuk ke Odoo sebagai administrator.
   - Pergi ke **Apps**.
   - Aktifkan mode debug jika belum.
   - Klik **Update Apps List**.
   - Cari "Ruangan dan Pemesanan" dan klik **Install**.

## Penggunaan

### Menambahkan Master Ruangan
1. Masuk ke menu **Master Ruangan**.
2. Klik tombol **Create**.
3. Isi semua field yang diperlukan dan klik **Save**.

### Melihat dan Mengelola Master Ruangan
- Anda dapat melihat daftar ruangan dalam tampilan grid.
- Klik nama ruangan untuk mengedit, lalu simpan perubahan.

### Menambahkan Pemesanan Ruangan
1. Masuk ke menu **Pemesanan Ruangan**.
2. Klik tombol **Create**.
3. Isi semua field yang diperlukan dan klik **Save**.

### Mengelola Pemesanan Ruangan
- Untuk mengupdate status pemesanan, gunakan tombol **Proses Pemesanan** untuk mengubah ke status **On Going**, dan **Done** untuk menyelesaikan pemesanan.

## Validasi

- Modul ini mencegah pemesanan ruangan yang sama pada tanggal yang sama.
- Nama pemesanan tidak boleh sama. 
- Nama ruangan juga harus unik.
