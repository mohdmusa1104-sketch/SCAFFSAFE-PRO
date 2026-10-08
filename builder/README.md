# ScaffSafe Pro — 3D Builder (Fasa 1)

Modul berasingan; aplikasi asal `../index.html` tidak diubah.

## Buka pada komputer

Python 3 diperlukan. Dari akar repositori:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Buka `http://127.0.0.1:8000/builder/` dalam Chrome, Edge atau Firefox dengan WebGL aktif. Gunakan HTTP, bukan membuka fail HTML terus. Pustaka Three.js 0.180.0 dan OrbitControls disimpan dalam `vendor/`; tiada npm/build atau internet diperlukan untuk menjalankan modul. Lesen MIT Three.js disertakan.

## Ujian manual

- Preset: 3 × 3 × 4 m, jarak bay 1.5 m, lift maksimum 2 m.
- Tinggi ialah tinggi struktur/rail atas. Platform tertinggi pada tinggi − 1 m. Geometri tube menggunakan diameter luar visual 48.3 mm; ketebalan dinding tidak dimodelkan.
- Bay dibahagi sama rata menggunakan `ceil(dimensi / jarak bay)`; jarak sebenar tidak melebihi input dan dipaparkan dalam ringkasan. Lift sokongan dibahagi daripada tinggi; aras platform tambahan ditunjukkan berasingan.
- Tukar panjang kepada 5, lebar 2, tinggi 6, bay 1.4 dan lift 2.5. Tekan Jana model: grid menjadi 4 × 2 bay dan platform pada 5 m.
- Cuba semua 11 pilihan Show/Hide, empat pandangan kamera, butang zoom, seretan putaran dan mod pan. Reset mengembalikan preset.
- Input di luar julat ditolak; model berlebihan dilindungi had saiz.
- Buka aplikasi asal pada `/` untuk memastikan ciri asal masih tersedia.

## Had Fasa 1

Visualisasi susun atur tube-and-coupler, bukan ringlock/cuplock. Coupler ialah representasi blok ringkas pada titik sambungan, bukan model fabrikasi. Rail, platform dan bracing dijana sebagai konsep geometri; ukuran/penempatan belum disahkan mengikut edisi BS1139 tertentu. Tiada analisis beban, tanah, ties, kestabilan, reka bentuk akses atau kelulusan kejuruteraan. Tiada simpanan projek atau eksport dalam fasa ini.

## Pengesahan pembangunan

Ujian Chromium automatik dijalankan untuk preset, semua komponen dan Show/Hide, Front/Side/Top/Isometric, zoom/pan/rotate, perubahan dimensi, reset, lebar paparan mudah alih dan pemaparan aplikasi asal. Tiada ralat JavaScript. Fail aplikasi asal mempunyai SHA-256 yang sama sebelum dan selepas pembangunan.
