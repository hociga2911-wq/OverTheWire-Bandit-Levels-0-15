# Bandit Level 8 → Level 9

## 1. Objective

Find the only line in `data.txt` that occurs exactly once.

## 2. Step-by-Step Solution

```bash
sort data.txt | uniq -u
```

Why two commands?

1. `sort` groups identical lines together.
2. `uniq -u` prints lines that occur only once.
3. `|` sends the output of `sort` into `uniq`.

Then:

```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- Pipes\n- sorting\n- duplicate detection\n- `sort`\n- `uniq`.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-08-09.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
