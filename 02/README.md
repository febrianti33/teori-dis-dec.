# RANGKUMAN  SISTEM TERDISTRIBUSI DAN TERDESENTRALISASI
## Modul 2: Proses dan Komunikasi Antar Proses pada Sistem Terdistribusi

- **Nama:** Maria Widya Febrianti
- **NIM:** 255410011
- **Kelas:** IF-1
- **Program Studi:** Informatika
- **Universitas:** Universitas Teknologi Digital Indonesia (UTDI) Yogyakarta
- # MODUL 2 – Proses dan Komunikasi Antar Proses pada Sistem Terdistribusi
- Promt:buatkan saya ringkasan atau rangkuman dari  modul 2 di atas(pakai AI GPT)
- Promt:tolong ubah format ini ke bentuk format markdown REDMI.md GitHub (pakai Gemini AI)
- # MODUL 2 – Proses dan Komunikasi Antar Proses pada Sistem Terdistribusi

## 1. Pengertian Proses
**Proses** merupakan program yang sedang dijalankan oleh sistem operasi. Dalam sistem terdistribusi, setiap *node* dapat menjalankan proses yang berbeda dan saling berkomunikasi untuk menyelesaikan suatu pekerjaan secara bersama-sama.

---

## 2. Manajemen Proses
Manajemen proses dalam sistem terdistribusi mencakup beberapa kegiatan utama:

* **Process Creation**: Membuat atau menjalankan proses baru.
* **Process Migration**: Memindahkan proses yang sedang berjalan dari satu komputer ke komputer lain.
* **Process Monitoring**: Memantau kinerja dan status proses agar berjalan sesuai kebutuhan.

---

## 3. Komunikasi pada Sistem Terdistribusi
Komunikasi sangat diperlukan karena setiap komputer dalam sistem terdistribusi bekerja secara independen. Agar dapat beroperasi sebagai satu kesatuan, setiap *node* harus saling bertukar informasi.

**Contoh penerapan:**
Aplikasi seperti **Gojek** dan **Grab** yang menghubungkan berbagai proses secara *real-time*—mulai dari pemesanan oleh pengguna, pencarian *driver*, pelacakan lokasi, hingga perhitungan biaya perjalanan.

---

## 4. Model Komunikasi Pesan
Terdapat tiga model utama dalam komunikasi berbasis pesan:

| Model Komunikasi | Deskripsi |
| :--- | :--- |
| **Komunikasi Langsung** | Proses saling berkomunikasi secara langsung menggunakan *socket*. |
| **Komunikasi Tidak Langsung** | Pesan dikirim dan diterima melalui perantara seperti *mailbox* atau *message queue*. |
| **Publish/Subscribe (Pub/Sub)** | Pengirim (*publisher*) mengirimkan pesan ke suatu topik, dan penerima (*subscriber*) yang berlangganan pada topik tersebut akan menerima pesannya. |

---

## 5. Inter-Process Communication (IPC)
**IPC** merupakan mekanisme pertukaran data atau komunikasi antarproses. Terdapat empat jenis IPC utama yang dibahas:

1. **Shared Memory**
2. **Message Passing**
3. **Remote Procedure Call (RPC)**
4. **Middleware**

> **Catatan:** *Shared memory* kurang cocok diterapkan pada sistem terdistribusi karena proses-proses yang berjalan pada komputer yang berbeda tidak memiliki akses langsung ke ruang memori fisik yang sama.

---

## 6. Message Passing
**Message Passing** merupakan metode komunikasi antarproses dengan cara mengirim dan menerima pesan secara eksplisit. Salah satu standar populer yang digunakan pada metode ini adalah **MPI (*Message Passing Interface*)**.

---

## 7. Remote Procedure Call (RPC)
**RPC** merupakan mekanisme yang memungkinkan suatu program memanggil fungsi atau prosedur yang berada di komputer lain seolah-olah fungsi tersebut dijalankan secara lokal. 

* **Contoh teknologi:** **gRPC**

---

## 8. Message-Oriented Middleware (MOM)
**MOM** merupakan infrastruktur perangkat lunak yang memfasilitasi aplikasi terdistribusi untuk saling berkomunikasi menggunakan pesan. Pengiriman dan penerimaan pesan pada MOM umumnya dilakukan secara **asinkron**.

**Protokol yang umum digunakan pada MOM:**
- **AMQP** (*Advanced Message Queuing Protocol*)
- **MQTT** (*Message Queuing Telemetry Transport*)
- **DDS** (*Data Distribution Service*)
- **XMPP** (*Extensible Messaging and Presence Protocol*)
- **XATMI**

---

## 9. Komunikasi Sinkron dan Asinkron
Perbedaan cara kerja pengiriman pesan berdasarkan waktu tunggu respons:

- **Sinkron (*Synchronous*)**: Pengirim harus menunggu respons dari penerima (*blocking*) sebelum dapat melanjutkan proses berikutnya.
- **Asinkron (*Asynchronous*)**: Pengirim dapat langsung melanjutkan pekerjaan lain tanpa harus menunggu penerima selesai memproses pesan (*non-blocking*).

---

## 10. Masalah Komunikasi Antarproses
Beberapa tantangan utama yang sering terjadi dalam komunikasi antarproses meliputi:

* **Reliability**: Memastikan pesan berhasil dikirim dan diterima dengan utuh tanpa hilang.
* **Ordering**: Memastikan urutan pengiriman dan penerimaan pesan tetap benar.
* **Security**: Menjaga kerahasiaan dan integritas komunikasi menggunakan enkripsi serta autentikasi.
* **Performance**: Memperhatikan faktor *latency* (waktu tunda) dan kapasitas *bandwidth*.

**Protokol komunikasi yang sering digunakan:**
`TCP` • `UDP` • `HTTP` • `REST` • `GraphQL` • `gRPC`

---

> **Kesimpulan Modul 2**  
> Komunikasi antarproses merupakan bagian fundamental dalam sistem terdistribusi karena setiap komputer harus saling bertukar informasi. Dengan memanfaatkan **IPC**, **Message Passing**, **RPC**, dan **Middleware**, proses komunikasi dapat berjalan lebih teratur, efisien, serta mampu mendukung arsitektur aplikasi modern seperti *microservices*.
