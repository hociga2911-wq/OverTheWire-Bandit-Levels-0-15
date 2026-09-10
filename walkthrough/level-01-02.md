# Bandit Level 1 → Level 2

## 1. Objective

The password is stored in a file named `-` in the home directory.

## 2. Step-by-Step Solution

```bash
ls
cat ./-
```
The `./` prefix is important because `-` can otherwise be interpreted as an option.

Then:

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- Relative paths\n- special filenames\n- option parsing\n- `./`.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-01-02.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
