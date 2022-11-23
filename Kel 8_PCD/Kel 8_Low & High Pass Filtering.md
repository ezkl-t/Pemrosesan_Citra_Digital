## Anggota Kelompok 8
1. Ana Maria Parasanti (2110131320009)
2. Ferzy Triwarsana Putra (2110131310003)
3. Tio Ezekiel (2110131210018)

---
# Low pass filtering
Proses filter yang melewatkan komponen citra dengan nilai intensitas yang rendah dan meredam komponen citra dengan nilai intensitas yang tinggi. digunakan untuk membuat citra menjadi lebih halus dan lebih blur. Efek pengaburan ini disebut dengan efek blurring.

Ciri-ciri Kernel Low Pass Filtering
* Jumlah semua elemen kernel bernilai satu. 
* Elemen kernel tidak ada yang bernilai negatif. 
* Tinggi dan lebar kernel sama.
* Bobot dalam kernel bersifat simetris terhadap piksel pusat. 

# High Pass Filtering
Proses filter yang mengambil citra dengan gradiasi intensitas yang tinggi dan perbedaan intensitas yang rendah akan dikurangi atau dibuang. High Pass Filtering adalah salah satu dari metode penajaman (sharpening).  Tujuan utama dari proses penajaman ini adalah untuk menyoroti detail-detail halus dalam gambar atau untuk meningkatkan detail yang telah dikaburkan baik dalam kesalahan atau efek alami dari proses akuisisi citra tertentu.

Aturan-aturan dalam high-pass filter
* Koefisien penapis boleh negatif, nol, ataupun bernillai positif.
* Total keseluruhan koefisiennya ialah bernilai 0 ataupun 1.
* Apabila jumlah koefisiennya berjumlah = 0, maka setiap elemen yang rendah frekuensinya nilainya akan menurun. 
* Namun, apabila total dari koefisien adalah = 1, maka elemen yang memiliki frekuensi rendah nilainya tetap sama dengan nilai semula.

# Penerapan Low Pass Filtering dan High Pass Filtering

>## Low Pass Filtering dan High Pass Filtering Dengan Function Bawaan Octave



>## Low Pass Filtering dan High Pass Filtering Tanpa Function Octave

## Kode Program

<p align="center"><img width="479" alt="low1" src="https://user-images.githubusercontent.com/112605121/203600635-eac4d070-306d-4a71-8085-78916110a58e.PNG"></p>

<p align="center"><img width="479" alt="low2" src="https://user-images.githubusercontent.com/112605121/203600681-1b7958fd-09bf-4f77-a3c0-f5c2ce9d54c6.PNG"></p>

## Hasilnya:

<p align="center"><img width="961" alt="low3" src="https://user-images.githubusercontent.com/112605121/203601078-bbdd171d-6ce0-4fdd-8d70-884870204462.PNG"></p>

---
