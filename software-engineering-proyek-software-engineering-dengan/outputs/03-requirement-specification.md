# 03 Requirement Specification

## Nama Proyek
Campus Service Request and Maintenance System

## Sumber Input
- `outputs/01-inception-stakeholder.md`
- `outputs/02-elicitation-findings.md`
- `outputs/02-elicitation-questions.md`

## Ringkasan Sistem
Sistem digunakan oleh mahasiswa dan dosen untuk melaporkan masalah fasilitas kampus. Administrator memeriksa laporan, menolak laporan tidak valid, menugaskan teknisi, memperbarui progress teknisi, dan menutup laporan. Teknisi menangani laporan yang diberikan, memperbarui progress, dan menyelesaikan pekerjaan. Pelapor dapat melihat progress, memberi komentar, menerima notifikasi aplikasi, dan memberi konfirmasi. Manajer Fasilitas dapat melihat dashboard, laporan ringkas, dan memperbarui daftar ruangan.

## Functional Requirement

| ID | Requirement | Sumber |
| --- | --- | --- |
| FR-001 | Sistem harus mengizinkan mahasiswa dan dosen login menggunakan akun kampus sebelum membuat atau memantau laporan. | REQ-DRAFT-001 |
| FR-002 | Sistem harus mengizinkan pelapor membuat laporan masalah fasilitas kampus. | REQ-DRAFT-002 |
| FR-003 | Sistem harus menyimpan judul masalah, deskripsi, kategori masalah, lokasi ruangan, dan tingkat urgensi pada laporan. | REQ-DRAFT-003, REQ-DRAFT-025 |
| FR-004 | Sistem harus mengizinkan pelapor menyertakan bukti atau foto kerusakan secara opsional. | REQ-DRAFT-004 |
| FR-005 | Sistem harus menyediakan kategori masalah fasilitas seperti proyektor, internet, AC, kursi, alat laboratorium, kebersihan ruangan, dan kategori fasilitas lainnya. | REQ-DRAFT-005 |
| FR-006 | Sistem harus mengizinkan pelapor memilih lokasi dari daftar ruangan yang disediakan sistem. | REQ-DRAFT-006 |
| FR-007 | Sistem harus mengizinkan administrator memeriksa laporan yang masuk. | REQ-DRAFT-007 |
| FR-008 | Sistem harus mengizinkan administrator menolak laporan yang tidak valid. | REQ-DRAFT-008, REQ-DRAFT-027 |
| FR-009 | Sistem harus menyimpan alasan penolakan laporan jika laporan ditolak. | REQ-DRAFT-027 |
| FR-010 | Sistem harus mengizinkan administrator menugaskan laporan yang valid kepada teknisi. | REQ-DRAFT-009 |
| FR-011 | Sistem harus mengizinkan teknisi melihat dan menangani laporan yang diberikan kepadanya. | REQ-DRAFT-010 |
| FR-012 | Sistem harus mengizinkan teknisi memperbarui progress pekerjaan sampai selesai. | REQ-DRAFT-011 |
| FR-013 | Sistem harus mengizinkan administrator memperbarui progress teknisi dengan catatan alasan. | REQ-DRAFT-012, REQ-DRAFT-029 |
| FR-014 | Sistem harus mengizinkan teknisi mengubah status pekerjaan menjadi butuh bantuan, tertunda, atau menunggu suku cadang. | REQ-DRAFT-013 |
| FR-015 | Sistem harus mengizinkan lebih dari satu teknisi dikerahkan jika teknisi menyatakan butuh bantuan dan administrator menyetujuinya. | REQ-DRAFT-028 |
| FR-016 | Sistem harus mengizinkan pelapor melihat perkembangan laporan. | REQ-DRAFT-014 |
| FR-017 | Sistem harus mengizinkan pelapor memberi komentar tambahan setelah laporan dibuat. | REQ-DRAFT-015 |
| FR-018 | Sistem harus mengizinkan pelapor memberi konfirmasi setelah teknisi menyelesaikan pekerjaan. | REQ-DRAFT-016 |
| FR-019 | Sistem harus memberi batas waktu 45 menit kepada pelapor untuk memberikan konfirmasi setelah pekerjaan selesai. | REQ-DRAFT-020 |
| FR-020 | Sistem harus menutup laporan secara otomatis jika pelapor tidak memberi konfirmasi dalam 45 menit setelah pekerjaan selesai. | REQ-DRAFT-030 |
| FR-021 | Sistem harus mengizinkan administrator menutup laporan. | REQ-DRAFT-017, REQ-DRAFT-018 |
| FR-022 | Sistem harus mengirim notifikasi melalui aplikasi saat status laporan berubah pada kondisi yang ditentukan. | REQ-DRAFT-019, REQ-DRAFT-031 |
| FR-023 | Sistem harus mengirim notifikasi aplikasi saat masalah sudah ditangani, membutuhkan suku cadang baru, teknisi butuh bantuan, dan pekerjaan terjeda. | REQ-DRAFT-031 |
| FR-024 | Sistem harus menyediakan dashboard untuk Manajer Fasilitas. | REQ-DRAFT-021 |
| FR-025 | Dashboard harus menampilkan total masalah yang sudah diselesaikan. | REQ-DRAFT-022 |
| FR-026 | Dashboard harus menampilkan chart kategori masalah yang paling sering muncul. | REQ-DRAFT-023 |
| FR-027 | Dashboard harus dapat difilter atau diurutkan berdasarkan terbaru, terlama, ruangan, dan kategori. | REQ-DRAFT-032 |
| FR-028 | Sistem harus menyediakan laporan ringkas untuk Manajer Fasilitas. | REQ-DRAFT-024 |
| FR-029 | Laporan ringkas harus mengandung ruangan masalah dan kategori masalah. | REQ-DRAFT-033 |
| FR-030 | Sistem harus mengizinkan Manajer Fasilitas memperbarui daftar ruangan jika ada ruangan baru. | REQ-DRAFT-026 |

