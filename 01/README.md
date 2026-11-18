# RANGKUMAN  SISTEM TERDISTRIBUSI DAN TERDESENTRALISASI
## Modul 1: Pengenalan Sistem Terdistribusi dan Terdesentralisasi

- **Nama:** Maria Widya Febrianti
- **NIM:** 255410011
- **Kelas:** IF-1
- **Program Studi:** Informatika
- **Universitas:** Universitas Teknologi Digital Indonesia (UTDI) Yogyakarta
- # MODUL 1 – Pengenalan Sistem Terdistribusi dan Terdesentralisasi
- Promt:buatkan saya ringkasan atau rangkuman dari  modul 1 di atas(pakai AI GPT)
- Promt:tolong ubah format ini ke bentuk format markdown README.md GitHub (pakai Gemini AI)

## 1. Pengertian Sistem Terdistribusi
**Sistem terdistribusi** merupakan sekumpulan komputer atau *node* yang saling terhubung melalui jaringan dan bekerja sama untuk menjalankan suatu sistem secara keseluruhan. Meskipun terdiri dari beberapa komputer yang berbeda, pengguna melihatnya seolah-olah sebagai satu sistem yang utuh.

Sistem ini digunakan untuk:
- Menangani jumlah pengguna dan data yang besar.
- Meningkatkan kinerja serta ketersediaan layanan (*availability*).

---

## 2. Arsitektur Sistem Terdistribusi
Terdapat tiga arsitektur dasar dalam sistem terdistribusi:

* **Client-Server**: Komunikasi antara *client* yang meminta layanan dan *server* yang memberikan layanan.
* **Peer-to-Peer (P2P)**: Setiap komputer dapat bertindak sebagai *client* maupun *server*.
* **Hybrid**: Gabungan dari arsitektur *client-server* dan *peer-to-peer*.

---

## 3. Karakteristik Sistem Terdistribusi
Beberapa karakteristik utama sistem terdistribusi meliputi:

| Karakteristik | Penjelasan |
| :--- | :--- |
| **Transparansi Lokasi** | Pengguna tidak perlu mengetahui lokasi fisik penyimpanan data. |
| **Skalabilitas** | Kemampuan sistem dalam menangani peningkatan jumlah pengguna dan beban kerja. |
| **Fault Tolerance** | Kemampuan sistem untuk tetap berjalan normal meskipun terjadi kegagalan pada komponen tertentu. |
| **Kinerja Tinggi** | Kemampuan memproses berbagai permintaan secara cepat dan efisien. |
| **Heterogenitas** | Kemampuan menggabungkan perangkat keras dan perangkat lunak yang berbeda-beda. |

---

## 4. Pengertian Sistem Terdesentralisasi
**Sistem terdesentralisasi** merupakan sistem yang pengendalian dan pengambilan keputusannya tidak hanya bergantung pada satu pusat. Kontrol didistribusikan kepada beberapa pihak atau *node*.

**Contoh penerapan:**
- Blockchain
- DNS (*Domain Name System*)
- BitTorrent

---

## 5. Perbedaan Sistem Terdistribusi dan Terdesentralisasi
Keduanya memiliki hubungan yang erat, tetapi mempunyai fokus tujuan yang berbeda:

- **Sistem Terdistribusi:** Lebih berfokus pada **pembagian beban kerja** (*workload*).
- **Sistem Terdesentralisasi:** Lebih berfokus pada **pembagian kendali atau kontrol** (*authority/control*).

---

## 6. Teorema CAP
Teorema CAP menjelaskan tiga karakteristik penting dalam sistem terdistribusi:

1. **Consistency (C)**: Semua *node* memiliki data yang sama dan konsisten pada waktu yang bersamaan.
2. **Availability (A)**: Sistem tetap memberikan respons setiap kali pengguna meminta layanan.
3. **Partition Tolerance (P)**: Sistem tetap dapat beroperasi meskipun terjadi gangguan komunikasi jaringan antar-*node*.

Ketika terjadi gangguan jaringan (*network partition*), sistem harus memilih salah satu dari dua pendekatan berikut:
* **AP (*Availability* & *Partition Tolerance*)**: Sistem tetap melayani permintaan pengguna, tetapi data antar-*node* mungkin belum sinkron.
* **CP (*Consistency* & *Partition Tolerance*)**: Sistem mempertahankan konsistensi data meskipun sebagian permintaan terpaksa tidak dapat dilayani.

---

## 7. Tantangan dan Tren Masa Depan

### Tantangan
- *Latency* (latensi)
- *Throughput*
- Keamanan (*security*)
- Pengelolaan *node*
- Tata kelola sistem (*governance*)

### Tren Perkembangan
- Cloud-native
- Kubernetes & Docker
- Edge Computing & Fog Computing
- Web3 & DeFi (*Decentralized Finance*)
- Federated Learning

---

> **Kesimpulan Modul 1**  
> Sistem terdistribusi dan terdesentralisasi merupakan fondasi penting dalam perkembangan teknologi modern. Sistem terdistribusi membantu membagi beban kerja, sedangkan sistem terdesentralisasi membantu membagi kendali. Kombinasi keduanya memungkinkan layanan berskala global seperti Google, Netflix, dan jaringan Blockchain dapat berjalan dengan optimal.
