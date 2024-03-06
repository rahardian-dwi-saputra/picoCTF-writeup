# Tab, Tab, Attack
- Link: https://play.picoctf.org/practice/challenge/176?category=5&page=1

## Tantangan
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip)

## Penyelesaian
- Download file `Addadshashanammu.zip` yang terlampir disoal
```sh
wget https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip
```


- Unzip file `Addadshashanammu.zip`
```sh
unzip Addadshashanammu.zip
```

- Setelah proses ekstrak berhasil terdapat file binary `fang-of-haynekhtnamet` yang berada di dalam path folder `Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku`
- Sekarang kita coba eksekusi file binary tersebut dan kita berhasil mendapatkan
```sh
./Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet
```


- Flag
```sh
picoCTF{l3v3l_up!_t4k3_4_r35t!_d32e018c}
```