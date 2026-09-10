# Bandit Level 5 → Level 6

## 1. Objective

Find a file under `inhere` that is human-readable, exactly 1033 bytes, and not executable.

## 2. Step-by-Step Solution

```bash
find inhere -type f -size 1033c ! -executable
```

A more informative version is:

```bash
find inhere -type f -size 1033c ! -executable -exec file {} \;
```

Read the matching file. In the standard layout:

```bash
cat inhere/maybehere07/.file2
```

Then:

```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- `find`\n- file size filters\n- executable permissions\n- recursive searching.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-05-06.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
