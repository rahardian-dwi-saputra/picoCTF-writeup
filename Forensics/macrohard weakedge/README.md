# MacroHard WeakEdge
- Link: https://play.picoctf.org/practice/challenge/44?category=4&page=1

## Tantangan
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/9a7436948cc502e9cacf5bc84d2cccb5/Forensics%20is%20fun.pptm)

## Penyelesaian
- Download file task
```sh
wget https://mercury.picoctf.net/static/9a7436948cc502e9cacf5bc84d2cccb5/Forensics%20is%20fun.pptm
```

- Copy dan ubah file `Forensics is fun.pptm` menjadi zip file
```sh
cp 'Forensics is fun.pptm' 'Forensics is fun.zip'
```

- Unzip ke dalam satu folder
```sh
unzip 'Forensics is fun.zip' -d 'Forensics is fun'
```

- Tampilkan semua isi list file dan tekan `q` untuk keluar
```sh
ls -alR 'Forensics is fun' | more
```

- Di folder `Forensics is fun/ppt/slideMasters` ditemukan file `hidden`

- Jika dibuka file tersebut berisi kumpulan karakter yang dipisahkan dengan spasi
```sh
cat 'Forensics is fun/ppt/slideMasters/hidden'
```

- Edit file `hidden` dengan menggunakan vi editor
```sh
vi 'Forensics is fun/ppt/slideMasters/hidden'
```

- Ketik `:s/ //g` dan tekan enter untuk menghilangkan tanda spasi

- Ketik `:wq` untuk menyimpan dan keluar dari vi editor

- Tampilkan kembali isi file `hidden` dan copy teks tersebut
```sh
cat 'Forensics is fun/ppt/slideMasters/hidden'
```

- Decode teks tersebut menggunakan base64 dengan tool Cyber Chef https://gchq.github.io/CyberChef/


- Flag
```sh
picoCTF{D1d_u_kn0w_ppts_r_z1p5}
```