# Bandit Level 9 → Level 10

## 1. Objective

Find one of the few human-readable strings in `data.txt` that is preceded by several `=` characters.

## 2. Step-by-Step Solution

Use ls to list the files.


<img width="416" height="62" alt="image" src="https://github.com/user-attachments/assets/8098b7e4-a65e-4e5d-9a73-de2d7e5fbfe9" />


"data.txt" is a binary data.

`strings` extracts printable character sequences from binary/non-text data. 


```bash
strings data.txt 
```


<img width="553" height="38" alt="image" src="https://github.com/user-attachments/assets/820e7424-b8a8-4024-918b-db75ad5c20ff" />




If the output contains several candidates, inspect the entries with multiple `=` characters and identify the password line.


Then:

Using the password enter into next level.

```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
```

<img width="1054" height="447" alt="image" src="https://github.com/user-attachments/assets/8d1d168c-2ffa-4aac-81d5-5f54956ae57b" />




## 3. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
