# Pertemuan 12 File I/O dan Error Handling

Nama: Amandita Pebriana Putri  
NIM: 2225250134  
Kelas: 3A Pendidikan Matematika  

## Tujuan
Membaca, memvalidasi, mengolah, dan menulis data file secara aman menggunakan Python, serta menangani error dasar seperti FileNotFoundError dan ValueError tanpa menghentikan seluruh proses.

## Format File Input
NIM, nilai (dipisahkan oleh tanda koma per baris, contoh: A001,85)

## Cara Menjalankan
python3 tugas/rekap_nilai_file.py

## Error yang Ditangani
- FileNotFoundError: Ditangani ketika file input belum tersedia atau salah jalur direktori.
- ValueError: Ditangani per baris ketika data nilai mengandung teks atau format yang tidak valid agar baris lain tetap dapat diproses.

## Test Case
| Kasus Pengujian | Kondisi | Hasil Utama yang Diharapkan | Status |
| :--- | :--- | :--- | :---: |
| Normal | Semua baris valid | Semua record diproses dan ringkasan rekapitulasi benar | Sesuai |
| File hilang | nilai.txt tidak tersedia | Menampilkan pesan file tidak ditemukan; program tidak crash | Sesuai |
| Nilai invalid | A004,abc | Baris invalid dilewati/dilaporkan; record lain tetap diproses | Sesuai |
| Baris kosong | Ada baris kosong | Baris kosong berhasil dilewati secara otomatis | Sesuai |
| Batas lulus | Nilai 60 | Dihitung ke dalam kategori kelulusan dengan benar | Sesuai |

## Refleksi
Dalam praktik file I/O dan error handling ini, penanganan exception secara spesifik sangat penting agar kesalahan kecil pada satu baris data (seperti format huruf pada kolom nilai) tidak merusak keseluruhan program. Penggunaan blok try-except di dalam iterasi baris memungkinkan data yang valid tetap berhasil direkap secara akurat.