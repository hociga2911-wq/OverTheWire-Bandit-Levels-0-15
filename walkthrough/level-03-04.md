# Bandit Level 3 → Level 4

## 1. Objective

The password is stored in a hidden file inside the `inhere` directory.

## 2. Step-by-Step Solution

```bash
ls
cd inhere
ls
ls -la
```

`ls` does not normally show hidden files. `ls -la` reveals them.

Read the hidden file shown by the listing. In the standard Bandit layout it is:

```bash
cat ./...Hiding-From-You
```

Then:

```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- Hidden files\n- dot-prefix filenames\n- `ls -a`\n- `ls -l`\n- directory navigation.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-03-04.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
