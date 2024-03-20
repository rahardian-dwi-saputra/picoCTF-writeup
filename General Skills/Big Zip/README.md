# Big Zip
- Link: https://play.picoctf.org/practice/challenge/322?category=5&page=3

## Tantangan
Unzip this archive and find the flag.
- [Download zip file](https://artifacts.picoctf.net/c/504/big-zip-files.zip)

## Penyelesaian
- Unduh file zip diatas
```sh
wget https://artifacts.picoctf.net/c/504/big-zip-files.zip
```


- Ekstrak file zip yang sudah diunduh
```sh
unzip big-zip-files.zip
```

- Sekarang kita cari flag menggunakan `grep`
```sh
grep -r pico big-zip-files 
```

- Flag
```sh
picoCTF{gr3p_15_m4g1c_ef8790dc}
```