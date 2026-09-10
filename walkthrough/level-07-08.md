# Bandit Level 7 → Level 8

## 1. Objective

The password is stored in `data.txt` next to the word `millionth`.

## 2. Step-by-Step Solution

Use ls to list the file.


<img width="308" height="59" alt="image" src="https://github.com/user-attachments/assets/4d8bb6eb-8e6d-4a66-97da-fc6581f345d4" />


```bash
grep "millionth" data.txt
```

<img width="652" height="31" alt="image" src="https://github.com/user-attachments/assets/d5fbc5ef-3780-4d2b-8ef3-8b0bc76322a5" />


`grep` searches the file for the specified pattern and prints the matching line.

Then:


```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
```

<img width="1104" height="453" alt="image" src="https://github.com/user-attachments/assets/ddd8ed21-b539-465f-9862-26cbc06c9261" />



## 3. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
