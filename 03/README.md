# RANGKUMAN  SISTEM TERDISTRIBUSI DAN TERDESENTRALISASI
## Modul 3: Sinkronisasi dan Koordinasi pada Sistem Terdistribusi

- **Nama:** Maria Widya Febrianti
- **NIM:** 255410011
- **Kelas:** IF-1
- **Program Studi:** Informatika
- **Universitas:** Universitas Teknologi Digital Indonesia (UTDI) Yogyakarta
- # MODUL 3 – Sinkronisasi dan Koordinasi pada Sistem Terdistribusi
- Promt:buatkan saya ringkasan atau rangkuman dari  modul 3 di atas(pakai AI GPT)
- Promt:tolong ubah format ini ke bentuk format markdown REDMI.md GitHub (pakai Gemini AI)
- # MODUL 3 – Sinkronisasi dan Koordinasi pada Sistem Terdistribusi

## 1. Pengertian Sinkronisasi
**Sinkronisasi** merupakan proses mengatur dan menyelaraskan jalannya proses, data, serta penggunaan sumber daya pada beberapa *node* agar dapat bekerja secara terkoordinasi.

**Tujuan utama sinkronisasi:**
- Menjaga konsistensi data.
- Mencegah terjadinya konflik akses.
- Memastikan setiap proses berjalan sesuai urutan dan aturan yang benar.

---

## 2. Pentingnya Sinkronisasi
Sinkronisasi sangat diperlukan dalam sistem terdistribusi untuk:

* Menjaga integritas data.
* Menyelaraskan kondisi atau *state* aplikasi.
* Mengatur pelaksanaan tugas (*task scheduling*).
* Mengelola penggunaan sumber daya bersama.
* Mencegah terjadinya *deadlock*.
* Mendukung proses *load balancing*.
* Meningkatkan efisiensi sistem secara keseluruhan.

> **Contoh Kasus:**  
> Pada aplikasi *e-commerce*, ketika dua pengguna membeli produk yang sama secara bersamaan, mekanisme sinkronisasi memastikan pengurangan stok diproses secara akurat. Tanpa sinkronisasi, jumlah stok dapat tercatat tidak sesuai dengan transaksi sebenarnya (*race condition*).

---

## 3. Tantangan Sinkronisasi
Beberapa tantangan utama yang sering dihadapi dalam melakukan sinkronisasi pada sistem terdistribusi:

- *Network latency* dan *network partitioning*
- Skalabilitas sistem
- Kegagalan komponen atau *node*
- *Concurrency control* (pengendalian akses bersamaan)
- Konsistensi data antar-*node*
- Perbedaan jam (*clock drift*) pada setiap komputer

---

## 4. Sinkronisasi Waktu Fisik
**Sinkronisasi waktu fisik** merupakan proses menyelaraskan jam nyata (*real-time clock*) pada komputer-komputer yang berbeda agar menunjukkan waktu yang seragam. Hal ini sangat krusial untuk pencatatan *log*, penjadwalan kegiatan, dan pengurutan kejadian.

| Standar / Teknologi | Keterangan |
| :--- | :--- |
| **UTC** (*Coordinated Universal Time*) | Standar waktu utama yang digunakan secara global. |
| **TAI** (*International Atomic Time*) | Skala waktu berpresisi tinggi berdasarkan jam atom. |
| **GPS** | Sistem satelit yang menyediakan referensi waktu akurat. |
| **Atomic Clock** | Jam dengan tingkat akurasi tertinggi sebagai referensi waktu fisik. |
| **NTP** (*Network Time Protocol*) | Protokol untuk menyinkronkan waktu komputer melalui jaringan. |
| **PTP** (*Precision Time Protocol*) | Protokol sinkronisasi waktu jaringan dengan tingkat presisi jauh lebih tinggi dibanding NTP. |

---

## 5. Sinkronisasi Waktu Logis
**Sinkronisasi waktu logis** digunakan untuk menentukan urutan kausal kejadian dalam sistem terdistribusi tanpa harus bergantung pada kesamaan jam fisik.

### Lamport Logical Clock
Prinsip kerja algoritma *Lamport Logical Clock*:
1. Setiap kali terjadi suatu kejadian internal di dalam proses, nilai *logical clock* bertambah satu ($C_i = C_i + 1$).
2. Ketika mengirimkan pesan, proses pengirim menyertakan nilai *logical clock* terbarunya pada pesan tersebut.
3. Ketika menerima pesan, proses penerima membandingkan nilai *clock* yang diterima dengan *clock* miliknya sendiri, mengambil nilai terbesar, lalu menambahkannya dengan satu:
   $$C_j = \max(C_j, C_{\text{pesan}}) + 1$$

### Vector Clock
Selain *Lamport Clock*, terdapat juga **Vector Clock** yang mencatat hubungan sebab-akibat (*causality*) kejadian antarproses menggunakan struktur array/vektor nilai dari setiap *node*.

---

## 6. Mutual Exclusion
**Mutual Exclusion** merupakan mekanisme untuk memastikan hanya **satu proses** yang dapat mengakses atau menggunakan sumber daya kritis (*critical section*) tertentu pada satu waktu.

- **Tujuan:** Mencegah inkonsistensi dan konflik ketika beberapa proses mencoba memodifikasi sumber daya yang sama secara bersamaan.
- **Contoh:** Mengunci akses baris data stok barang sementara waktu ketika dua pengguna melakukan transaksi *checkout* di detik yang sama.

---

## 7. Pemilihan Koordinator (*Leader Election*)
**Pemilihan koordinator** merupakan proses menentukan satu *node* utama yang bertugas mengatur atau mengoordinasikan jalannya pekerjaan *node-node* lainnya.

- Koordinator dibutuhkan agar orkestrasi proses dalam sistem berjalan teratur.
- Apabila *node* koordinator mengalami kegagalan (*crash*), sistem secara otomatis akan menjalankan algoritma pemilihan untuk menentukan koordinator pengganti.

---

> **Kesimpulan Modul 3**  
> Sinkronisasi dan koordinasi sangat diperlukan dalam sistem terdistribusi agar setiap *node* dapat bekerja secara selaras dan teratur. Sinkronisasi waktu fisik maupun logis membantu mengatur urutan kejadian secara akurat, sementara *mutual exclusion* dan pemilihan koordinator berperan mencegah konflik serta mengoptimalkan penggunaan sumber daya bersama.
