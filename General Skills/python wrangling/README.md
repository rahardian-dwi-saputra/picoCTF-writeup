# Python Wrangling
- Link: https://play.picoctf.org/practice/challenge/166?category=5&page=1

## Tantangan
Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/ende.py) using [this password](https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/pw.txt) to get [the flag](https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/flag.txt.en)?

## Penyelesaian
- Download python script
```sh
wget https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/ende.py
```

- Download password
```sh
wget https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/pw.txt
```

- Download file flag
```sh
wget https://mercury.picoctf.net/static/1b247b1631eb377d9392bfa4871b2eb1/flag.txt.en
```

- Tampilkan isi file `pw.txt`
```sh
cat pw.txt 
```

- Jalankan program python yang sudah diunduh untuk mendekrip file `flag.txt.en`. Jika dimintai password masukkan isi file `pw.txt` diatas
```sh
python3 ende.py -d flag.txt.en
```

- Flag
```sh
picoCTF{4p0110_1n_7h3_h0us3_dbd1bea4}
```