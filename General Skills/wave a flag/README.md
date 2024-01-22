# Wave a flag
- Link: https://play.picoctf.org/practice/challenge/170?category=5&page=1

## Tantangan
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm) has extraordinarily helpful information...

## Penyelesaian
- Download file task
```sh
wget https://mercury.picoctf.net/static/a00f554b16385d9970dae424f66ee1ab/warm
```


- Tambahkan permission execute pada file `warm`
```sh
chmod +x warm
```

- Eksekusi file `warm`
```sh
./warm
```

- Terdapat pesan untuk menggunakan opsi `-h`
```sh
./warm -h
```


- Flag
```sh
picoCTF{b1scu1ts_4nd_gr4vy_18788aaa}
```