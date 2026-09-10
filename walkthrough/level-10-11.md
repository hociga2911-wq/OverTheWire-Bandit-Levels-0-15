# Bandit Level 10 → Level 11

## 1. Objective

The password is stored in `data.txt` as Base64-encoded data.

## 2. Step-by-Step Solution

```bash
base64 -d data.txt
```

Alternative:

```bash
cat data.txt | base64 -d
```

The decoded output contains the password for `bandit11`.

Then:

```bash
ssh bandit11@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- Base64 encoding/decoding\n- command-line decoding\n- standard input/output.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-10-11.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
