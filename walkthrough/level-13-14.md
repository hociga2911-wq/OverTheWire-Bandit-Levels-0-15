# Bandit Level 13 → Level 14

## 1. Objective

The password for `bandit14` is readable only by user `bandit14`. Instead of a password, the level provides an SSH private key.

## 2. Step-by-Step Solution

```bash
ls
```

You should find:

```text
sshkey.private
```

Use the key to authenticate as `bandit14` on localhost:

```bash
ssh -i sshkey.private bandit14@localhost -p 2220
```

If SSH asks whether you trust the host key, enter:

```text
yes
```

Once logged in as `bandit14`:

```bash
cat /etc/bandit_pass/bandit14
```

This reveals the password needed for the next transition.

Then exit the nested session:

```bash
exit
```

And connect normally:

```bash
ssh bandit14@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- SSH public-key authentication\n- private keys\n- localhost\n- file permissions\n- nested SSH sessions.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-13-14.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
