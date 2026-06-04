# 🏆 JUARA OSN — Latihan IPS SD

Aplikasi web latihan soal **Olimpiade Sains Nasional (OSN) bidang IPS tingkat Sekolah Dasar**. Dibuat untuk membantu siswa berlatih secara terstruktur dengan pembahasan tiap soal dan pemantauan perkembangan hasil belajar.

🔗 **Demo langsung:** _aktifkan GitHub Pages (lihat di bawah), lalu tautannya muncul di sini._

## ✨ Fitur

- **Sesi 30 soal acak** dari bank soal tiap kali berlatih, jadi latihan tidak monoton.
- **Pembahasan langsung** muncul setiap selesai menjawab — fokus memahami konsep, bukan menghafal kunci.
- **Rapor akhir per sesi**: skor, jumlah benar, penguasaan per bidang, dan perbaikan jawaban lengkap.
- **Riwayat & grafik perkembangan** tersimpan otomatis di perangkat (localStorage), sehingga orang tua/guru dapat memantau kemajuan anak dari waktu ke waktu.
- **Tampilan rapi** untuk soal pernyataan bernomor, soal dua-pernyataan (A/B), dan soal menjodohkan.
- Materi mencakup **Sejarah, Geografi, Ekonomi, dan Sosial-Budaya Indonesia**.

## 🚀 Cara Menjalankan

Aplikasi ini adalah satu berkas HTML mandiri — tidak butuh server, database, atau proses build.

**Lokal:** cukup buka `index.html` di browser (Chrome, Edge, Firefox, Safari).

**Online (GitHub Pages):**
1. Buka repo ini → **Settings** → **Pages**.
2. Pada *Source*, pilih branch `main` dan folder `/ (root)`, lalu **Save**.
3. Tunggu beberapa menit; situs akan tersedia di `https://<username>.github.io/<nama-repo>/`.

## 💾 Penyimpanan Data

Rapor dan riwayat latihan disimpan di **localStorage browser**, di perangkat masing-masing. Artinya:

- Data **tidak dikirim ke server mana pun** — sepenuhnya privat dan luring.
- Data terikat pada **browser + perangkat** yang dipakai. Membuka di perangkat/browser lain akan dimulai dari kosong.
- Membersihkan data browser atau menekan **"Hapus semua riwayat"** akan menghapus rapor.

## 🧱 Struktur Berkas

```
.
├── index.html      # Seluruh aplikasi (HTML + CSS + JS + bank soal)
├── README.md
└── LICENSE
```

## 📚 Bank Soal

Berisi 50 soal pilihan ganda yang sudah dikurasi dan dideduplikasi, masing-masing dengan kunci jawaban dan pembahasan. Untuk menambah/menyunting soal, ubah array `BANK` di dalam `index.html` (cari `const BANK =`). Format tiap soal:

```js
{
  id: 99,
  kategori: "Sejarah & Tokoh",
  soal: "Teks soal...",
  opsi: ["Pilihan A", "Pilihan B", "Pilihan C", "Pilihan D"],
  jawaban: 0,            // indeks jawaban benar (0=A, 1=B, 2=C, 3=D)
  pembahasan: "Penjelasan jawaban..."
}
```

## 🤝 Kontribusi

Saran soal baru, koreksi pembahasan, dan perbaikan tampilan sangat diterima melalui Issue atau Pull Request.

## 📄 Lisensi

Dirilis di bawah lisensi MIT. Lihat berkas [LICENSE](LICENSE).
