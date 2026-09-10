# Bandit Level 12 → Level 13

## 1. Objective

`data.txt` is a hexdump of a file that has been compressed repeatedly using different formats.

## 2. Step-by-Step Solution

Use a temporary directory because the home directory is not the right place for repeated extraction:

```bash
mktemp -d
```

Copy the path printed by the command, then:

```bash
cd /tmp/<your-directory>
cp ~/data.txt .
xxd -r data.txt > data
file data
```

Now repeatedly identify the format with `file` and decompress it.

Typical sequence in the current standard Bandit layout:

```bash
mv data data.gz
gzip -d data.gz
file data

mv data data.bz2
bzip2 -d data.bz2
file data

mv data data.gz
gzip -d data.gz
file data

mv data data.tar
tar -xf data.tar
file data5.bin

mv data5.bin data5.tar
tar -xf data5.tar
file data6.bin

mv data6.bin data6.bz2
bzip2 -d data6.bz2
file data6

mv data6 data6.tar
tar -xf data6.tar
file data8.bin

mv data8.bin data8.gz
gzip -d data8.gz
file data8

cat data8
```

Important: do not blindly guess the next format. After every extraction, use `file` and choose the decompression tool that matches the detected format.

Then:

```bash
ssh bandit13@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- Hexdumps\n- `xxd -r`\n- gzip\n- bzip2\n- tar\n- file identification\n- temporary workspaces.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-12-13.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
