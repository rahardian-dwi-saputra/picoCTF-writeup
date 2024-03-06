# Wave a flag
- Link: https://play.picoctf.org/practice/challenge/170?category=5&page=1

## Tantangan
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm) has extraordinarily helpful information...

## Penyelesaian
- Download file task
```sh
wget https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/wave%20a%20flag/assets/wave%20a%20flag%201.JPG)

- Tambahkan permission execute pada file `warm`
```sh
chmod +x warm
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/wave%20a%20flag/assets/wave%20a%20flag%202.JPG)

- Eksekusi file `warm`
```sh
./warm
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/wave%20a%20flag/assets/wave%20a%20flag%203.JPG)

- Terdapat pesan untuk menggunakan opsi `-h`
```sh
./warm -h
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/wave%20a%20flag/assets/wave%20a%20flag%204.JPG)

- Flag
```sh
picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}
```