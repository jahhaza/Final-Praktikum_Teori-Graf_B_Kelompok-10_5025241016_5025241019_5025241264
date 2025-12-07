|             Name                   |    NRP     |      
|------------------------------------|------------|
| Farrel Hasudungan Immanuel Limbong | 5025241016 | 
| Jahhaza Assiqooyah Nurul Hidayah   | 5025241019 | 
| Muhammad Hilman Azhar              | 5025241264 | 


# Praktikum 1 : 🐴 The Knight’s Tour 

## Deskripsi

**Knight’s Tour** merupakan permasalahan klasik dalam permainan **catur** dimana sebuah **bidak kuda** harus melakukan perjalanan mengunjungi **setiap petak papan catur tepat satu kali** dengan pola pergerakan sesuai aturan kuda.

Pada praktikum ini diberikan ketentuan:

- Bidak kuda ditempatkan pada sembarang petak awal pada papan **8 x 8**
- Kuda harus melakukan perjalanan sampai **seluruh 64 petak telah dikunjungi**
- Terdapat dua situasi akhir perjalanan:
  1. **Open Tour** yaitu perjalanan dapat berakhir di sembarang kotak
  2. **Closed Tour** yaitu perjalanan harus ditutup pada petak yang **dapat menyerang petak awal** (artinya langkah terakhir kuda masih dapat kembali ke posisi awal)

Program harus menampilkan **urutan langkah** perjalanan kuda seperti pada contoh yang diberikan di soal.

---

## 🎯 Tujuan Program

Program ini bertujuan untuk:

- Mengimplementasikan **algoritma Knight’s Tour**
- Menghasilkan jalur lengkap (64 langkah) baik dalam bentuk:
  - **Closed Tour**
  - **Open Tour**
- Menampilkan hasil rute dalam bentuk **papan numerik** urutan kunjungan kuda

---

## Konsep & Algoritma yang Digunakan

Program ini menggunakan heuristik **Warnsdorff’s Rule**, yaitu memilih langkah berikutnya berdasarkan:

> *“Selalu pilih kotak berikutnya yang memiliki jumlah kemungkinan gerakan lanjutan paling sedikit.”*

Langkah penting:
1. Cek apakah kotak tujuan valid dan belum dikunjungi
2. Hitung **degree** (jumlah langkah potensial berikutnya)
3. Pilih kotak dengan **degree minimum**
4. Ulangi hingga semua petak terisi
5. Cek apakah langkah terakhir masih bisa menyerang titik awal → **Closed Tour**

Jika gagal, dilakukan percobaan ulang hingga batas tertentu.

---

