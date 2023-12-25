# tunn3l v1s10n
- Link: https://play.picoctf.org/practice/challenge/112?category=4&page=1

## Tantangan
We found this [file](https://mercury.picoctf.net/static/d0129ad98ba9258ab59e7700a1b18c14/tunn3l_v1s10n). Recover the flag.

## Penyelesaian
- Download file task
```sh
wget https://mercury.picoctf.net/static/5eb456e480e485183c9c1b16952c6eda/dolls.jpg
```

- Format file tersebut belum diketahui sehingga kita tidak dapat membacanya 
```sh
file tunn3l_v1s10n
```

- Sekarang kita coba analisis file tersebut dengan tool `hexeditor`. Disini terdapat karakter `BM` yang menandakan file tersebut sebanarnya adalah file bitmap dengan ekstensi `.bmp`
```sh
hexeditor tunn3l_v1s10n
```

- Berdasarkan informasi di https://asecuritysite.com/forensics/bmp?file=router.bmp Karakteristik file bitmap adalah sebagai berikut
	- Byte 1 dan 2 harus bernilai: 42 4D
	- Byte 3 hingga 6 adalah ukuran file: 8E 26 2C 00
	- Byte 7 hingga 10 harus bernilai: 00 00 00 00





