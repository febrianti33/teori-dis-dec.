# RANGKUMAN  SISTEM TERDISTRIBUSI DAN TERDESENTRALISASI
## Modul 4:Konsistensi dan Replikasi pada Sistem Terdistribusi

- **Nama:** Maria Widya Febrianti
- **NIM:** 255410011
- **Kelas:** IF-1
- **Program Studi:** Informatika
- **Universitas:** Universitas Teknologi Digital Indonesia (UTDI) Yogyakarta
- # MODUL 4 – Konsistensi dan Replikasi pada Sistem Terdistribusi
- Promt:buatkan saya ringkasan atau rangkuman dari  modul 4 di atas(pakai AI GPT)
- Promt:tolong ubah format ini ke bentuk format markdown README.md GitHub (pakai Gemini AI)
- # MODUL 4 – Konsistensi dan Replikasi pada Sistem Terdistribusi

## 1. Pengertian Konsistensi
**Konsistensi** merupakan keadaan ketika semua *node* dalam sistem terdistribusi memiliki data yang sama atau menampilkan informasi yang sinkron dan sesuai. 

Hal ini sangat diperlukan karena data disimpan pada beberapa server yang berbeda. Jika salah satu server mengalami perubahan data, server-server lainnya juga perlu mendapatkan pembaruan tersebut agar tidak terjadi perbedaan informasi (*data divergence*).

---

## 2. Pentingnya Konsistensi
Konsistensi sangat penting untuk menjaga keakuratan dan integritas data. 

> **Contoh Kasus:**  
> Dalam transaksi perbankan, ketika seseorang melakukan transfer uang, saldo rekening pengirim harus berkurang dan saldo rekening penerima harus bertambah secara akurat. Jika perubahan tersebut tidak tersinkronisasi dengan baik, pengguna dapat melihat informasi saldo yang tidak konsisten atau salah.

---

## 3. Teorema CAP
Teorema CAP membahas tiga aspek utama dalam sistem terdistribusi:
- **Consistency**: Kesamaan dan ketepatan data di setiap *node*.
- **Availability**: Ketersediaan layanan agar selalu dapat diakses.
- **Partition Tolerance**: Kemampuan sistem dalam menghadapi gangguan koneksi jaringan.

Ketika terjadi gangguan jaringan (*network partition*), sistem harus menentukan pilihan prioritas antara pendekatan **AP** (*Availability & Partition Tolerance*) atau **CP** (*Consistency & Partition Tolerance*).

---

## 4. Model Konsistensi
Terdapat beberapa model konsistensi dalam sistem terdistribusi:

1. **Strong Consistency**: Semua *node* langsung melihat data terbaru secara serentak setelah terjadi perubahan.
2. **Eventual Consistency**: Data tidak harus langsung sama di semua tempat, tetapi dijamin akan menjadi konsisten setelah beberapa waktu.
3. **Causal Consistency**: Urutan kejadian yang saling berhubungan secara kausal harus tetap dipertahankan oleh semua *node*.
4. **Read-Your-Writes Consistency**: Memastikan bahwa pengguna dapat langsung melihat perubahan data yang baru saja dibuatnya sendiri.
5. **Monotonic Read Consistency**: Pengguna tidak akan melihat versi data yang lebih lama dari versi data yang sudah pernah dilihatnya sebelumnya.
6. **Sequential Consistency**: Semua *node* melihat urutan operasi yang sama, meskipun tidak harus terjadi secara *real-time*.
7. **Linearizability**: Operasi terlihat seolah-olah berlangsung secara langsung (*instantaneous*) dan atomik dengan urutan global yang konsisten.

---

## 5. Trade-off Latensi dengan Konsistensi
Terdapat hubungan berbanding terbalik antara tingkat konsistensi dan kecepatan respons (*latency*) sistem:

- **Konsistensi tinggi**: Biasanya membutuhkan waktu lebih lama karena sistem harus menunggu proses sinkronisasi selesai di seluruh replika.
- **Konsistensi lebih longgar**: Memungkinkan respons yang jauh lebih cepat, tetapi data antarserver mungkin belum sama dalam waktu tertentu.

> **Contoh Penerapan:**  
> - **Sistem Perbankan**: Membutuhkan tingkat konsistensi yang sangat tinggi untuk mencegah kesalahan nominal.
> - **Media Sosial**: Dapat menggunakan *eventual consistency* demi performa dan kecepatan akses yang tinggi.

---

## 6. Pengertian Replikasi Data
**Replikasi data** merupakan proses membuat dan memelihara salinan data yang sama pada beberapa *node* atau server yang berbeda.

**Tujuan utama replikasi:**
- Meningkatkan ketersediaan data (*availability*).
- Meningkatkan kinerja sistem secara keseluruhan.
- Mengurangi risiko kehilangan data (*data loss*).
- Membantu pembagian beban kerja (*load distribution*).
- Meningkatkan skalabilitas sistem.

---

## 7. Jenis Replikasi
Beberapa jenis arsitektur replikasi yang umum digunakan:

- **Master-Slave (Primary-Backup)**: Satu server bertindak sebagai pusat penulisan data (*master*), sedangkan server lainnya bertindak sebagai *slave* yang hanya memuat salinan data untuk dibaca.
- **Multi-Master (Master-Master)**: Beberapa server dapat melakukan operasi pembacaan dan penulisan data secara mandiri.
- **Synchronous Replication**: Perubahan data harus diselesaikan dan dikonfirmasi pada semua replika sebelum transaksi dianggap selesai.
- **Asynchronous Replication**: Perubahan data dikirim ke replika setelah transaksi pada server utama selesai diproses.

---

## 8. Strategi Sinkronisasi Replika
Strategi sinkronisasi replika dapat diklasifikasikan berdasarkan beberapa parameter:

- **Waktu sinkronisasi**: *Synchronous*, *asynchronous*, dan *semi-synchronous*.
- **Arah replikasi**: *Master-slave*, *master-master*, dan *master-master asymmetric*.
- **Cara sinkronisasi**: *Pull-based*, *push-based*, dan *hybrid*.
- **Penanganan konflik**: 
  - *Last Write Wins* (LWW)
  - *Vector Clock*
  - CRDT (*Conflict-free Replicated Data Types*)
  - *Operational Transformation*

---

> **Kesimpulan Modul 4**  
> Konsistensi dan replikasi merupakan fondasi penting dalam menjaga keandalan dan ketahanan data pada sistem terdistribusi. Konsistensi memastikan keakuratan data antarserver, sementara replikasi menyediakan salinan cadangan guna meningkatkan ketersediaan, performa, serta keamanan penyimpanan data secara global.

