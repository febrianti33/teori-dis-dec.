# RANGKUMAN  SISTEM TERDISTRIBUSI DAN TERDESENTRALISASI
## Modul 6:Distributed File System

- **Nama:** Maria Widya Febrianti
- **NIM:** 255410011
- **Kelas:** IF-1
- **Program Studi:** Informatika
- **Universitas:** Universitas Teknologi Digital Indonesia (UTDI) Yogyakarta
- # MODUL 6 – Distributed File System
- Promt:buatkan saya ringkasan atau rangkuman dari  modul 6 di atas(pakai AI GPT)
- Promt:tolong ubah format ini ke bentuk format markdown README.md.md GitHub (pakai Gemini AI)
- # MODUL 6 – Distributed File System

## 1. Pengertian File System
**File System** merupakan metode dan struktur data yang digunakan sistem operasi untuk mengelola, mengatur, serta melacak file pada media penyimpanan seperti *harddisk*, SSD, dan USB *flashdisk*.

**Contoh File System berdasarkan Sistem Operasi:**
- **Linux**: `ext4`, `XFS`, `Btrfs`
- **Windows**: `FAT16`, `FAT32`, `NTFS`
- **macOS**: `APFS`

*File System* bekerja melalui *driver* yang dikelola oleh *kernel* sehingga berbagai aplikasi dapat membaca dan menulis data ke media penyimpanan.

---

## 2. Pengertian Distributed File System (DFS)
**Distributed File System (DFS)** merupakan sistem file yang menggabungkan beberapa media penyimpanan dari komputer yang berbeda menjadi satu sistem penyimpanan terintegrasi. 

Meskipun data secara fisik disimpan tersebar pada beberapa komputer (*node*), pengguna dapat melihat dan mengaksesnya seolah-olah berada pada satu media penyimpanan lokal yang utuh.

**Tujuan utama DFS:**
- Mengelola penyimpanan data secara terdistribusi.
- Meningkatkan keandalan (*reliability*) dan ketersediaan data.
- Memberikan kinerja (*throughput*) akses yang tinggi.

---

## 3. Perbedaan DAS, DFS, NAS, dan SAN

| Teknologi | Kepanjangan | Penjelasan & Karakteristik |
| :--- | :--- | :--- |
| **DAS** | *Direct-Attached Storage* | Media penyimpanan yang terhubung secara langsung ke satu komputer tanpa melalui jaringan. |
| **DFS** | *Distributed File System* | Sistem file yang mengelola dan menyatukan kapasitas penyimpanan dari beberapa *node* menjadi satu kesatuan logis. |
| **NAS** | *Network-Attached Storage* | Perangkat penyimpanan khusus yang menyediakan akses data berbasis file (*file-level*) melalui jaringan. |
| **SAN** | *Storage Area Network* | Jaringan berkecepatan tinggi khusus yang menyediakan akses penyimpanan dalam bentuk *block-level storage*. |

---

## 4. Jenis-Jenis Distributed File System
Beberapa implementasi DFS yang umum digunakan dalam skala industri:
- **Google File System (GFS)**
- **Colossus** (penerus GFS)
- **CephFS**
- **GlusterFS**
- **HDFS** (*Hadoop Distributed File System*)
- **Lustre**

---

## 5. Hadoop Distributed File System (HDFS)
**HDFS** merupakan *file system* terdistribusi yang bersifat *open source*, *scalable*, dan *fault-tolerant*. HDFS dirancang khusus untuk menyimpan serta mengelola kumpulan data berukuran sangat besar (*Big Data*) pada klaster komputer atau server komoditas. HDFS adalah salah satu komponen inti dari ekosistem **Apache Hadoop**.

**Cara kerja HDFS secara umum:**
1. File yang akan disimpan dipecah menjadi beberapa **blok** (*data blocks*) berukuran besar.
2. Blok-blok data tersebut didistribusikan ke berbagai server penyimpanan (*DataNode*).
3. Sistem secara otomatis membuat dan menyimpan salinan blok melalui proses **replikasi** ke *node* lain.
4. Data dapat diakses atau diproses kembali secara paralel melalui ekosistem Hadoop.

Dengan mekanisme tersebut, HDFS mampu menangani penyimpanan berskala *petabyte* sekaligus menjamin ketersediaan data meskipun terjadi kegagalan pada salah satu server.

---

