<div align="center">

# 🏭DTG

### Digital Twin Gudang — Pemantauan Suhu & Asap Secara Real-Time

*Kembaran digital yang menjaga gudang tetap aman.*

![Status](https://img.shields.io/badge/Sprint-1%20(Project%20Setup)-2ea44f?style=for-the-badge)
![Mata Kuliah](https://img.shields.io/badge/Mata%20Kuliah-Rekayasa%20Perangkat%20Lunak-orange?style=for-the-badge)

</div>

---

## ✨ Tentang Proyek

**DTG** adalah aplikasi *digital twin* untuk gudang. Setiap zona di gudang (rak, ruang penyimpanan, area bongkar muat) punya **kembaran digital** di layar yang menampilkan kondisi aslinya: **suhu** dan **kadar asap**.

Kalau ada zona yang mulai panas atau berasap, kembaran digitalnya langsung berubah warna dan sistem mencatat alarm, sehingga potensi kebakaran bisa terdeteksi lebih dini.

---

## 🎯 Fitur Utama

| | Fitur | Deskripsi |
|---|---|---|
| 🌡️ | **Monitoring Suhu** | Suhu tiap zona gudang diperbarui berkala |
| 💨 | **Monitoring Asap** | Kadar asap (ppm) tiap zona dipantau terus-menerus |
| 🚦 | **Status Tiga Level** | Aman 🟢 · Waspada 🟡 · Bahaya 🔴 |
| 🚨 | **Alarm Otomatis** | Setiap kondisi bahaya tercatat lengkap dengan waktu |

---

## 📄 Dokumen Sprint 1

| # | Dokumen | Keterangan |
|---|---|---|
| 1 | 📋 [Project Charter](docs/project-charter.md) | Latar belakang, tujuan, ruang lingkup, risiko |
| 2 | 🧮 [Perhitungan Function Point](docs/function-point.md) | Estimasi ukuran fungsionalitas aplikasi |
| 3 | 📝 [Product Backlog & Sprint 1 Backlog](docs/product-backlog.md) | User story dan target pekerjaan |
| 4 | 🧩 [System Design](docs/system-design.md) | Arsitektur, flowchart, dan ERD |
| 5 | 🎨 [Desain UI/UX](docs/ui-design.md) | Wireframe, palet warna, dan alur pengguna |
| 6 | 🌐 [context-diagram](UML-DIAGRAM/1_context-diagram.png) | Gambaran batas sistem secara umum serta aliran data antara perangkat sensor, sistem Digital Twin, dan pengguna. |
| 7 | 👥 [Use Case Diagram](UML-DIAGRAM/2_Use-Case%20Diagram.drawio.png) | Daftar fitur dan hak akses yang dapat dijalankan oleh aktor (Petugas/Admin Gudang) di dalam aplikasi. |
| 8 | 🔄 [Activity-Diagram-DTG](UML-DIAGRAM/3_Activity-Diagram-DTG.png) | Alur kerja bertahap dari proses akuisisi sensor, evaluasi ambang batas suhu/asap, hingga pemicuan alarm. |
| 9 | ⏱️ [sequence-diagram](UML-DIAGRAM/4_sequence-diagram.png) | Urutan komunikasi *real-time* antar komponen (Node IoT, Server, Database, dan Dashboard) berdasarkan garis waktu. |
| 10 | 🗂️ [Class Diagram](UML-DIAGRAM/5_class-diagram.drawio.png) | **Daftar Kelas Utama:**<br>• **`Gudang`**: Menyimpan informasi utama bangunan gudang dan referensi denah visual.<br>• **`ZonaGudang`**: Merepresentasikan titik/area ruangan pada denah beserta koordinat dan status warnanya (*Normal/Waspada/Bahaya*).<br>• **`NodeSensor`**: Merepresentasikan perangkat sensor suhu dan asap yang mengirimkan data telemetri melalui API.<br>• **`LogSensor`**: Menyimpan riwayat pembacaan suhu dan asap secara berkala (*time-series*) untuk grafik riwayat.<br>• **`KonfigurasiThreshold`**: Mengatur batas nilai waspada dan bahaya sebagai dasar evaluasi logika status gudang.<br>• **`AlarmInsiden`**: Mencatat kejadian darurat dan mengontrol aktivasi alarm ketika ambang batas terlampaui.<br>• **`PetugasGudang`**: Entitas pengguna/admin yang memantau dashboard Digital Twin dan melakukan *acknowledge* saat alarm berbunyi. |
| 11 | 🚦 [State-Diagram-DTG](UML-DIAGRAM/6_State-Diagram-DTG.png) | Siklus perubahan status kondisi gudang (Normal, Waspada, Bahaya) berdasarkan pemicu nilai sensor. |
| 12 | ☁️ [deployment-diagram](UML-DIAGRAM/7_deployment-diagram.png) | Arsitektur penempatan perangkat keras (Node IoT, Server, Client) dan protokol jaringan yang menghubungkannya. |
| 13 | 🔌 [component-diagram](UML-DIAGRAM/8_component-diagram.png) | Hubungan modular dan antarmuka (*interface*) antar subsistem *hardware*, *backend*, *database*, dan *frontend*. |
---

## 📁 Struktur Repository

```
Digital-Twin-RPL/
├── README.md
├── docs/
│   ├── project-charter.md
│   ├── function-point.md
│   ├── product-backlog.md
│   ├── system-design.md
│   └── ui-design.md
└── backend/        ← API & simulator sensor
```
---

## 🚦 Ambang Batas Status

| Status | Suhu | Kadar Asap |
|---|---|---|
| 🟢 **Aman** | < 35 °C | < 300 ppm |
| 🟡 **Waspada** | 35 – 45 °C | 300 – 600 ppm |
| 🔴 **Bahaya** | > 45 °C | > 600 ppm |

Ambang batas bisa diubah admin per zona.


Detail lengkap ada di [System Design](docs/system-design.md).

---

Detail lengkap ada di [System Design](docs/system-design.md).

---

## 🗓️ Roadmap

- [x] **[Sprint 1](./docs)** — [Project setup](./docs), [desain (UML)](./UML-DIAGRAM).
- [ ] **Sprint 2** — API sensor dan logika status
- [ ] **Sprint 3** — Dashboard denah gudang dan grafik riwayat
- [ ] **Sprint 4** — Alarm, pengujian, dan **Product Release**

---

## 👥 Tim

| No | Nama | NIM | Akun GitHub | Fokus Sprint 1 |
|:---:|---|:---:|---|---|
| **1** | Muhammad Rizky Syaban | 240504081 | [@Iksyaban14](https://github.com/Iksyaban14) | Project Charter & Project Setup |
| **2** | Muhammad Arby | 240504089 | [@Arby2464](https://github.com/Arby2464) | Product Backlog & System Design |
| **3** | Muhammad Fazil Fayyaz | 240504084 | [@FazilFayyaz](https://github.com/FazilFayyaz) | Function Point & Desain UI/UX |
---

<div align="center">

**Universitas Samudera** · Program Studi Informatika
Mata Kuliah Rekayasa Perangkat Lunak · 2026

*Dibuat dengan ☕ dan sedikit rasa panik menjelang deadline.*

</div>
