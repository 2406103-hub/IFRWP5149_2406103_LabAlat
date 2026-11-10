

| No | Temuan | Perbaikan yang Diperlukan | Alasan |
| --- | --- | --- | --- |
| 1 | *Swimlane* dan Aktor | Memastikan setiap *action* ditempatkan pada *swimlane* aktor yang tepat (Mahasiswa, Sistem, Petugas Laboratorium, Kepala Laboratorium) sesuai tabel skenario.

 | Agar tanggung jawab setiap kegiatan terbaca jelas dari partisi *swimlane* masing-masing aktor.

 |
| 2 | *Initial* & *Final Node* | Memastikan setiap *activity diagram* memiliki tepat satu *titik awal* (*initial node*) dan minimal satu *titik akhir* (*activity final node*) tanpa alur yang terputus.

 | Karena aturan dasar UML 2.5.1 mewajibkan alur dimulai dari satu titik awal dan bermuara ke titik akhir yang jelas.

 |
| 3 | *Decision* & *Guard* | Menambahkan *guard* (syarat dalam kurung siku seperti `[tersedia]` atau `[tidak tersedia]`) pada setiap alur keluar dari titik percabangan (*decision*).

 | Agar setiap jalur alternatif memiliki kondisi yang valid, saling lepas, dan bersama-sama menutup semua kemungkinan.

 |
| 4 | *Merge* dan Percabangan | Mengembalikan setiap cabang *decision* ke alur utama melalui titik penggabungan (*merge*) atau mengakhirinya langsung pada *activity final node*.

 | Agar alur diagram terstruktur dengan baik dan tidak ada jalur percabangan yang menggantung atau tidak jelas arahnya.

 |
| 5 | *Fork* dan *Join* (Paralel) | Menggunakan *fork* dan *join* secara berpasangan untuk proses yang berjalan paralel (seperti pada pemeriksaan kondisi fisik dan kelengkapan aksesori).

 | Karena proses paralel wajib disatukan kembali oleh *join* sebelum alur dilanjutkan, serta tidak boleh menggunakan *merge* untuk proses paralel.

 |
| 6 | Keterlacakan Langkah (*Traceability*) | Menyelaraskan nama *action* menggunakan kata kerja dan objek yang sama persis dengan bunyi langkah pada tabel skenario Pertemuan 5.

 | Agar keterlacakan antara dokumen skenario dan *activity diagram* mudah diperiksa dan divalidasi.

 |
| 7 | Langkah *Include* | Memasukkan langkah *include* (seperti *Periksa Ketersediaan* atau *Periksa Kondisi Peralatan*) sebagai *action* wajib pada alur utama.

 | Karena fungsi tersebut merupakan sub-proses yang selalu dipanggil di dalam alur aktivitas induknya.

 |
| 8 | Langkah *Extend* (Bersyarat) | Menggambarkan perilaku *extend* (seperti pilihan cetak bukti) sebagai cabang *decision* bersyarat dengan kondisi yang sesuai.

 | Agar alur penambahan fungsionalitas opsional terhubung dengan tepat pada *extension point* yang ditentukan.

 |
| 9 | Unsur Proses Baru | Memberikan keterangan "unsur proses baru" pada penambahan proses latihan khusus (seperti pemeriksaan kelengkapan aksesori).

 | Agar dapat dibedakan dengan jelas bahwa unsur tersebut merupakan tambahan materi latihan praktikum, bukan dari skenario sebelumnya.

 |
| 10 | Konsistensi Berkas & Struktur Folder | Menyimpan berkas sumber `.drawio` dan hasil ekspor `.png` ke dalam folder yang sesuai (`04_model_analisis/P06/LAB` atau `SIA`) dengan nomor versi yang konsisten.

 | Untuk menjaga kerapian struktur *workspace* praktikum dan kesesuaian penamaan artefak tugas.

 |