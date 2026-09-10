# Bandit Level 11 → Level 12

## 1. Objective

The password in `data.txt` has been transformed using ROT13.

## 2. Step-by-Step Solution

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

`tr` maps each letter to the letter 13 positions away. ROT13 is a substitution cipher, not encryption.

Then:

```bash
ssh bandit12@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- ROT13\n- substitution ciphers\n- character translation\n- `tr`.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-11-12.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
