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


|         Elemen         |                            Deskripsi                                                  |
|------------------------|----------------------------------------------------------------                      -|
| Sumber kebutuhan       | SIA-R04 (bagian dari SIA-R03)                                                         |
| Tujuan                 | Memastikan data lengkap, prasyarat terpenuhi, dan tidak bentrok.|
| Aktor utama            | Sistem Informasi Akademik (dipanggil oleh SIA-UC03)             |
| Aktor pendukung        | Mahasiswa sebagai pengaju melalui SIA-UC03                      |
| Pemicu                 | SIA-UC03 mencapai tahap validasi pengajuan.                     |
| Prasyarat              | Mahasiswa terautentikasi dan telah memilih matkul di KRS.       |
| Alur utama             | Sistem menerima data, memeriksa kelengkapan, prasyarat, dan bentrok, lalu kirim hasil.|
| Alur alternatif        | Data tak lengkap, prasyarat tak sesuai, atau jadwal bentrok, pengajuan batal.|
| Pascakondisi berhasil  | Validasi lolos, SIA-UC03 dapat menyimpan pengajuan.             |
| Pascakondisi gagal     | Validasi gagal, SIA-UC03 tidak menyimpan pengajuan.             |
| Aturan bisnis/asumsi   | Validasi wajib dijalankan; batas SKS dan biaya di luar cakupan. |