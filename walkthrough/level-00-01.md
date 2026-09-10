# Bandit Level 0 → Level 1

## 1. Objective

Log in to the Bandit server using SSH. The password for Level 1 is stored in a file named `readme` in the home directory.

## 2. Step-by-Step Solution

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls
cat readme
```
The `cat readme` command displays the password for `bandit1`.

Then connect to the next level:

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- SSH\n- remote login\n- non-default SSH port\n- `ls`\n- `cat`.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-00-01.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
