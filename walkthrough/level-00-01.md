# Bandit Level 0 → Level 1

## 1. Objective

Log in to the Bandit server using SSH. The password for Level 1 is stored in a file named `readme` in the home directory.

## 2. Step-by-Step Solution

# Step 1 

The first step is to connect to Bandit Server using ssh

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

# Step 2 – List the Files

After logging in, the next step is to check what files are available in the current directory.

Use:

ls

<img width="346" height="55" alt="image" src="https://github.com/user-attachments/assets/818e00b2-8950-42b0-a51b-d3448be5ddf9" />


## Command Explanation

ls stands for list.

It is used to display the files and directories in the current working directory.

Example:

bandit0@bandit:~$ ls
readme

The output shows:

readme

This means that a file named readme exists in the current directory.

Why did we use ls?

We do not know the exact location or name of the file containing the next password.

Therefore, we first inspect the current directory using ls.

# Step 3 – Read the readme File

After finding the readme file, we need to read its contents.

Use:

cat readme

<img width="1116" height="162" alt="image" src="https://github.com/user-attachments/assets/47cfb0fe-9a8e-4f43-a0ef-f6a19aea7215" />


## Command Explanation

cat is a Linux command used to display the contents of a file directly in the terminal.


The cat command reads and displays the contents of a file.

readme

readme is the name of the file we found using the ls command.

Therefore:

cat readme

means:

Display the contents of the readme file.

The output contains the password required for Bandit Level 1.

# Step 4 - Exit the Bandit0

Exit the Bandit0 using exit command

<img width="610" height="80" alt="image" src="https://github.com/user-attachments/assets/fe0ec7fa-30f1-41e4-904a-33f1a1da211a" />

Then connect to the next level:

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.


## 4. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.



## 5. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.
Then connect to the next level:

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

---
