# Struktur-Data
# Sistem Sederhana Pengelolaan Nilai Mahasiswa

Repositori ini berisi implementasi sistem sederhana untuk mengelola nilai mahasiswa menggunakan struktur data *array* (atau *list* dalam Python), dilengkapi dengan fitur analisis statistik dasar dan visualisasi data menggunakan Matplotlib.

---

## 1. Penjelasan Konsep Array



Dalam ilmu komputer, **Array** adalah sebuah struktur data yang digunakan untuk menyimpan sekumpulan elemen data (biasanya dengan tipe data yang sama) secara berurutan di dalam memori komputer. 

Dalam bahasa pemrograman Python, implementasi *array* yang paling umum digunakan adalah **List**. Berikut adalah beberapa karakteristik utama *array/list* yang diterapkan pada program ini:
* **Indeksing:** Setiap elemen dalam *array* memiliki posisi atau indeks yang dimulai dari `0`. Misalnya, nilai mahasiswa pertama disimpan pada indeks `0`, nilai kedua pada indeks `1`, dan seterusnya.
* **Dinamis:** Di Python, *list* bersifat dinamis, artinya kita bisa menambahkan data baru kapan saja (menggunakan metode `.append()`) tanpa harus menentukan ukuran maksimalnya sejak awal.
* **Penyimpanan Kolektif:** Alih-alih membuat 10 variabel berbeda untuk menyimpan 10 nilai mahasiswa (seperti `nilai1`, `nilai2`, dst.), kita cukup menggunakan satu variabel `nilai_mahasiswa` yang menampung seluruh nilai tersebut.

---

## 2. Analisis Kompleksitas

Berikut adalah analisis *Time Complexity* (kompleksitas waktu) untuk setiap operasi utama dalam skrip `1_Soal_01.ipynb`, dengan asumsi $n$ adalah jumlah data di dalam *array* (dalam kasus ini $n = 10$):

* **Input Nilai (Perulangan):** $O(n)$
  Program melakukan iterasi sebanyak $n$ kali untuk menerima input pengguna. Operasi penambahan data ke dalam *array* (`.append()`) berjalan dalam waktu konstan $O(1)$.
* **Mencari Nilai Tertinggi (`max()`) & Terendah (`min()`):** $O(n)$
  Fungsi bawaan Python ini harus memindai seluruh elemen *array* dari awal hingga akhir untuk membandingkan dan menemukan nilai ekstrem.
* **Menghitung Rata-rata (`sum() / len()`):** $O(n)$
  Fungsi `sum()` melakukan iterasi ke seluruh elemen untuk menjumlahkannya secara kumulatif. Fungsi `len()` berjalan dalam $O(1)$. Total kompleksitas adalah $O(n)$.
* **Menghitung Jumlah Kelulusan:** $O(n)$
  Operasi pengecekan kondisi (`>= 60`) memindai setiap elemen dalam *array* satu per satu sebanyak $n$ kali.
* **Membuat Grafik Matplotlib:** $O(1)$
  Proses *rendering* grafik pada kasus ini memproses titik data yang sudah diagregasi (seperti nilai max/min dan jumlah lulus/gagal), sehingga waktu eksekusinya relatif konstan dan tidak bergantung pada panjang *array* awal $n$.

---

## 3. Refleksi Pembelajaran

Melalui pengerjaan tugas ini, saya mendapatkan beberapa pelajaran penting:
1. **Pemahaman Struktur Data:** Saya menjadi lebih paham bagaimana *array/list* sangat menyederhanakan proses pengumpulan dan pengelolaan banyak data dibandingkan menggunakan variabel tunggal.
2. **Validasi Input:** Saya belajar pentingnya menangani *error* (menggunakan `try-except`) untuk memastikan program tidak *crash* jika pengguna memasukkan tipe data yang salah, serta memastikan nilai berada di rentang yang logis (0-100).
3. **Visualisasi Data:** Mengubah angka mentah menjadi grafik (diagram batang dan diagram lingkaran) menggunakan Matplotlib membuat hasil analisis jauh lebih mudah dipahami secara visual.
4. **Efisiensi Algoritma:** Melalui analisis kompleksitas, saya menyadari bahwa sebagian besar operasi statistik dasar pada *array* membutuhkan waktu sebanding dengan jumlah datanya ($O(n)$), yang mana masih sangat efisien untuk jumlah data yang kecil hingga menengah.

## 4. Screenshot hasil eksekusi
<img width="1138" height="773" alt="image" src="https://github.com/user-attachments/assets/037eca75-a541-47d0-af7a-defa1bebc064" />
<img width="1201" height="790" alt="image" src="https://github.com/user-attachments/assets/d631553c-46ee-47ca-aa46-9373ca81ba28" />


