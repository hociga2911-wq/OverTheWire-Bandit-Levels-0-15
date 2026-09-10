# Bandit Level 8 → Level 9

## 1. Objective

Find the only line in `data.txt` that occurs exactly once.

## 2. Step-by-Step Solution

Use ls to list the file.


<img width="482" height="73" alt="image" src="https://github.com/user-attachments/assets/eeb78e87-a75a-4725-86c8-85c1b69a892a" />


```bash
sort data.txt | uniq -u
```

<img width="700" height="40" alt="image" src="https://github.com/user-attachments/assets/8bcf8c27-f7da-45fe-a6fd-438285b3406e" />



Why two commands?

1. `sort` groups identical lines together.
2. `uniq -u` prints lines that occur only once.
3. `|` sends the output of `sort` into `uniq`.


Exit the level using exit command.


Then:

We will get a password after the above step. Using it enter into next level.


```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
```

<img width="1180" height="456" alt="image" src="https://github.com/user-attachments/assets/547fe639-2436-40d5-9652-d9c64e2c6089" />




## 3. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
