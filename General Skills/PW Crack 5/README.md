# PW Crack 5
- Link: https://play.picoctf.org/practice/challenge/249?category=5&page=3

## Tantangan
Can you crack the password to get the flag?
Download the password checker [here](https://artifacts.picoctf.net/c/31/level5.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/31/level5.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/31/level5.hash.bin) in the same directory too. Here's a [dictionary](https://artifacts.picoctf.net/c/31/dictionary.txt) with all possible passwords based on the password conventions we've seen so far.

## Penyelesaian
- Unduh password checker diatas
```sh
wget https://artifacts.picoctf.net/c/31/level5.py
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/PW%20Crack%205/assets/pw%20crack%201.JPG)

- Unduh flag yang terenkripsi
```sh
wget https://artifacts.picoctf.net/c/31/level5.flag.txt.enc
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/PW%20Crack%205/assets/pw%20crack%202.JPG)

- Unduh hash
```sh
wget https://artifacts.picoctf.net/c/31/level5.hash.bin
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/PW%20Crack%204/assets/pw%20crack%203.JPG)

- Unduh dictionary
```sh
wget https://artifacts.picoctf.net/c/31/dictionary.txt
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/PW%20Crack%205/assets/pw%20crack%204.JPG)

- Gunakan text editor seperti mousepad untuk membuka script `level5.py`. Disini kita menambahkan function baru untuk melakukan brute force dan menemukan password yang cocok di file `dictionary.txt` untuk mendekrip flag. Kemudian memindahkan pemanggilan function password check ke baris paling akhir setelah melakukan brute force. Ubah script `level5.py` menjadi sebagai berikut
```sh
import hashlib

### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level5.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level5.hash.bin', 'rb').read()


def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


def level_5_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")

def print_pw():
    with open('dictionary.txt','r') as file:
        for line in file:
            check = hash_pw(line.strip())
            if(check == correct_pw_hash):
                print("Valid password : ",line)
                break

print_pw()
level_5_pw_check()

```
- Jalankan script `level5.py` diatas dengan `python3` lalu masukkan password yang ditampilkan
```sh
python3 level5.py
```

![alt text](https://github.com/rahardian-dwi-saputra/picoCTF-writeup/blob/main/General%20Skills/PW%20Crack%205/assets/pw%20crack%205.JPG)

- Flag
```sh
picoCTF{h45h_sl1ng1ng_36e992a6}
```