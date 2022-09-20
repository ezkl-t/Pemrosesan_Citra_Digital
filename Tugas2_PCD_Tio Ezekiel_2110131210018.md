**Tio Ezekiel | 2110131210018 | Tugas 2 PCD**

># Eksplorasi Layer Pada Gambar

Ada 3 layer utama pada sebuah gambar. Yaitu Red (merah), Green (hijau), dan Blue (biru) atau sering juga dikenal dengan RGB.

Untuk mengambil layer warna dari sebuah gambar dengan Octave dapat digunakan code berikut:

```
Red     = 0 * img; R(:,:,1) = img(:,:,1); # Untuk warna merah
Green   = 0 * img; G(:,:,2) = img(:,:,2); # Untuk warna hijau
Blue    = 0 * img; B(:,:,3) = img(:,:,3); # Untuk warna biru
```

Berikut adalah hasil eksplorasi saya dalam mengambil ketiga layer warna pada sebuah gambar.

============================================================================================

Gambar yang saya gunakan berukuran 32x32 seperti ini: ![gambar emoji 32x32](/img/sus.png)

Berikut screenshot Editor Octave:

<p align="center"><img src="img/editor1.png" width=45%></p>

Dan berikut hasil kode sudah dijalankan:

<p align="center"><img src="img/editor2.png" width=45%></p>

># Fungsi imread, imshow, imhist

## 1. imread

imread adalah method untuk memuat gambar dari file yang ditentukan. Method ini digunakan untuk membaca citra menjadi sebuah data matriks.


Berikut adalah screenshot di Command Windows Octave ketika imread dijalankan pada gambar 32x32 tadi.
<p align="center"><img src="img/imread.png" width=45%></p>

## 2. imshow

imshow menampilkan gambar dengan cara membaca data matriks pada sebuah gambar dan menampilkannya secara visual.

Berikut adalah screenshot di Command Windows Octave ketika imshow dijalankan pada gambar 32x32.

<p align="center"><img src="img/imshow.png" width=45%></p>

## 3. imhist

Singkatnya imhist menghitung intensitas grayscale pada matriks yang telah dibaca oleh imread tadi menjadi sebuah histogram.

Berikut adalah screenshot di Command Windows Octave ketika imhist dijalankan pada gambar 32x32 tadi.

<p align="center"><img src="img/imhist.png" width=45%></p>