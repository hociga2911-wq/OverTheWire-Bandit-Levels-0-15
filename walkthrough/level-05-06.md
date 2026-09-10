# Bandit Level 5 → Level 6

## 1. Objective

Find a file under `inhere` that is human-readable, exactly 1033 bytes, and not executable.

## 2. Step-by-Step Solution

After entering into level 5. Use ls for listing files.There is a inhere directory. Enter into it using cd command. Inside the inhere directory there will be many directory.

<img width="1918" height="170" alt="image" src="https://github.com/user-attachments/assets/dbfc59b9-783d-40e1-86b8-ef15ea8563ed" />



```bash
find inhere -type f -size 1033c 
```

By using the above syntax, we can easily find out a particular directory with particular file.


<img width="641" height="55" alt="image" src="https://github.com/user-attachments/assets/364963b3-36d6-44b6-bb2d-a25b9586becb" />




Read the matching file. In the standard layout:

Using the cat command we can easily find out the password in the particular directory in particular file.

```bash
cat inhere/maybehere07/.file2
```

<img width="638" height="29" alt="image" src="https://github.com/user-attachments/assets/75c91583-bcf3-4d78-a1b3-12f83b2a9819" />


Then:

Using the password enter into next level.


```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
```

<img width="901" height="362" alt="image" src="https://github.com/user-attachments/assets/d96289ab-eb6a-4a13-9f0f-8f544442f566" />



## 3. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
