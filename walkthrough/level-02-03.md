# Bandit Level 2 → Level 3

## 1. Objective

The password is stored in a file whose name contains spaces: `--spaces in this filename--`.

## 2. Step-by-Step Solution

```bash
ls
cat "./--spaces in this filename--"
```

An alternative is:

```bash
cat -- "--spaces in this filename--"
```

The quotes keep the filename as one shell argument.

Then:

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- Quoting\n- escaping spaces\n- filenames beginning with `-`\n- shell argument parsing.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-02-03.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
