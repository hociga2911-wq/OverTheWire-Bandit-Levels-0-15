# Bandit Level 4 → Level 5

## 1. Objective

The password is in the only human-readable file inside `inhere`.

## 2. Step-by-Step Solution

```bash
cd inhere
file ./*
```


Most files will be identified as `data`; one will be identified as `ASCII text`.

Read the ASCII text file. In the standard layout it is:

```bash
cat ./-file07
```

The `./` prefix prevents the filename beginning with `-` from being treated as an option.


<img width="774" height="287" alt="image" src="https://github.com/user-attachments/assets/f73f4fb8-418a-442c-8f22-c44fdd8b6145" />



Then:

```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
```


<img width="1003" height="346" alt="image" src="https://github.com/user-attachments/assets/bfdecfc2-cf61-4e98-b219-246d787475a2" />




## 3. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
