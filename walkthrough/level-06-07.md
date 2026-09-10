# Bandit Level 6 → Level 7

## 1. Objective

Find a file anywhere on the server that is owned by user `bandit7`, owned by group `bandit6`, and exactly 33 bytes.

## 2. Step-by-Step Solution

Use ls to list the files but there is no file found.


<img width="301" height="34" alt="image" src="https://github.com/user-attachments/assets/35270775-0d5f-4b35-9092-71fdf68327bf" />



For this level they already told that the file will be in the user `bandit7`, owned by group `bandit6`, and exactly 33 bytes. So we use the below syntax.



```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

The `2>/dev/null` redirects permission-denied errors away from the terminal.

Read the path returned by `find`. In the standard layout:

```bash
cat /var/lib/dpkg/info/bandit7.password
```


<img width="1076" height="79" alt="image" src="https://github.com/user-attachments/assets/0687f52f-9167-47a5-8ea3-2a1fd3d0644c" />


After read the path we get a password to enter next level.

Then:

Enter the password to enter next level.


```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
```


<img width="871" height="366" alt="image" src="https://github.com/user-attachments/assets/b403bbf7-2727-4adc-9b03-2109821560b8" />




## 3. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
