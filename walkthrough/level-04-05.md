# Bandit Level 4 → Level 5

## 1. Objective

The password is in the only human-readable file inside `inhere`.

## 2. Step-by-Step Solution

```bash
cd inhere
file ./*
```

Most files will be identified as `data`; one will be identified as `ASCII text`.

Read the ASCII text file. In the standard layout it is:

```bash
cat ./-file07
```

The `./` prefix prevents the filename beginning with `-` from being treated as an option.

Then:

```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- File-type identification\n- ASCII text\n- binary data\n- wildcards\n- `file`.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-04-05.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
