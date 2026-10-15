<!-- tabel ajukan KRS-->
|         Elemen         |                            Deskripsi                                                        |
|------------------------|---------------------------------------------------------------------------------------------|
| Sumber kebutuhan       | SIA-R03, SIA-R04, SIA-R05                                                                   |
| Tujuan                 | Mengirim pengajuan KRS yang lolos validasi.                                                 |
| Aktor utama            | Mahasiswa                                                                                   |
| Aktor pendukung        | Sistem Informasi Akademik                                                                   |
| Pemicu                 | Mahasiswa memilih menu KRS.                                                                 |
| Prasyarat              | Mahasiswa terautentikasi.                                                                   |
| Alur utama             | Mahasiswa mengajukan matkul, sistem memvalidasi, menyimpan data, lalu tampilkan konfirmasi. |
| Alur alternatif        | Validasi gagal, pengajuan batal tersimpan.                                                  |
| Pascakondisi berhasil  | KRS tersimpan berstatus Menunggu persetujuan.                                               |
| Pascakondisi gagal     | Pengajuan tidak tersimpan.                                                                  |
| Aturan bisnis/asumsi   | KRS tersimpan belum disetujui; unduh bukti opsional.                                        |

<!-- tabel Validasi KRS-->
|         Elemen         |                            Deskripsi                                                  |
|------------------------|---------------------------------------------------------------------------------------|
| Sumber kebutuhan       | SIA-R04 (bagian dari SIA-R03)                                                         |
| Tujuan                 | Memastikan data lengkap, prasyarat terpenuhi, dan tidak bentrok.                      |
| Aktor utama            | Sistem Informasi Akademik (dipanggil oleh SIA-UC03)                                   |
| Aktor pendukung        | Mahasiswa sebagai pengaju melalui SIA-UC03                                            |
| Pemicu                 | SIA-UC03 mencapai tahap validasi pengajuan.                                           |
| Prasyarat              | Mahasiswa terautentikasi dan telah memilih matkul di KRS.                             |
| Alur utama             | Sistem menerima data, memeriksa kelengkapan, prasyarat, dan bentrok, lalu kirim hasil.|
| Alur alternatif        | Data tak lengkap, prasyarat tak sesuai, atau jadwal bentrok, pengajuan batal.         |
| Pascakondisi berhasil  | Validasi lolos, SIA-UC03 dapat menyimpan pengajuan.                                   |
| Pascakondisi gagal     | Validasi gagal, SIA-UC03 tidak menyimpan pengajuan.                                   |
| Aturan bisnis/asumsi   | Validasi wajib dijalankan; batas SKS dan biaya di luar cakupan.                       |

<!-- tabel Unduh bukti pengajuan KRS-->
|         Elemen         |                                       Deskripsi                                       |
|------------------------|---------------------------------------------------------------------------------------|
| Sumber kebutuhan       | SIA-R05                                                                               |
| Tujuan                 | Mendapatkan berkas bukti pengajuan KRS yang tersimpan.                                |
| Aktor utama            | Mahasiswa                                                                             |
| Aktor pendukung        | Sistem Informasi Akademik                                                             |
| Pemicu                 | Mahasiswa memilih tombol unduh bukti.                                                 |
| Prasyarat              | KRS telah tersimpan dan konfirmasi pengajuan muncul.                                  |
| Alur utama             | Mahasiswa memilih unduh, sistem menyiapkan berkas dan menyediakan file untuk diunduh.|
| Alur alternatif        | Jika bukti gagal disiapkan, beri pesan error; jika opsi tak dipilih, KRS tetap sukses.|
| Pascakondisi berhasil  | File bukti pengajuan siap diunduh.                                                    |
| Pascakondisi gagal     | Bukti gagal diunduh, namun pengajuan KRS tetap tersimpan.                             |
| Aturan bisnis/asumsi   | Merupakan ekstensi opsional dari SIA-UC03 saat opsi unduh dipilih.                    |

<!-- tabel Proses keputusan KRS--> 
|         Elemen         |                                       Deskripsi                                       |
|------------------------|---------------------------------------------------------------------------------------|
| Sumber kebutuhan       | SIA-R06                                                                               |
| Tujuan                 | Mencatat keputusan persetujuan/penolakan KRS dosen wali beserta catatannya.           |
| Aktor utama            | Dosen wali                                                                            |
| Aktor pendukung        | Sistem Informasi Akademik                                                             |
| Pemicu                 | Dosen wali membuka pengajuan KRS yang menggantung.                                    |
| Prasyarat              | Dosen wali sudah login dan ada pengajuan KRS berstatus Menunggu.                      |
| Alur utama             | Dosen wali meninjau detail, memilih keputusan, mengisi catatan, lalu kirim hasil.     |
| Alur alternatif        | Jika data/keputusan kosong, minta dilengkapi; jika tak ada pengajuan, tampilkan error.|
| Pascakondisi berhasil  | Keputusan dan catatan tersimpan.                                                      |
| Pascakondisi gagal     | Keputusan tidak berubah dan pengajuan belum diproses.                                 |
| Aturan bisnis/asumsi   | Hanya dosen wali terautentikasi yang bisa memproses keputusan.                        |