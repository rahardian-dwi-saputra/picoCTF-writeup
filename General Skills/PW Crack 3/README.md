# PW Crack 3
- Link: https://play.picoctf.org/practice/challenge/247?category=5&page=2

## Tantangan
Can you crack the password to get the flag?
Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.
There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## Penyelesaian
- Unduh password checker diatas
```sh
wget https://artifacts.picoctf.net/c/16/level3.py
```


- Unduh flag yang terenkripsi
```sh
wget https://artifacts.picoctf.net/c/16/level3.flag.txt.enc
```


- Unduh hash
```sh
wget https://artifacts.picoctf.net/c/16/level3.hash.bin
```


- Gunakan text editor seperti mousepad untuk membuka script `level3.py`. Disini kita menambahkan function baru untuk melakukan brute force dan menemukan password yang cocok untuk mendekrip flag. Kemudian memindahkan pemanggilan function password check ke baris paling akhir setelah melakukan brute force. Ubah script `level3.py` menjadi sebagai berikut
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

flag_enc = open('level3.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level3.hash.bin', 'rb').read()


def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


def level_3_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")






# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]

def print_pw():
    for p in pos_pw_list:
        check = hash_pw(p)
        if( check == correct_pw_hash):
            print("Valid password : ",p)
            break
            
print_pw()
level_3_pw_check()

```
- Jalankan script `level3.py` diatas dengan `python3` lalu masukkan password yang ditampilkan
```sh
python3 level3.py
```

- Flag
```sh
picoCTF{m45h_fl1ng1ng_2b072a90}
```