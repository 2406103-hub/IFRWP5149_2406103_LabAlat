| Sumber | Hubungan | Tujuan |
|---|---|---|
| Mahasiswa | Association | SIA-UC01 Lihat Jadwal Kuliah |
| Admin Akademik | Association | SIA-UC02 Kelola Jadwal Kuliah |
| Mahasiswa | Association | SIA-UC03 Ajukan KRS |
| SIA-UC03 Ajukan KRS | `<<include>>` (tetap dari Pertemuan 3) | SIA-UC04 Validasi KRS |
| Mahasiswa | Association | SIA-UC05 Unduh Bukti Pengajuan KRS |
| SIA-UC05 Unduh Bukti Pengajuan KRS | `<<extend>>` (tetap dari Pertemuan 3) | SIA-UC03 Ajukan KRS |
| Dosen Wali | Association | SIA-UC06 Proses Keputusan KRS |
| Civitas Akademika | Association | SIA-UC07 Lihat Kalender Akademik |
| Mahasiswa | Generalization → | Civitas Akademika |
| Dosen | Generalization → | Civitas Akademika |
| Dosen | Association | SIA-UC08 Input Nilai Mata Kuliah |
| Mahasiswa | Association | SIA-UC09 Lihat KHS |
| Admin Akademik | Association | SIA-UC10 Kelola Data Mahasiswa |
| SIA-UC11 Tambah Data Mahasiswa | Generalization → | SIA-UC10 Kelola Data Mahasiswa |
| SIA-UC12 Ubah Data Mahasiswa | Generalization → | SIA-UC10 Kelola Data Mahasiswa |
| SIA-UC13 Hapus Data Mahasiswa | Generalization → | SIA-UC10 Kelola Data Mahasiswa |
| SIA-CO01 (collaboration) | Realization → | SIA-UC08 Input Nilai Mata Kuliah |
| SIA-CO02 (collaboration) | Realization → | SIA-UC09 Lihat KHS |