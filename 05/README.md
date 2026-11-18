# RANGKUMAN  SISTEM TERDISTRIBUSI DAN TERDESENTRALISASI
## Modul 5:Fault Tolerance

- **Nama:** Maria Widya Febrianti
- **NIM:** 255410011
- **Kelas:** IF-1
- **Program Studi:** Informatika
- **Universitas:** Universitas Teknologi Digital Indonesia (UTDI) Yogyakarta
- # MODUL 5 – Fault Tolerance
- Promt:buatkan saya ringkasan atau rangkuman dari  modul 5 di atas(pakai AI GPT)
- Promt:tolong ubah format ini ke bentuk format markdown README.md.md GitHub (pakai Gemini AI)
- # MODUL 5 – Fault Tolerance

## 1. Pengertian Fault Tolerance
**Fault Tolerance** merupakan kemampuan suatu sistem untuk tetap beroperasi dengan baik meskipun terjadi kegagalan (*failure*) pada satu atau beberapa komponen penyusunnya.

Konsep ini sangat penting untuk sistem yang membutuhkan tingkat ketersediaan tinggi (*high availability*), seperti layanan perbankan, infrastruktur *cloud*, dan berbagai aplikasi kritikal lainnya.

---

## 2. Pentingnya Fault Tolerance
Sistem terdistribusi melibatkan banyak komponen yang saling terhubung secara kompleks. Jika salah satu komponen mengalami gangguan atau kerusakan, komponen lainnya harus tetap mampu menjalankan tugasnya agar layanan keseluruhan tidak berhenti sepenuhnya (*fail-stop prevention*).

---

## 3. Jenis-Jenis Fault
Terdapat empat jenis kegagalan (*fault*) utama yang dibahas:
- **Transient Fault**: Kegagalan yang bersifat sementara dan tidak berulang secara konstan.
- **Intermittent Fault**: Kegagalan yang muncul, hilang, dan berulang secara berkala.
- **Permanent Fault**: Kegagalan yang bersifat tetap dan memerlukan perbaikan atau penggantian komponen fisik/logika.
- **Byzantine Fault**: Kegagalan paling kompleks di mana komponen memberikan hasil yang tidak konsisten, saling bertentangan, atau bahkan bersifat manipulatif/tidak dapat dipercaya.

---

## 4. Klasifikasi Fault Berdasarkan Sumber
Berdasarkan sumber penyebabnya, *fault* dibagi menjadi tiga kategori:
- **Hardware Faults**: Kerusakan atau masalah pada perangkat keras, seperti *disk crash*, kerusakan RAM, atau *power failure*.
- **Software Faults**: Kesalahan pada perangkat lunak, seperti *bugs*, *memory leak*, dan *race condition*.
- **Communication Faults**: Gangguan pada jaringan komunikasi, seperti *packet loss*, *latency* tinggi, dan *network partition*.

---

## 5. Teknik untuk Mencapai Fault Tolerance
Beberapa teknik dan strategi yang dapat diterapkan untuk membangun sistem yang tahan banting:

### a. Redundansi dan Replikasi
Menyediakan beberapa salinan sumber daya atau data pada *node* yang berbeda agar sistem tetap berjalan lancar ketika salah satu *node* mengalami kegagalan.

### b. Load Balancing
Membagi beban kerja secara merata ke beberapa *instance* aplikasi menggunakan *load balancer* populer seperti **HAProxy** dan **Nginx**.

### c. Checkpointing dan Rollback Recovery
- **Checkpointing**: Proses menyimpan status (*state*) sistem secara berkala ke media penyimpanan aman.
- **Rollback Recovery**: Mekanisme untuk mengembalikan sistem ke kondisi *checkpoint* terakhir yang valid ketika terjadi kegagalan fatal.

### d. Heartbeat dan Failure Detection
- **Heartbeat**: Sinyal pengingat/status yang dikirim secara berkala oleh suatu komponen untuk menunjukkan bahwa dirinya masih aktif.
- **Failure Detection**: Mekanisme untuk mendeteksi apakah suatu komponen atau *node* mengalami kegagalan saat *heartbeat* berhenti diterima.

### e. Retry Mechanism
Mencoba kembali suatu proses atau permintaan secara otomatis apabila terjadi kegagalan koneksi sesaat. Salah satu *library* populer untuk ini adalah **Tenacity** (Python).

### f. Circuit Breaker
Pola desain (*design pattern*) yang digunakan untuk mencegah kegagalan berantai (*cascading failure*) pada arsitektur *microservices*.

**Tiga status utama dalam Circuit Breaker:**
1. **Closed**: Permintaan dari klien diizinkan lewat sepenuhnya dan tingkat kegagalan dipantau.
2. **Open**: Permintaan langsung ditolak sementara karena layanan terdeteksi mengalami kegagalan (*fail-fast*).
3. **Half-Open**: Beberapa permintaan uji coba diizinkan lewat untuk memeriksa apakah layanan target sudah pulih sepenuhnya.

---

## 6. Consensus dan Coordination
- **Consensus**: Proses ketika beberapa *node* terdistribusi mencapai kesepakatan mutlak terhadap suatu nilai, status, atau urutan operasi tertentu.
- **Coordination**: Proses mengatur interaksi dan sinkronisasi antar-*node* agar dapat bekerja sama secara efektif.

> **Contoh Penerapan:**  
> Pemilihan *leader* pada *database*, sinkronisasi pembaruan file pada *cloud storage*, serta validasi transaksi pada jaringan *blockchain*.

---

## 7. Actor Model
**Actor Model** merupakan pendekatan paradigma pemrograman di mana *Actor* bertindak sebagai unit komputasi independen terkecil. Setiap *actor* menjalankan tugas dan berkomunikasi secara eksklusif melalui pengiriman pesan (*message passing*). 

Model ini sangat handal untuk melakukan supervisi proses, termasuk mendeteksi serta menangani kegagalan secara otomatis (*let-it-crash philosophy*).

---

## 8. Implementasi Fault Tolerance pada Berbagai Teknologi
Beberapa bahasa pemrograman dan *library* yang mendukung implementasi *fault tolerance*:

- **Erlang & Elixir**: Memiliki bawaan *Actor Model* dan arsitektur *Supervisor-Worker* yang sangat tangguh.
- **Pony**: Bahasa pemrograman berorientasi performa tinggi yang berfokus penuh pada *Actor Model*.
- **Python**: Menggunakan *library* seperti **Xoscar**, **Tenacity**, dan **Circuit Breaker**.
- **Java**: Menggunakan kerangka kerja seperti **Apache Pekko** dan **Resilience4j**.

---

> **Kesimpulan Modul 5**  
> *Fault Tolerance* merupakan kemampuan esensial yang wajib dimiliki oleh sistem terdistribusi agar tetap andal melayani pengguna meskipun terjadi gangguan pada komponennya. Melalui penerapan redundansi, replikasi, *load balancing*, *checkpointing*, *heartbeat*, hingga *circuit breaker*, sistem mampu meminimalkan dampak gangguan serta menjaga ketersediaan layanan secara optimal.
