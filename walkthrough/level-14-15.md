# Bandit Level 14 → Level 15

## 1. Objective

Retrieve the next password by sending the current password to TCP port 30000 on localhost.

## 2. Step-by-Step Solution

First confirm the current user's password:

```bash
cat /etc/bandit_pass/bandit14
```

Send it to the local service with netcat:

```bash
echo "YOUR_BANDIT14_PASSWORD" | nc localhost 30000
```

A successful response returns the password for `bandit15`.

You can also use an interactive connection:

```bash
nc localhost 30000
```

Then paste the current password and press Enter.

Finally:

```bash
ssh bandit15@bandit.labs.overthewire.org -p 2220
```


## 3. Explanation

The main idea is to use the information given by the challenge to narrow down the correct file, data representation, authentication method, or network service. The commands above are intentionally shown in the order they should be executed.

## 4. Key Concepts Learned

- TCP\n- localhost\n- ports\n- netcat (`nc`)\n- pipes\n- standard input/output.

## 5. Result

**Status:** Completed.

**Password obtained:** Do not publish the password in GitHub. Save it privately in your own notes if needed.

## 6. Evidence

Add your screenshot here:

`../screenshots/level-14-15.png`

## 7. Next Level

Use the password obtained from the terminal to authenticate to the next Bandit user on SSH port `2220`.

---
