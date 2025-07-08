
# 🎬 FlixRec – Sistem Rekomendasi Film dan Serial Berbasis MongoDB

Sistem ini adalah aplikasi web sederhana yang memberikan **rekomendasi film dan serial** berdasarkan preferensi pengguna, seperti genre, jenis tontonan, durasi, dan tahun rilis. Aplikasi ini menggunakan **MongoDB** sebagai database NoSQL untuk menyimpan data film dan melakukan query rekomendasi.

---

## 📌 Fitur Utama
- Form kuisioner interaktif untuk menentukan preferensi pengguna.
- Rekomendasi film/serial berdasarkan filter:
  - Genre favorit
  - Tipe tayangan (Movie / TV Show)
  - Tahun rilis (Latest / 2010s / 2000s / 1990s)
  - Durasi tontonan
- Tampilan dinamis dengan **HTML + CSS + JavaScript**
- Backend menggunakan **PHP native** dan **MongoDB driver**
- Data film real dari Netflix dataset (diimpor ke MongoDB)

---

## 🧰 Teknologi yang Digunakan

| Komponen     | Teknologi                  |
|--------------|-----------------------------|
| Frontend     | HTML, CSS, JavaScript       |
| Backend      | PHP Native                  |
| Database     | MongoDB (NoSQL)             |
| Dependency   | Composer + mongodb/mongodb  |
| Tools        | XAMPP / Apache              |

---

## 🗃️ Struktur Proyek

```
📁 film/
├── index.html              # Halaman utama (form pertanyaan)
├── rekomendasi.php         # Backend PHP: koneksi dan query MongoDB
├── uji_mongo.php           # (opsional) File uji koneksi MongoDB
├── composer.json           # File dependency Composer
├── vendor/                 # Folder autoload (hasil composer install)
└── README.md               # Dokumentasi proyek ini
```

---

## ⚙️ Cara Menjalankan Aplikasi

### 1. Clone atau Salin Project

```bash
https://github.com/MdnXD/FlixRec
```

Atau salin ke folder `htdocs` jika pakai XAMPP:
```
C:\xampp\htdocs\film\
```

---

### 2. Jalankan Composer Install

```bash
cd film
composer install
```

> Pastikan Composer sudah terinstal dan MongoDB driver aktif di `php.ini`:
> Tambahkan:
> `extension=php_mongodb.dll`

---

### 3. Jalankan XAMPP (Apache) dan MongoDB
- Buka XAMPP Control Panel → Start Apache
- Pastikan MongoDB sudah aktif dan dataset `film` sudah dimasukkan ke `rekomendasi_film.film`

---

### 4. Akses Aplikasi via Browser

```
http://localhost/film/index.html
```

Isi form, klik “Get Recommendations”, dan lihat hasil film yang cocok dengan preferensimu.

---

## 📸 Screenshot

| Halaman Kuisioner | Hasil Rekomendasi |
|-------------------|-------------------|
| ![Form](screenshots/form.png) | ![Rekomendasi](screenshots/result.png) |

---

## 🧪 Contoh Data MongoDB

Contoh dokumen di koleksi `film`:
```json
{
  "title": "Stranger Things",
  "type": "TV Show",
  "listed_in": ["Sci-Fi", "Thriller"],
  "release_year": 2016,
  "duration": 50,
  "rating": "TV-14",
  "description": "...",
  "image": "..."
}
```

---

## ✍️ Tim Pengembang

| Nama           | NIM        |
|----------------|------------|
| Nama 1         | 1234567890 |
| Nama 2         | 0987654321 |

---

## 📚 Referensi
- https://www.mongodb.com/docs/
- https://pecl.php.net/package/mongodb
- https://www.php.net/manual/en/set.mongodb.php
- Netflix Dataset (Kaggle or other source)

---

## 📦 Lisensi
Proyek ini dibuat untuk keperluan pembelajaran dan tugas akhir mata kuliah **NoSQL**.
