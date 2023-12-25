# Glory of the Garden
- Link: https://play.picoctf.org/practice/challenge/44?category=4&page=1

## Tantangan
This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.

## Penyelesaian
- Download file task
```sh
wget https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg
```

- Gunakan tool `strings` untuk menampilkan string yang terdapat dalam gambar. Pada bagian paling bawah terdapat informasi flag
```sh
strings garden.jpg
```

- Kita bisa menyeleksi string tersebut dengan perintah berikut
```sh
strings garden.jpg | grep -oE picoCTF{.*}
```


- Flag
```sh
picoCTF{more_than_m33ts_the_3y33dd2eEF5}
```