## Non-Functional Requirement

| ID | Requirement | Sumber |
| --- | --- | --- |
| NFR-001 | Sistem harus membatasi akses pembuatan dan pemantauan laporan kepada pelapor yang login menggunakan akun kampus. | REQ-DRAFT-001 |
| NFR-002 | Sistem harus menyediakan notifikasi di dalam aplikasi, bukan melalui email, WhatsApp, atau kanal eksternal pada scope awal. | REQ-DRAFT-019, ASUMSI dari elicitation |
| NFR-003 | Sistem harus menjaga pemisahan hak akses berdasarkan peran: pelapor, administrator, teknisi, dan Manajer Fasilitas. | STK-001 sampai STK-005 |
| NFR-004 | Sistem harus menyimpan jejak informasi penting pada laporan, termasuk status, progress, teknisi yang ditugaskan, komentar, konfirmasi, alasan penolakan, dan catatan alasan pembaruan progress administrator. | Data yang ditemukan |
| NFR-005 | Sistem tidak mencakup pembayaran, biaya perbaikan, pengadaan barang, integrasi sistem akademik, integrasi notifikasi eksternal, penilaian kinerja teknisi, atau dashboard analitik tingkat lanjut pada scope awal. | Di Luar Scope Awal |

## User Story

| ID | User Story | Requirement Terkait |
| --- | --- | --- |
| US-001 | Sebagai mahasiswa atau dosen, saya ingin login menggunakan akun kampus agar hanya pengguna kampus yang dapat membuat dan memantau laporan. | FR-001, NFR-001 |
| US-002 | Sebagai pelapor, saya ingin membuat laporan masalah fasilitas agar masalah kampus dapat diketahui dan ditangani. | FR-002, FR-003, FR-004, FR-005, FR-006 |
| US-003 | Sebagai administrator, saya ingin memeriksa laporan masuk agar laporan yang valid dapat diproses dan laporan tidak valid dapat ditolak. | FR-007, FR-008, FR-009 |
| US-004 | Sebagai administrator, saya ingin menugaskan laporan kepada teknisi agar pekerjaan perbaikan dapat dimulai. | FR-010 |
| US-005 | Sebagai teknisi, saya ingin melihat laporan yang diberikan kepada saya agar saya dapat menangani masalah fasilitas. | FR-011 |
| US-006 | Sebagai teknisi, saya ingin memperbarui progress dan status pekerjaan agar pelapor dan administrator mengetahui perkembangan pekerjaan. | FR-012, FR-014, FR-022, FR-023 |
| US-007 | Sebagai teknisi, saya ingin meminta bantuan melalui status butuh bantuan agar administrator dapat mengerahkan lebih dari satu teknisi jika diperlukan. | FR-014, FR-015 |
| US-008 | Sebagai administrator, saya ingin memperbarui progress teknisi dengan catatan alasan agar progress tetap akurat ketika teknisi sudah memberi informasi kepada administrator. | FR-013 |
| US-009 | Sebagai pelapor, saya ingin melihat perkembangan laporan dan memberi komentar tambahan agar saya dapat mengikuti proses penanganan masalah. | FR-016, FR-017 |
| US-010 | Sebagai pelapor, saya ingin memberi konfirmasi setelah pekerjaan selesai agar administrator dapat mengetahui apakah laporan dapat ditutup. | FR-018, FR-019 |
| US-011 | Sebagai administrator, saya ingin laporan dapat ditutup otomatis setelah 45 menit tanpa konfirmasi agar laporan selesai tidak tertahan terlalu lama. | FR-020, FR-021 |
| US-012 | Sebagai Manajer Fasilitas, saya ingin melihat dashboard agar saya dapat memantau total masalah selesai dan kategori masalah yang sering muncul. | FR-024, FR-025, FR-026, FR-027 |
| US-013 | Sebagai Manajer Fasilitas, saya ingin melihat laporan ringkas agar saya dapat mengetahui ruangan dan kategori masalah. | FR-028, FR-029 |
| US-014 | Sebagai Manajer Fasilitas, saya ingin memperbarui daftar ruangan agar pilihan lokasi laporan tetap sesuai kondisi kampus. | FR-030 |

