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

```PROGRAM: Sistem Transaksi dan Validasi Toko Buku Modern

DEKLARASI:  
 is_member: Boolen   
 jumlah_buku: Integer  
 total_awal: Real  
 persen_diskon: Real  
 nominal_diskon: Real   
 total_diskon: Real  

 DESKRIPSI:    
     INPUT (total_awal)  
     INPUT (jumlah_buku)   
  
     WHILE (total_awal < 0) OR (jumlah_buku < 1) DO  
            OUTPUT ("ERROR: Input tidak valid, silahkan input ulang")   
            INPUT (total_awal)     
            INPUT (jumlah_buku) 
     ENDWHILE
  
     INPUT(is_member)
  
     IF (is_member = True) THEN     
         IF (total_awal >= 200000) AND (jumlah_buku >= 3) THEN    
             nominal_diskon <- 15
        ENDIF   
    ELSE  
        IF (total_awal > 300000) THEN  
            nominal_diskon <- 0.05  
        ELSE  
            nominal_diskon <- 0.0 
        ENDIF    
 ENDIF 
 
 nominal_diskon <- total_awal (persentase_diskon)          
 total_bayar <- total_awal - nominal_diskon



 OUTPUT: nominal_diskon 
 OUTPUT: total_bayar
```




# 3. Trace Table

**Kasus A**

Input: `is_member = True`, `total_awal = 250000`, `jumlah_buku = 4`
| Langkah | `is_member` | `total_awal` | `jumlah_buku` | `persen_diskon` | `nominal_diskon` | `total_bayar` |
|---|---|---|---|---|---|---|
| Input | True | 250000 | 4 | - | - | - |
| Validasi member | True | 250000 | 4 | 10% | - | - |
| Status member | True | 250000 | 4 | 15% | - | - |
| Hitung nominal diskon | True | 250000 | 4 | 15% | 37500 | - |
| Hitung total bayar | True | 250000 | 4 | 15% | 37500 | 212500 |

Output: **`nominal diskon`**: 37500,  **`total_bayar`**: 250000-37500 : 212500

**Kasus B**

Input: `is_member = False`, `total_awal = 350000`, `jumlah_buku = 2`
| No. | `is_member` | `total_awal` | `jumlah_buku` | `persen_diskon` | `nominal_diskon` | `total_bayar` |
|---|---|---|---|---|---|---|
| Input | False | 350000 | 2 | - | - | - |
| Validasi member| False | 350000 | 2 | 5% | - | - |
| Status member dan diskon | False | 350000 | 2 | 5% | - | - |
| Hitung nominal diskon | False | 350000 | 2 | 5% | 17500 | - |
| Hitung total bayar | False | 350000 | 2 | 5% | 17500 | 332500 |

Output: **`nominal diskon`**: 17500,  **`total_bayar`**: 350000-17500 : 332500

**Kasus C**

Input: `is_member = False`, `total_awal = -50000`, `jumlah_buku = 1`

| No. | `is_member` | `total_awal` | `jumlah_buku` | `persen_diskon` | `nominal_diskon` | `total_bayar` |
|---|---|---|---|---|---|---|
| Input | False | -50000 | 1 | - | - | - |
| Cek validasi dan input ulang | False | -50000 | 1 | - | - | - |
| Input data yang benar | False | 10000 | 1 | - | - | - |
| Cek syarat diskon tidak terpenuhi | False | 10000 | 1 | 0% | 10000 | - |
| Hitung total bayar | False | 10000 | 1 | 0% | - | 10000 |

Output: **`nominal diskon`**: 0,  **`total_bayar`**: 100000-0 : 100000











       


