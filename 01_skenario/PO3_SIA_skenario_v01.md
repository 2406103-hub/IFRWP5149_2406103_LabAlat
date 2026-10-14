<!-- skenario tugas-->
Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap pengajuan menjalankan validasi KRS yang memeriksa kelengkapan, prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil, sistem menyimpan pengajuan berstatus menunggu persetujuan dosen wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS dan memberikan catatan keputusan.

<!-- tabel kebutuhan-->
|  ID   |                                         Kebutuhan                                          |
|-------|--------------------------------------------------------------------------------------------|
|SIA-R01|                           Mahasiswa dapat melihat jadwal kuliah.                           |
|SIA-R02|                       Admin akademik dapat mengelola jadwal kuliah.                        |
|SIA-R03|                              Mahasiswa dapat mengajukan KRS.                               |
|SIA-R04|                Sistem memvalidasi KRS sebagai bagian dari proses pengajuan.                |
|SIA-R05|         Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan.         |
|SIA-R06|Dosen wali dapat memproses persetujuan atau penolakan KRS dan memberikan catatan keputusan. |

<!-- Batas sistem dan aturan -->
Batas dan asumsi:
•	Pengguna telah terautentikasi dan memiliki hak akses sesuai perannya.
•	Data mata kuliah, prasyarat, dan jadwal tersedia.
•	Validasi yang gagal menyebabkan pengajuan belum berhasil tersimpan.
•	Unduh bukti bukan syarat keberhasilan pengajuan KRS.
•	KRS yang tersimpan berstatus menunggu persetujuan dosen wali dan belum berarti disetujui.
•	Pembayaran, pengisian nilai, batas SKS, serta implementasi basis data berada di luar cakupan tugas.

<!-- identifikasi  aktor-->
|    Aktor    |                                 Tujuan                                               |
|-------------|--------------------------------------------------------------------------------------|
|  Mahasiswa  |Melihat jadwal kuliah, mengajukan KRS, dan mengunduh bukti pengajuan jika diperlukan. |
|Adminakademik|                               Mengelola jadwal kuliah.                               |
|  Dosenwali  |           Menyetujui atau menolak KRS serta memberikan catatan keputusan.            |

<!-- katalog usecase -->
|   ID   |     Nama use case         |                   Aktor terkait                           |Sumber kebutuhan|
|--------|---------------------------|-----------------------------------------------------------|----------------|
|SIA-UC01|  Lihat jadwal kuliah      |                    Mahasiswa                              |    SIA-R01     |
|SIA-UC02|  Kelola jadwal kuliah     |                  Adminakademik                            |    SIA-R02     |
|SIA-UC03|      Ajukan KRS           |                    Mahasiswa                              |    SIA-R03     |
|SIA-UC04|     Validasi KRS          |Bagian dari SIA-UC03, tidak dimulai aktor secara terpisah  |    SIA-R04     |
|SIA-UC05|Unduh bukti pengajuan KRS  |                    Mahasiswa                              |    SIA-R05     |
|SIA-UC06|  Proses keputusanKRS      |                    Dosenwali                              |    SIA-R06     |
 
<!-- relasi include -->
«include» SIA-UC04. Alasan: validasi kelengkapan data, prasyarat mata kuliah, dan benturan jadwal selalu menjadi bagian dari setiap pengajuan KRS.

<!-- relasi extend -->
«extend» SIA-UC03. Use case dasar: Ajukan KRS. Kondisi: [mahasiswa memilih unduh]. Extension point: Bukti pengajuan tersedia. Alasan: pengajuan tetap berhasil tersimpan walaupun mahasiswa tidak mengunduh bukti.