## Acceptance Criteria

### FR-001 Login Akun Kampus
1. Jika mahasiswa atau dosen belum login, sistem tidak mengizinkan pengguna membuat laporan.
2. Jika mahasiswa atau dosen berhasil login dengan akun kampus, sistem mengizinkan pengguna mengakses fitur pelaporan.

### FR-002, FR-003, FR-004, FR-005, FR-006 Pembuatan Laporan
1. Jika pelapor mengisi judul masalah, deskripsi, kategori masalah, lokasi ruangan, dan tingkat urgensi, sistem dapat menyimpan laporan.
2. Jika pelapor tidak mengisi deskripsi, sistem tidak dapat mengirim laporan sebagai laporan valid.
3. Jika pelapor memilih kategori masalah dari daftar kategori fasilitas, sistem menyimpan kategori tersebut pada laporan.
4. Jika pelapor memilih lokasi dari daftar ruangan, sistem menyimpan lokasi tersebut pada laporan.
5. Jika pelapor menyertakan bukti atau foto, sistem menyimpan bukti tersebut bersama laporan.
6. Jika pelapor tidak menyertakan bukti atau foto, sistem tetap dapat menyimpan laporan selama data wajib terpenuhi.

### FR-007, FR-008, FR-009 Pemeriksaan dan Penolakan Laporan
1. Administrator dapat melihat laporan yang masuk.
2. Administrator dapat menolak laporan jika judul tidak sesuai dengan deskripsi dan/atau kategori.
3. Administrator dapat menolak laporan jika deskripsi kosong.
4. Administrator dapat menolak laporan jika lokasi tidak diketahui atau salah.
5. Jika administrator menolak laporan, sistem menyimpan alasan penolakan.

### FR-010, FR-011 Penugasan Teknisi
1. Administrator dapat menugaskan laporan valid kepada teknisi.
2. Setelah laporan ditugaskan, teknisi yang ditunjuk dapat melihat laporan tersebut.
3. Teknisi lain yang tidak ditugaskan tidak dianggap sebagai teknisi utama laporan tersebut.

### FR-012, FR-014 Progress Teknisi
1. Teknisi dapat memperbarui progress pekerjaan pada laporan yang ditugaskan kepadanya.
2. Teknisi dapat mengubah status menjadi butuh bantuan.
3. Teknisi dapat mengubah status menjadi tertunda.
4. Teknisi dapat mengubah status menjadi menunggu suku cadang.
5. Perubahan progress atau status tersimpan pada laporan.

### FR-013 Progress oleh Administrator
1. Administrator dapat memperbarui progress teknisi.
2. Sistem meminta catatan alasan saat administrator memperbarui progress teknisi.
3. Sistem menyimpan catatan alasan pembaruan progress administrator.

### FR-015 Bantuan Teknisi Tambahan
1. Jika teknisi mengubah status menjadi butuh bantuan, administrator dapat menyetujui bantuan tambahan.
2. Jika administrator menyetujui bantuan tambahan, lebih dari satu teknisi dapat dikerahkan untuk laporan tersebut.
3. Jika status bukan butuh bantuan, sistem tidak menggunakan aturan pengerahan teknisi tambahan.

### FR-016, FR-017 Pemantauan dan Komentar Pelapor
1. Pelapor dapat melihat perkembangan laporan miliknya.
2. Pelapor dapat memberi komentar tambahan setelah laporan dibuat.
3. Komentar tambahan tersimpan pada laporan.

### FR-018, FR-019, FR-020 Konfirmasi Pelapor dan Penutupan Otomatis
1. Setelah teknisi menyelesaikan pekerjaan, pelapor dapat memberi konfirmasi.
2. Sistem memberi waktu 45 menit untuk konfirmasi pelapor setelah pekerjaan selesai.
3. Jika pelapor tidak memberi konfirmasi dalam 45 menit, sistem menutup laporan secara otomatis.

### FR-021 Penutupan oleh Administrator
1. Administrator dapat menutup laporan.
2. Administrator boleh menutup laporan tanpa konfirmasi pelapor.
3. Status laporan berubah menjadi tertutup setelah administrator menutup laporan.

