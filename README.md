# Tugas Mandiri Pertemuan 2

**Nama:** Nadisa Kusuma Chair

**Nim:** 1251170162

**Mata Kuliah:** Algoritma dan Struktur Data



# 1. Analisis Komponen
**A. Identifikasi Variabel dan Jenis Tipe Data**

| No. | Variabel | Tipe Data | Keterangan |
|---|---|---|---|
| 1 | is_member | Boolean | Menentukan status keanggotaan pelanggan (True/False) |
| 2 | jumlah_buku | Integer | Jumlah buku yang di beli |
| 3 | total_awal | Real | Total nominal belanja sebelum diskon |
| 4 | Persentase_diskon | Real | Persentase diskon yang berlaku |
| 5 | nominal_diskon | Real | Jumlah potongan harga dalam rupiah |
| 6 | total_bayar | Real | Total harga akhir yang harus di bayar setelah diskon |

**B. Struktur kontrol yang digunakan**

a). Sequence: Digunakan untuk menjalankan perintah dilakukan secara berurutan. Mulai dari input data, validasi, perhitungan diskon, perhitungan total bayar hingga diakhir output.

b). Selection: Digunakan untuk menentukan diskon berdasarkan status pelanggan, yaitu member atau non member.

c). Iteration: validasi input: di gunakan untuk mengulang permintaan input apabila data yang dimasukan belum valid, jika (`total_awal < 0`) atau (`jumlah_buku < 1`) pengguna diminta memasukan data kembali sampai data yang dimasukkan valid maka perulangan akan berhenti. 


---

# 2. Pseudocode

**PROGRAM: Sistem Transaksi dan Validasi Toko Buku Modern**

DEKLARASI:

 is_member: Boolen  
 jumlah_buku: Integer  
 total_awal: Real  
 persen_diskon: Real  
 nominal_diskon: Real   
 total_diskon: Real  

 DESKRIPSI
 :  
  INPUT (is_member)   
  INPUT (jumlah_buku)   
  INPUT (total_awal)   

 Validation loop
WHILE (`total_awal < 0 OR jumlah_buku < 1`) DO  
  OUTPUT ("ERROR: Input tidak valid.`total_awal harus > 0 dan jumlah_buku harus > 1`")
  INPUT (is_member)
  INPUT (jumlah_buku)
  INPUT (total_awal)
ENDWHILE
