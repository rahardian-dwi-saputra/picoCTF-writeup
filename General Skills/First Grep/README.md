# First Grep
- Link: https://play.picoctf.org/practice/challenge/85?category=5&page=2

## Tantangan
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file)? This would be really tedious to look through manually, something tells me there is a better way.

## Penyelesaian
- Unduh lampiran file pada soal diatas
```sh
wget https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/First%20Grep/assets/first%20grep%201.JPG)

- Setelah berhasil diunduh, file tersebut berisi ASCII dan terdiri dari 4200 baris
```sh
file file
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/First%20Grep/assets/first%20grep%202.JPG)

- Karena isi file yang begitu panjang, kita perlu menbaca isi file lalu memfilternya untuk mencari flag
```sh
cat file | grep pico 
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/First%20Grep/assets/first%20grep%203.JPG)

- Flag
```sh
picoCTF{grep_is_good_to_find_things_5af9d829}
```