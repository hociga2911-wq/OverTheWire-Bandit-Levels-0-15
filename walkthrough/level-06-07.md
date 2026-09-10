# Bandit Level 6 → Level 7

## 1. Objective

Find a file anywhere on the server that is owned by user `bandit7`, owned by group `bandit6`, and exactly 33 bytes.

## 2. Step-by-Step Solution

```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

The `2>/dev/null` redirects permission-denied errors away from the terminal.

Read the path returned by `find`. In the standard layout:

```bash
cat /var/lib/dpkg/info/bandit7.password
```

Then:

```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- Filesystem-wide search\n- ownership\n- groups\n- byte-size filtering\n- stderr redirection.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-06-07.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
