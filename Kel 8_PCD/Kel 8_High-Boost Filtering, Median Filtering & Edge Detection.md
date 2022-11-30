## Anggota Kelompok 8
1. Ana Maria Parasanti (2110131320009)
2. Ferzy Triwarsana Putra (2110131310003)
3. Tio Ezekiel (2110131210018)

---
# Penerapan High-Boost Filtering, Median Filtering & Edge Detection

>## High-Boost Filtering Dengan Function Bawaan Octave

```
% memuat citra awal
img = imread('CitraP6.jfif');

% merubah ke skala keabuan
img = rgb2gray(img);

% fungsi untuk membuat gaussian filtering
G = fspecial('gaussian',5,2.5);

% fungsi untuk memblurkan gambar
img_blur = imfilter(img,G);

% untuk mengurangi buram pada gambar
diff_img = img - img_blur;

highboost_img = img + diff_img;

% menampilkan output
subplot(2,2,1); imshow(img); title('Citra awal')
subplot(2,2,2); imshow(img_blur); title('Citra buram')
subplot(2,2,3); imshow(output); title('Citra hasil dari highboost filter');
```
## Hasilnya:

<img width="960" alt="highboostFunction" src="https://user-images.githubusercontent.com/112605121/204825673-69e6ad25-ed14-4cee-a8b8-b3df82e16bec.PNG">

>## Median Filtering Dengan Function Bawaan Octave
```

```

## Hasilnya:


>## Edge Detection Dengan Function Bawaan Octave
```

```

## Hasilnya:


>## High-Boost Filtering Tanpa Function Octave

```
% Memuat citra awal
awal = imread('CitraP6.jfif');

% Merubah ke skala keabuan
Img = rgb2gray(awal);

% Memberi noise (derau) pada citra
A = imnoise(Img,'Gaussian',0.04,0.003);

I = double(A);

% Desain Kernel Gaussian
% Deviasi Standar
sigma = 1.76;
% Ukuran jendela
sz = 4;
[x,y]=meshgrid(-sz:sz,-sz:sz);

M = size(x,1)-1;
N = size(y,1)-1;
Exp_comp = -(x.^2+y.^2)/(2*sigma*sigma);
Kernel = exp(Exp_comp)/(2*pi*sigma*sigma);

Simpan = zeros(size(I));

I = padarray(I,[sz sz]);

% Konvolusi
for i = 1:size(I,1)-M
    for j =1:size(I,2)-N
        Temp = I(i:i+M,j:j+M).*Kernel;
        Simpan(i,j)=sum(Temp(:));
    end
end

% Citra setelah gaussian filter (buram)
Simpan = uint8(Simpan);

% Penerapan highboost
% Untuk mengurangi buram pada gambar
diff = Img - output;

% Menambahkan perbedaan pada gambar aslinya
hasil = Img + diff;

% Menampilkan gambar
subplot(2,2,1),imshow(Img);title('Citra awal')
subplot(2,2,2),imshow(Simpan);title('Citra buram')
subplot(2,2,3),imshow(hasil);title('Citra hasil dari highboost filter')
```

## Hasilnya:

<img width="960" alt="highboostManual" src="https://user-images.githubusercontent.com/112605121/204826817-d781159b-4f52-4eb4-82d7-c8475e74bef7.PNG">

>## Median Filtering Tanpa Function Octave

```

```

## Hasilnya:


>## Edge Detection Tanpa Function Octave

```

```

## Hasilnya:



---
