# Bandit Level 10 → Level 11

## 1. Objective

The password is stored in `data.txt` as Base64-encoded data.

## 2. Step-by-Step Solution

Using the ls command to list the files.


<img width="550" height="65" alt="image" src="https://github.com/user-attachments/assets/98a5db9e-4715-4d80-b423-9aa6296f1db7" />


The data.txt is a encoded file. we have to decode it. so we use the below command to decode it.


```bash
base64 -d data.txt
```

<img width="673" height="31" alt="image" src="https://github.com/user-attachments/assets/b202a70d-c63b-49eb-8bc4-05808ff3559b" />



Alternative:

```bash
cat data.txt | base64 -d
```

The decoded output contains the password for `bandit11`.


Then:

Use the password to enter to next level.


```bash
ssh bandit11@bandit.labs.overthewire.org -p 2220
```


<img width="1109" height="459" alt="image" src="https://github.com/user-attachments/assets/2a723eff-7580-4e8a-a587-90d617145010" />



## 3. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
