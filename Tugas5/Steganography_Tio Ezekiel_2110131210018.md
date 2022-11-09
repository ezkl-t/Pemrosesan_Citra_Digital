# Steganography

Steganografi adalah sebuah metode dalam pemrosesan citra digital untuk menyembunyikan suatu data rahasia ke dalam sebuah citra.

Data yang disembunyikan dapat berupa:

- Gambar
- Teks
- Suara, dll

Adapun langkah-langkah yang dilakukan dalam menerapkan metode steganografi adalah:

1. Ubah citra warna ke dalam citra grayscale.

2. Ubah pesan yang akan disisipkan ke dalam bentuk biner.

3. Cek untuk setiap piksel yang ada pada citra, dan lakukan:

- Ambil nilai LSB pada citra

- Ambil nilai bit pesan yang akan disisipkan

- Jika nilai sama, tambahkan 0 ke dalam citra output, jika tidak tambahkan 1.

4. Simpan gambar.

Mari kita praktikkan pada Octave dengan source code seperti berikut:

```
clear;
clc;

% load citra dan ambil ukurannya (width dan height)
img = imread('lofi.jpg');
cover_img = rgb2gray(img);
[img_height, img_width] = size(cover_img);

# mengubah pesan ke dalam bentuk biner
pesan = "Tio Ezekiel 2110131210018";

# menggunakan fungsi uint8
ascii_pesan = uint8(pesan);  # u artinya unsigned angka tidak negatif. int8 karena citra sampai 255 yang mana 2^8

% mengambil nilai biner dari pesan
biner_pesan = dec2bin(ascii_pesan, 8);
biner_pesan = str2num(biner_pesan);

# mengubah biner pesan ke dalam betuk 1 baris
transpose_pesan = transpose(biner_pesan);
trans_pesan = transpose_pesan(:);

trans_hasil = transpose(trans_pesan);
panjang = length(trans_hasil);


counter = 1;

# copy cover ke citra hasil;
stego_img = cover_img;

for i = 1:img_height
  for y = 1:img_width
    if (counter <= panjang)
      LSB = bitget(cover_img(x,y),1);
      biner_pesan_sekarang = trans_hasil(counter);
      temp = xor(LSB, biner_pesan_sekarang);
      stego_img(x,y) = cover_img(x,y) + temp;

      counter = counter + 1;

    else
      break;

    endif
  endfor
endfor

# simpan gambar
imwrite(stego_img, "stego.png");
```

Berikut adalah gambar yang akan digunakan pada source code steganography di atas:

<p align="center"><img src="img/lofi.jpg" width=75%></p>

Dan berikut adalah gambar yang telah diproses menggunakan source code steganography tadi:

<p align="center"><img src="img/stego.png" width=75%></p>

Kasat mata tidak terdapat perubahan karena perubahan hanyar terjadi di bit yang mengalami perubahan yakni pada Least Significant Bit. Jika kita ambil LSB nya maka dapat terlihat sebuah perubahan yang merupakan penambahan penulisan dari pesan rahasia yang sudah kita masukkan yaitu berupa nama dan NIM.