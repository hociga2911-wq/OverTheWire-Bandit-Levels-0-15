# Bandit Level 14 → Level 15

## 1. Objective

Retrieve the next password by sending the current password to TCP port 30000 on localhost.

## 2. Step-by-Step Solution

First confirm the current user's password:

```bash
cat /etc/bandit_pass/bandit14
```


```bash
nc localhost 30000
```


<img width="526" height="117" alt="image" src="https://github.com/user-attachments/assets/263301c2-f931-412b-baf8-a0520c91db1c" />



Then paste the current password and press Enter.


Finally:

Enter the password that already.find out in above step.


```bash
ssh bandit15@bandit.labs.overthewire.org -p 2220
```


<img width="949" height="411" alt="image" src="https://github.com/user-attachments/assets/bf07b0ad-4bc7-421b-9804-eab82d73d7d0" />




## 3. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
