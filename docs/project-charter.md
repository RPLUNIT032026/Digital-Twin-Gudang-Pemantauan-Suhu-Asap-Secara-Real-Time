# 📋 Project Charter — GTD

> Dokumen resmi yang memuat latar belakang, tujuan, ruang lingkup, dan struktur tim proyek.

| | |
|---|---|
| **Nama Proyek** | DTG — Digital Twin Gudang |
| **Mata Kuliah** | Rekayasa Perangkat Lunak |
| **Periode Sprint 1** | September 2026 |
| **Target** | Product Release 1 |
| **Repository** | https://github.com/RPLUNIT032026/24-GACORRR |

---

## 1. 🌍 Latar Belakang

Gudang menyimpan banyak barang bernilai, dan sebagian bersifat mudah terbakar (kardus, plastik, kayu, bahan kimia). Kebakaran di gudang sering terlambat disadari karena pemantauan masih dilakukan secara manual, yaitu petugas berkeliling memeriksa kondisi.

Dua tanda awal kebakaran yang paling mudah diukur adalah **kenaikan suhu** dan **munculnya asap**. Bila keduanya dipantau terus-menerus dan ditampilkan dalam satu tampilan yang mudah dibaca, tindakan pencegahan dapat dilakukan lebih cepat.

Konsep **digital twin** menjawab kebutuhan ini: membuat representasi digital dari gudang fisik yang selalu diperbarui berdasarkan data sensor.

## 2. 🎯 Tujuan Proyek

1. Membangun software digital twin yang menampilkan kondisi **suhu** dan **asap** tiap zona gudang.
2. Memberikan **status otomatis** (Aman, Waspada, Bahaya) berdasarkan ambang batas.
3. Menerapkan praktik rekayasa perangkat lunak: Agile (Scrum), pengukuran Function Point, dan version control dengan GitHub.

## 3. 📦 Ruang Lingkup

### ✅ Termasuk (In Scope)
- Simulasi data sensor suhu dan sensor asap
- API untuk menerima dan menyajikan data sensor
- Penyimpanan data ke database
- Pencatatan dan tampilan alarm
- Login admin dan pengaturan ambang batas

### ❌ Tidak Termasuk (Out of Scope)
- Pemasangan sensor fisik di gudang sungguhan
- Aplikasi mobile
- Notifikasi WhatsApp/SMS ke pihak luar
- Sistem pemadam otomatis

## 4. 🗓️ Milestone

| Sprint | Fokus | Target |
|---|---|---|
| **Sprint 1** | Perencanaan, desain, project setup | September 2026 |
| **Sprint 2** | API sensor, database, logika status | Oktober 2026 |
| **Sprint 3** | Dashboard denah dan grafik | Oktober – November 2026 |
| **Sprint 4** | Alarm, pengujian, Product Release | November 2026 |

> Jadwal sprint selanjutnya bersifat rencana dan menyesuaikan kalender perkuliahan.

## 5. 🛠️ Teknologi

| Lapisan | Teknologi |
|---|---|
| Backend | Python, Flask |
| Database | SQL |
| Frontend | HTML, CSS, JavaScript |
| Desain | Figma |
| Version Control | Git & GitHub |
| Manajemen Tugas | Product Backlog |

## 6. ⚠️ Risiko & Mitigasi

| # | Risiko | Dampak | Mitigasi |
|---|---|---|---|
| 1 | Anggota belum familiar dengan API | Sedang | Belajar bertahap, latihan kode kecil, saling bantu |
| 2 | Pembagian tugas tidak merata | Tinggi | Setiap anggota punya dokumen/modul sendiri dan wajib commit |
| 3 | Sensor fisik tidak tersedia | Rendah | Menggunakan simulator data |
| 4 | Waktu terbatas menjelang Sprint Review | Tinggi | Prioritaskan fitur inti, tunda fitur tambahan |
| 5 | Konflik saat menggabungkan kode | Sedang | Commit kecil dan sering, bagi file per anggota |

## 7. ✅ Kriteria Keberhasilan

- Seluruh dokumen Sprint 1 terunggah di GitHub
- Setiap anggota memiliki riwayat commit
- Project setup dapat dijalankan (struktur folder, kerangka kode, database awal)
- Status zona berubah sesuai ambang batas pada dashboard (target Product Release 1)