### FR-022, FR-023 Notifikasi Aplikasi
1. Sistem mengirim notifikasi melalui aplikasi saat masalah sudah ditangani.
2. Sistem mengirim notifikasi melalui aplikasi saat laporan membutuhkan suku cadang baru.
3. Sistem mengirim notifikasi melalui aplikasi saat teknisi butuh bantuan.
4. Sistem mengirim notifikasi melalui aplikasi saat pekerjaan terjeda.

### FR-024, FR-025, FR-026, FR-027 Dashboard Manajer Fasilitas
1. Manajer Fasilitas dapat membuka dashboard.
2. Dashboard menampilkan total masalah yang sudah diselesaikan.
3. Dashboard menampilkan chart kategori masalah yang paling sering muncul.
4. Dashboard dapat difilter atau diurutkan berdasarkan terbaru.
5. Dashboard dapat difilter atau diurutkan berdasarkan terlama.
6. Dashboard dapat difilter berdasarkan ruangan.
7. Dashboard dapat difilter berdasarkan kategori.

### FR-028, FR-029 Laporan Ringkas
1. Manajer Fasilitas dapat melihat laporan ringkas.
2. Laporan ringkas menampilkan ruangan masalah.
3. Laporan ringkas menampilkan kategori masalah.

### FR-030 Daftar Ruangan
1. Manajer Fasilitas dapat menambahkan ruangan baru ke daftar ruangan.
2. Ruangan baru yang ditambahkan tersedia sebagai pilihan lokasi laporan.

## Requirement yang Masih Belum Dispesifikasikan
Bagian berikut berasal dari `02-elicitation-questions.md` dan belum dijadikan requirement formal karena belum ada jawaban final:

1. Apakah pelapor dapat mengubah laporan setelah dikirim.
2. Apakah pelapor dapat membatalkan laporan.
3. Apakah daftar ruangan perlu dikelompokkan berdasarkan gedung, lantai, atau jenis ruangan.
4. Apa yang terjadi jika pelapor tidak setuju bahwa pekerjaan sudah selesai.
5. Apakah notifikasi perlu memiliki daftar riwayat dan status sudah dibaca.
6. Apakah administrator dapat mengedit kategori, lokasi, atau deskripsi laporan sebelum menugaskan teknisi.
7. Apakah administrator dapat menggabungkan laporan duplikat.
8. Apakah administrator dapat mengganti teknisi setelah laporan berjalan.
9. Apakah teknisi dapat mengunggah foto hasil pekerjaan atau memperkirakan waktu penyelesaian.
10. Apakah laporan ringkas perlu dapat diunduh.
11. Apakah Manajer Fasilitas dapat memberi catatan tindak lanjut.

## Traceability Ringkas

| Source | Requirement Formal |
| --- | --- |
| REQ-DRAFT-001 | FR-001, NFR-001, US-001 |
| REQ-DRAFT-002 sampai REQ-DRAFT-006, REQ-DRAFT-025 | FR-002 sampai FR-006, US-002 |
| REQ-DRAFT-007, REQ-DRAFT-008, REQ-DRAFT-027 | FR-007 sampai FR-009, US-003 |
| REQ-DRAFT-009, REQ-DRAFT-010 | FR-010, FR-011, US-004, US-005 |
| REQ-DRAFT-011 sampai REQ-DRAFT-013, REQ-DRAFT-028, REQ-DRAFT-029 | FR-012 sampai FR-015, US-006 sampai US-008 |
| REQ-DRAFT-014 sampai REQ-DRAFT-020, REQ-DRAFT-030 | FR-016 sampai FR-021, US-009 sampai US-011 |
| REQ-DRAFT-019, REQ-DRAFT-031 | FR-022, FR-023 |
| REQ-DRAFT-021 sampai REQ-DRAFT-024, REQ-DRAFT-032, REQ-DRAFT-033 | FR-024 sampai FR-029, US-012, US-013 |
| REQ-DRAFT-026 | FR-030, US-014 |

## ASUMSI
1. ASUMSI: Mahasiswa dan dosen memiliki hak pelaporan yang sama pada tahap awal.
2. ASUMSI: Notifikasi aplikasi berarti notifikasi hanya tampil di dalam sistem.
3. ASUMSI: Laporan ringkas tidak termasuk dashboard analitik tingkat lanjut.

## Quality Check
- Functional requirement berisi perilaku sistem.
- Non-functional requirement berisi batasan akses, scope, dan kualitas pencatatan data.
- User story menggunakan format peran, tujuan, dan manfaat.
- Setiap user story terhubung ke requirement.
- Acceptance criteria dapat diuji.
- Setiap requirement memiliki ID unik.
- Requirement yang belum cukup jelas tidak dipaksa menjadi requirement formal.

## Human Review
Manusia perlu memeriksa apakah `FR`, `NFR`, `US`, dan acceptance criteria sudah mewakili kebutuhan stakeholder sebelum lanjut ke prioritas atau desain.
