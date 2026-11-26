# Arrow Beat

Game ritme 4 lajur yang berjalan di browser, satu file HTML tanpa library eksternal. Mainkan lagu bawaan atau tambahkan lagumu sendiri dari file audio atau video, lalu game membuat chart-nya otomatis.

## Fitur

- **Chart otomatis** dari lagu: deteksi tempo (BPM), beat, dan melodi. Tempo lagu memengaruhi kerapatan dan kecepatan note.
- **Hold note** mengikuti nada panjang lagu, **tap note** untuk nada singkat.
- **7 tingkat kesulitan:** Santai, Mudah, Normal, Sulit, Ahli, Gila, Neraka.
- **Obstacle:** ranjau (sekali kena gagal), racun 3 tingkat (jangan ditekan, HP berkurang), panah emas (wajib ditekan), panah hantu (memudar).
- **Bar HP**, hitung mundur, layar gagal dengan animasi dan suara.
- **Penilaian:** Perfect, Good, Bad, Early, Late, Miss, dengan animasi dan getaran.
- **Library Lagu** yang tersimpan permanen di browser (IndexedDB), lengkap dengan Edit konfigurasi per lagu, Delete, dan Reset to Default.
- **Kontrol dua jempol** untuk HP, toleransi lepas hold, dan kalibrasi latensi.
- **Auto Play** (bot) yang bermain sempurna.

## Cara main

Ketuk panah saat menyentuh garis. Tahan untuk note panjang. Jangan sentuh ranjau (X) dan racun (!). Keyboard: panah kiri/bawah/atas/kanan atau D F J K.

Jalankan **Kalibrasi** di menu "Kontrol dan latensi" sekali sebelum bermain untuk menyesuaikan delay audio perangkatmu.

## Menjalankan

Buka `index.html` di browser. Untuk fitur penyimpanan Library yang paling andal, buka lewat `https://` (misalnya GitHub Pages) atau server lokal, bukan lewat `file://`.

### Pasang di GitHub Pages

1. Buat repository baru di GitHub (misalnya `arrow-beat`).
2. Unggah semua file ini ke root repo (tombol **Add file > Upload files**): `index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`, dan `README.md`.
3. Buka **Settings > Pages**.
4. Di **Build and deployment**, pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu **Save**.
5. Tunggu satu sampai dua menit. Gamenya tersedia di `https://NAMA-GITHUB-KAMU.github.io/arrow-beat/`.

## Instal sebagai aplikasi (PWA)

Setelah GitHub Pages aktif, buka alamat game **sekali saat online**:

- **Android (Chrome):** menu ⋮ > **Instal aplikasi** atau **Tambahkan ke layar utama**.
- **iPhone (Safari):** tombol Bagikan > **Tambahkan ke Layar Utama**.

Setelah itu game bisa dibuka dan dimainkan tanpa internet. Library Lagu tetap ada karena tersimpan di browser.

### Memperbarui game

Setiap kali kamu mengunggah `index.html` baru, ubah juga angka versi di `sw.js` (misalnya `arrow-beat-v1` menjadi `arrow-beat-v2`). Tanpa itu, HP bisa tetap memakai versi lama. Setelah itu tutup aplikasi sepenuhnya lalu buka lagi (kadang perlu dua kali).

## Catatan teknis

- Lagu yang kamu tambahkan **tidak diunggah ke server mana pun**. Semuanya disimpan di browser perangkatmu (IndexedDB). Menghapus data browser akan menghapus Library.
- Batas ukuran file lagu: 150 MB.
- Deteksi melodi memakai campuran seluruh lagu, bukan vokal terpisah, jadi akurasinya bervariasi.
- Gunakan lagu yang kamu punya haknya. Jangan mengunggah lagu berhak cipta ke repository publik.

## Lisensi

Belum ditentukan. Tambahkan file `LICENSE` sesuai pilihanmu (misalnya MIT) sebelum membagikan kodenya.
