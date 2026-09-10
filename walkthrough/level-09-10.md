# Bandit Level 9 → Level 10

## 1. Objective

Find one of the few human-readable strings in `data.txt` that is preceded by several `=` characters.

## 2. Step-by-Step Solution

```bash
strings data.txt | grep "="
```

`strings` extracts printable character sequences from binary/non-text data. `grep` then filters the output for lines containing `=`.

If the output contains several candidates, inspect the entries with multiple `=` characters and identify the password line.

Then:

```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- Printable strings\n- binary-data inspection\n- `strings`\n- filtering with `grep`.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-09-10.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
