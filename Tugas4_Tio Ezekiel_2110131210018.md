># Pseudocode Algoritma Patterning

- Nilai matriks 0 - 25, maka grey level = 0
- Nilai matriks 26 - 51, maka grey level = 1
- Nilai matriks 52 - 77, maka grey level = 2
- Nilai matriks 78 - 103, maka grey level = 3
- Nilai matriks 104 - 129, maka grey level = 4
- Nilai matriks 130 - 155, maka grey level = 5
- Nilai matriks 156 - 181, maka grey level = 6
- Nilai matriks 182 - 207, maka grey level = 7
- Nilai matriks 208 - 233, maka grey level = 8
- Nilai matriks 234 - 256, maka grey level = 9

># Pseudocode Algoritma Dithering

- Matriks dither membandingkan dengan matriks thresholdnya. Apabila melebihi threshold maka piksel berwarna putih atau hitam jika kurang dari threshold.

Atau dapat ditentukan menggunakan kode algoritma seperti di bawah ini

```
for  all x & y do
      if f(x,y) > m(x,y) then
            g(x,y) = white
      else 
            g(x,y) = black
      end if
End for

```

># Pseudocode Algoritma Histogram Equalization

**1)** Cari run sum dari jumlah piksel.

**2)** Bagi tiap jumlah piksel dengan hasil terbesar dari run sum tadi.

**3)** Hasil dari langkah kedua dikalikan dengan graylevel terbesar kemudian hasilnya dibulatkan.

># Pseudocode Algoritma Bit Plane Slicing

**1)** Konversikan satu persatu tiap nilai desimal matriks ke dalam bilangan biner.

**2)** Menentukan Least Significant Bit (LSB) dan Most Significant Bit (MSB) adalah dengan melihat urutannya. Semakin ke kiri semakin signifikan bit tersebut (MSB), semakin ke kanan maka semakin kurang signifikan bit tersebut (LSB)

