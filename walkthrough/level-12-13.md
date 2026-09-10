# Bandit Level 12 → Level 13

## 1. Objective

`data.txt` is a hexdump of a file that has been compressed repeatedly using different formats.

## 2. Step-by-Step Solution

Use a temporary directory because the home directory is not the right place for repeated extraction:

```bash
mktemp -d
```

<img width="616" height="137" alt="image" src="https://github.com/user-attachments/assets/0ef7d095-9014-431b-8a96-e8bb7e5324f2" />


Copy the path printed by the command, then:

```bash
cd /tmp/<your-directory>
cp ~/data.txt .
mv data.txt new.txt
ls
xxd -r new.txt binary
ls
```

<img width="911" height="220" alt="image" src="https://github.com/user-attachments/assets/afd12f48-f6f7-45fe-91a8-33867c3eac7a" />


Now repeatedly identify the format with `file` and decompress it.

Typical sequence in the current standard Bandit layout:

```bash
mv binary binary.gz
gzip -d binary.gz
file binary

mv binary binary.bz2
bzip2 -d binary.bz2
file binary

mv binary binary.gz
gzip -d binary.gz
file binary


tar -xf binary
ls
file data5.bin


tar -xf data5.bin
ls
file data6.bin

tar -xf data6.bin
ls

tar -xf data8.bin
ls
file data8.bin

mv data8.bin data8.gz
gzip -d data8.gz
file data8

cat data8
```


<img width="1818" height="777" alt="image" src="https://github.com/user-attachments/assets/c46a47f3-30ca-4370-9353-e9b54605ed7c" />



Important: do not blindly guess the next format. After every extraction, use `file` and choose the decompression tool that matches the detected format.



<img width="1731" height="757" alt="image" src="https://github.com/user-attachments/assets/236d017b-2a91-47df-b748-2df6988e7539" />



Then:

```bash
ssh bandit13@bandit.labs.overthewire.org -p 2220
```

<img width="1082" height="384" alt="image" src="https://github.com/user-attachments/assets/f276328e-05aa-4b6e-b9c4-34b94a2b8bba" />




## 3. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
