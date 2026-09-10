# Bandit Level 7 → Level 8

## 1. Objective

The password is stored in `data.txt` next to the word `millionth`.

## 2. Step-by-Step Solution

```bash
grep "millionth" data.txt
```

`grep` searches the file for the specified pattern and prints the matching line.

Then:

```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- Pattern searching\n- `grep`\n- text filtering.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-07-08.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
