# Bandit Level 13 → Level 14

## 1. Objective

The password for `bandit14` is readable only by user `bandit14`. Instead of a password, the level provides an SSH private key.

## 2. Step-by-Step Solution

Use ls for list the file:


```bash
ls
```

<img width="378" height="61" alt="image" src="https://github.com/user-attachments/assets/dce98830-c2bf-401c-a90c-2677eb6c9a84" />



You should find:

```text
sshkey.private
```

Use the key to authenticate as `bandit14` on localhost:



```bash
scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .
```


<img width="1430" height="205" alt="image" src="https://github.com/user-attachments/assets/5e93dc12-1b6e-4e00-bc40-5d2c4e0f20d1" />




If SSH asks whether you trust the host key, enter:

```text
yes
```

<img width="1760" height="393" alt="image" src="https://github.com/user-attachments/assets/dce6770f-e0b5-458b-abe5-75e69617a2ac" />



The chmod command modifies the read,write and execute permissions of files or directory to control which users can access them.



<img width="1081" height="426" alt="image" src="https://github.com/user-attachments/assets/b8142a81-9cec-4ddb-99a6-328cff996888" />




Once logged in as `bandit14`:

```bash
cat /etc/bandit_pass/bandit14
```




<img width="686" height="88" alt="image" src="https://github.com/user-attachments/assets/b4a33805-4ad5-44af-a9a2-a2a5020019ac" />



This reveals the password needed for the next transition.

Then exit the nested session:

```bash
exit
```

And connect normally:

```bash
ssh bandit14@bandit.labs.overthewire.org -p 2220
```



## 3. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
