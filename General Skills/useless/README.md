# useless
- Link: https://play.picoctf.org/practice/challenge/384?category=5&page=3

## Tantangan
There's an interesting script in the user's home directory
Additional details will be available after launching your challenge instance.

## Penyelesaian
- Tekan tombol **Launch Instance** untuk memulai tantangan


- Setelah instance berjalan, konek ke SSH server sesuai petunjuk soal. Jika diminta konfirmasi ketik yes lalu enter kemudian masukkan password yang tertera setelah Launch Instance
```sh
ssh picoplayer@saturn.picoctf.net -p 62990
```


- Setelah berhasil login, ketik `ls` untuk melihat daftar file yang tersedia. Disini terdapat file bash `useless`. Jika kita jalankan muncul pesan `Read the code first`
```sh
ls
./useless
```

- Selanjutnya kita buka isi file `useless`
```sh
cat useless
```



- Setelah kita buka isi file `useless` kita tahu cara menjalankan bash script tersebut dengan cara sebagai berikut
```sh
./useless add 2 3
./useless mul 4 5
./useless div 2 3
```



- Selain cara menjalankan bash script tersebut, di script tersebut juga terdapat pesan untuk membaca manual penggunaan script tersebut. Untuk membuka user manual, kita bisa melakukan dengan perintah berikut
```sh
man useless
```


- Flag
```sh
picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_6140}
```