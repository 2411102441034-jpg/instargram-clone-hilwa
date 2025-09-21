# Tugas: Halaman Profil Instagram dgn Bootstrap Grid

Proyek ini adalah implementasi halaman profil Instagram yg responsif menggunakan sistem grid Bootstrap 5. Tujuannya adalah untuk menampilkan tata letak yg bersih dan adaptif di berbagai ukuran layar, mulai dri mobile hingga desktop.

---

### Fitur-fitur Utama

- **Struktur Halaman**: Dibangun dgn struktur yg jelas, memisahkan konten menjadi `Header Profil`, `Bio`, `Feed Foto`, dan `Footer`.
- **Feed Foto**: Menampilkan minimal 12 foto dlm format grid yg responsif, meniru tampilan galeri Instagram.
- **Responsivitas**: Halaman ini didesain dgn pendekatan _mobile-first_, memastikan tata letak g optimal di setiap perangkat.
- **Tombol Interaksi**: Tombol "Follow" dan "Edit Profile" disesuaikan secara dinamis, mengubah posisi dan ukurannya tergantung pada _breakpoint_ layar.
- **Penggunaan Bootstrap**: Semua tata letak dan _styling_ utama (seperti `card`, `btn`, `container`, `row`, `col`) menggunakan _utility classes_ Bootstrap.

---

### Jawaban Pertanyaan README

#### 1. Mengapa memilih konfigurasi `col-` tertentu untuk tiap _breakpoint_?

Saya memilih konfigurasi `col-` yg berbeda untuk setiap ukuran layar agar tata letak halaman tetap rapi dan mudah dilihat, tidak peduli perangkat apa yg digunakan.

- **Mobile (≤576px)**: Menggunakan `col-12`. Di layar kecil, satu postingan memenuhi seluruh lebar layar. Ini membuat gambar terlihat besar dan jelas, jadi tidak perlu repot-repot _zoom_ atau kesulitan melihat detail.
- **Tablet (>768px)**: Menggunakan `col-md-4`. Layar tablet lebih lebar, jadi kita bisa menampilkan tiga postingan dlm satu baris. Ini membuat halaman terlihat lebih efisien dan padat.
- **Desktop (≥992px)**: Menggunakan `col-lg-3`. Di layar komputer yg sangat lebar, kita bisa menampilkan empat postingan dlm satu baris. Ini memungkinkan  melihat lebih banyak konten tanpa harus banyak _scroll_.

Pendekatan ini bertujuan untuk memberikan pengalaman terbaik di semua perangkat.

---

#### 2. Bagaimana kamu memastikan tombol Follow/Edit Profile tetap mudah dijangkau di mobile? Jelaskan pendekatannya.

Untuk memastikan tombol **Follow** dan **Edit Profile** mudah dijangkau di mobile, saya menggunakan utilitas responsif Bootstrap. Di layar mobile, tombol-tombol ini ditempatkan di bawah nama . Pendekatan ini bertujuan agar tombol lebih menonjol dan mudah diklik oleh jempol pengguna.

Kemudian, di layar desktop, tombol-tombol ini diletakkan di samping nama karena tersedia ruang yg cukup. Saya menggunakan kelas `d-none d-md-block` (sembunyikan di mobile, tampilkan di desktop) dan `d-block d-md-none` (tampilkan di mobile, sembunyikan di desktop) untuk mengatur visibilitas tombol secara otomatis.

---

#### 3. Jika postingan bertambah jadi 50, apa potensi masalah dan bagaimana solusi gridmu mengatasinya?

Jika postingan bertambah dari 12 menjadi 50, potensi masalah utamanya adalah halaman menjadi sangat panjang dan memuatnya butuh waktu lebih lama, yg bisa membuat pengguna lelah.

Solusi dari sistem grid ini adalah:

1.  **Tata Letak Otomatis**: Dengan menggunakan kelas `col-` yg sdh ditentukan, grid akan secara otomatis menyesuaikan tata letak untuk 50 postingan. Setiap gambar bru akan diletakkan di baris berikutnya, mengikuti aturan jumlah kolom yg sdh kita tentukan. jadi tidak perlu mengubah kode HTML atau CSS untuk menambahkan postingan bru.
2.  **Solusi Jangka Panjang**: Untuk mengatasi masalah performa dan halaman yg terlalu panjang, bisa menambahkan fitur **lazy loading** (memuat gambar hanya saat dibutuhkan) atau **pagination** (membagi postingan menjadi beberapa halaman).