## 6. Pengertian Cloud Storage
**Cloud Storage** merupakan layanan penyimpanan data secara daring (*online*) yang memungkinkan pengguna menyimpan, mengelola, dan mengakses data melalui jaringan internet. Data tidak disimpan pada perangkat lokal pengguna, melainkan dikelola oleh penyedia layanan *cloud* pada pusat data (*data center*) terdistribusi.

**Contoh penyedia layanan:**
- **Amazon S3** (*Simple Storage Service*)
- **Azure Blob Storage**
- **Google Cloud Storage (GCS)**

---

## 7. Hubungan Cloud Storage dengan DFS
*Cloud Storage* berperan sebagai lapisan penyimpanan fisik/infrastruktur tempat data berada, sedangkan **DFS** dapat digunakan sebagai lapisan abstraksi untuk mengatur dan mengelola pemrosesan data tersebut.

> **Contoh Penerapan:**  
> **Amazon S3** dapat digunakan sebagai media penyimpanan utama yang diakses dan dikelola secara langsung oleh **HDFS** (melalui konektor seperti `s3a`) untuk kebutuhan pemrosesan analitik data besar.

---

## 8. Jenis-Jenis Cloud Storage
Terdapat tiga arsitektur utama dalam layanan *cloud storage*:

- **Object Storage**: Menyimpan data sebagai unit objek independen yang dilengkapi identitas unik (*unique ID*) dan metadata lengkap.
- **File Storage**: Menyimpan data secara hierarkis dalam bentuk struktur file dan folder/direktori tradisional.
- **Block Storage**: Memecah data menjadi blok-blok berukuran tetap (*volumes*) yang dapat dipasang layaknya *harddisk* terpisah pada server virtual.

---

> **Kesimpulan Modul 6**  
> *Distributed File System* memungkinkan penyimpanan dan pengelolaan data dilakukan secara terpadu pada banyak komputer yang saling terhubung. Contoh nyatanya adalah **HDFS** pada Apache Hadoop yang dirancang untuk menangani *Big Data*. Di samping itu, kehadiran **Cloud Storage** semakin mempermudah penyimpanan serta akses data berskala global melalui jaringan internet.

---
---

# RANGKUMAN KESELURUHAN MODUL 1–6

Secara keseluruhan, keenam modul tersebut membahas konsep fundamental sistem terdistribusi hingga penerapannya dalam pengelolaan data dan penyimpanan modern.

| Modul | Materi Utama | Inti Pembahasan |
| :---: | :--- | :--- |
| **1** | **Pengenalan Sistem Terdistribusi** | Konsep dasar, arsitektur, karakteristik, desentralisasi, dan Teorema CAP |
| **2** | **Proses dan Komunikasi Antar Proses** | Manajemen proses, IPC, *Message Passing*, RPC, dan *Middleware* |
| **3** | **Sinkronisasi dan Koordinasi** | Sinkronisasi waktu fisik & logis (*Logical Clock*), *Mutual Exclusion*, dan pemilihan koordinator |
| **4** | **Konsistensi dan Replikasi** | Model konsistensi, *trade-off* CAP, serta arsitektur & strategi replikasi data |
| **5** | **Fault Tolerance** | Klasifikasi *fault* dan teknik mitigasi kegagalan (*redundancy*, *heartbeat*, *circuit breaker*, dll.) |
| **6** | **Distributed File System** | Konsep *File System*, arsitektur penyimpanan (DAS/NAS/SAN/DFS), HDFS, dan *Cloud Storage* |

---

> ### Kesimpulan Akhir
> Berdasarkan keenam modul yang telah dipelajari, dapat disimpulkan bahwa **sistem terdistribusi** merupakan fondasi teknologi yang memungkinkan banyak komputer independen bekerja sama sebagai satu kesatuan sistem yang utuh. Dalam penerapannya, sistem terdistribusi membutuhkan komunikasi antarproses yang andal, sinkronisasi yang presisi, penjagaan konsistensi data, serta mekanisme penanganan kegagalan (*fault tolerance*) agar layanan tetap berjalan optimal.
>
> Penggunaan teknik replikasi dan *Distributed File System* terbukti mampu meningkatkan ketersediaan sekaligus keandalan penyimpanan data berskala masif. Salah satu implementasi nyatanya adalah **Apache Hadoop dengan HDFS** yang sanggup menyimpan dan mengelola data dalam jumlah besar secara terdistribusi. Dengan memahami seluruh konsep ini, kita dapat mengerti cara kerja di balik berbagai layanan modern seperti *cloud computing*, media sosial, sistem perbankan digital, hingga aplikasi berbasis internet skala global.
