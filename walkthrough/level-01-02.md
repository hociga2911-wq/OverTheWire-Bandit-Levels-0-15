# Bandit Level 1 → Level 2

## 1. Objective

The password is stored in a file named `-` in the home directory.

## 2. Step-by-Step Solution

```bash
ls
cat ./-
```
<img width="290" height="59" alt="image" src="https://github.com/user-attachments/assets/c7a7bf8c-907e-4960-be2f-c1aa3f380be0" />

<img width="340" height="35" alt="image" src="https://github.com/user-attachments/assets/bcaf2cf8-03de-4d6b-8e9c-213ac98de371" />


The `./` prefix is important because `-` can otherwise be interpreted as an option.
We get a password to unlock level 2.

Then:

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```

<img width="939" height="348" alt="image" src="https://github.com/user-attachments/assets/2565ff3e-b1b3-4870-a88d-9e196df639e9" />


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.



## 4. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.



## 5. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
