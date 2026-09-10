# Bandit Level 11 → Level 12

## 1. Objective

The password in `data.txt` has been transformed using ROT13.

## 2. Step-by-Step Solution

Using ls command to list the files and sort command is used to rearrange of text in a file.


```bash
sort data.txt
```


<img width="759" height="139" alt="image" src="https://github.com/user-attachments/assets/d50affe5-5354-4d52-a6f8-0f878eddc1b9" />



`tr` maps each letter to the letter 13 positions away. ROT13 is a substitution cipher, not encryption.


<img width="885" height="41" alt="image" src="https://github.com/user-attachments/assets/2194596c-cc50-4f66-bac4-a9a460a48ae3" />


The  required password is obtained.


Then:

Use the password to enter next level.

```bash
ssh bandit12@bandit.labs.overthewire.org -p 2220
```


<img width="1109" height="475" alt="image" src="https://github.com/user-attachments/assets/24831e99-704b-49fc-a5f9-55dbbeea155b" />



## 3. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
