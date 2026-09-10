# Bandit Level 2 → Level 3

## 1. Objective

The password is stored in a file whose name contains spaces: `--spaces in this filename--`.

## 2. Step-by-Step Solution

Use ls command for listing the files and use cat command for finding password


```bash
ls
cat "./--spaces in this filename--"
```

<img width="777" height="79" alt="image" src="https://github.com/user-attachments/assets/d9fb543d-aa62-4cf4-bec1-3632048f9574" />


An alternative is:

```bash
cat -- "--spaces in this filename--"
```

The quotes keep the filename as one shell argument.

Then:

Enter the password to enter the level 3

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

<img width="920" height="344" alt="image" src="https://github.com/user-attachments/assets/79c88784-c324-48e7-8256-ba2ae119f5fe" />



## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.


## 4. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.



## 5. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
