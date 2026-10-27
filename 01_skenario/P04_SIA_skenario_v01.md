# Skenario Sistem Informasi Akademik

Skenario ini merupakan kasus fiktif untuk praktikum. Mahasiswa dan dosen merupakan bagian dari Civitas Akademika yang dapat melihat kalender akademik. Dosen dapat menginput nilai mata kuliah yang diampunya setelah masa perkuliahan berakhir. Mahasiswa dapat melihat Kartu Hasil Studi (KHS) untuk semester yang nilainya sudah dipublikasikan.

Admin Akademik bertugas mengelola data mahasiswa, meliputi menambah data mahasiswa baru, mengubah data mahasiswa, dan menghapus data mahasiswa yang tidak memiliki data akademik aktif.

Dua use case utama, yaitu Input Nilai Mata Kuliah dan Lihat KHS, direalisasikan melalui collaboration yang bersesuaian.

# aktor
| Aktor | Kedudukan | Tujuan terhadap sistem |
|---|---|---|
| Civitas Akademika | Aktor umum, baru pada Pertemuan 4 | Melihat kalender akademik. |
| Mahasiswa | Aktor khusus dari Civitas Akademika; aktor lama | Melihat jadwal kuliah, mengajukan KRS, mengunduh bukti pengajuan KRS, dan melihat KHS. |
| Dosen | Aktor khusus dari Civitas Akademika, baru pada Pertemuan 4 | Melihat kalender akademik dan menginput nilai mata kuliah yang diampunya. |
| Admin Akademik | Aktor lama | Mengelola jadwal kuliah dan data mahasiswa. |
| Dosen Wali | Aktor lama | Memproses keputusan pengajuan KRS. |

| Aktor Khusus | Hubungan | Aktor Umum |
|---|---|---|
| Mahasiswa | Generalization → | Civitas Akademika |
| Dosen | Generalization → | Civitas Akademika |

# use case
| ID | Nama Use Case | Aktor Terkait | Sumber Kebutuhan | Keterangan |
|---|---|---|---|---|
| SIA-UC01 | Lihat Jadwal Kuliah | Mahasiswa | SIA-R01 | Tetap dari Pertemuan 2 |
| SIA-UC02 | Kelola Jadwal Kuliah | Admin Akademik | SIA-R02 | Tetap dari Pertemuan 2 |
| SIA-UC03 | Ajukan KRS | Mahasiswa | SIA-R03 | Tetap dari Pertemuan 3 |
| SIA-UC04 | Validasi KRS | — (perilaku sistem) | SIA-R04 | Tetap dari Pertemuan 3 |
| SIA-UC05 | Unduh Bukti Pengajuan KRS | Mahasiswa | SIA-R05 | Tetap dari Pertemuan 3 |
| SIA-UC06 | Proses Keputusan KRS | Dosen Wali | SIA-R06 | Tetap dari Pertemuan 3 |
| SIA-UC07 | Lihat Kalender Akademik | Civitas Akademika | SIA-R07 | Baru pada Pertemuan 4 |
| SIA-UC08 | Input Nilai Mata Kuliah | Dosen | SIA-R08 | Baru pada Pertemuan 4 |
| SIA-UC09 | Lihat KHS | Mahasiswa | SIA-R09 | Baru pada Pertemuan 4 |
| SIA-UC10 | Kelola Data Mahasiswa | Admin Akademik | SIA-R10 | Use case umum, baru pada Pertemuan 4 |
| SIA-UC11 | Tambah Data Mahasiswa | Admin Akademik | SIA-R11 | Use case khusus, baru pada Pertemuan 4 |
| SIA-UC12 | Ubah Data Mahasiswa | Admin Akademik | SIA-R11 | Use case khusus, baru pada Pertemuan 4 |
| SIA-UC13 | Hapus Data Mahasiswa | Admin Akademik | SIA-R11 | Use case khusus, baru pada Pertemuan 4 |

# include 
| Use Case Utama | Hubungan | Use Case yang Disertakan | Alasan |
|---|---|---|---|
| SIA-UC03 Ajukan KRS | `<<include>>` | SIA-UC04 Validasi KRS | Setiap pengajuan KRS harus melalui proses validasi. |

# extend
| Use Case Tambahan | Hubungan | Use Case Utama | Kondisi |
|---|---|---|---|
| SIA-UC05 Unduh Bukti Pengajuan KRS | `<<extend>>` | SIA-UC03 Ajukan KRS | Mahasiswa memilih untuk mengunduh bukti pengajuan. |