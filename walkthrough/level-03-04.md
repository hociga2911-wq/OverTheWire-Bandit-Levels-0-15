# Bandit Level 3 → Level 4

## 1. Objective

The password is stored in a hidden file inside the `inhere` directory.

## 2. Step-by-Step Solution

First use ls for listing the files. It gives a inhere directory. Enter into a directory using cd directory name (inhere) command,then list the file using ls. But the directory has no files, it was hidden.

so use ls -la for showing hidden files.


```bash
ls
cd inhere
ls
ls -la
```

<img width="338" height="60" alt="image" src="https://github.com/user-attachments/assets/2892439a-ee31-42ed-959a-c724e5a73836" />


<img width="382" height="52" alt="image" src="https://github.com/user-attachments/assets/afa83a94-2ee9-4262-98a7-637511862091" />



`ls` does not normally show hidden files. `ls -la` reveals them.


<img width="1026" height="127" alt="image" src="https://github.com/user-attachments/assets/23f6696c-e1c1-46e6-8f48-7947581246e1" />



Read the hidden file shown by the listing. In the standard Bandit layout it is:

```bash
cat ./...Hiding-From-You
```

<img width="661" height="36" alt="image" src="https://github.com/user-attachments/assets/31264815-7576-4bcb-b2b2-187671cd9fec" />


We got a password to enter level 4.


Then:

```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
```

Enter the password to enter the level 4


<img width="845" height="366" alt="image" src="https://github.com/user-attachments/assets/bcae02cf-1d74-444f-a5a2-ba97ff3be005" />




## 3. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
