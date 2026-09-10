# OverTheWire Bandit — Levels 0 to 15

A beginner-friendly, step-by-step walkthrough of my progress through the **OverTheWire Bandit** wargame.

> **Scope:** Level 0 → Level 1 through Level 14 → Level 15 (15 completed transitions).

## About Bandit

Bandit is an introductory Linux/command-line wargame designed to teach the basics needed for other OverTheWire wargames. The official game explains that each level is completed by obtaining information needed to start the next level. 

Official website: https://overthewire.org/wargames/bandit/

## Environment

- Platform: OverTheWire Bandit
- Host: `bandit.labs.overthewire.org`
- SSH Port: `2220`
- Protocol: SSH
- Tools used: SSH, Linux shell commands, `grep`, `find`, `file`, `strings`, `sort`, `uniq`, `base64`, `tr`, `xxd`, `gzip`, `bzip2`, `tar`, SSH keys and `nc`

## Important Security Note

I intentionally **do not publish the passwords in this repository**. The official Bandit page notes that passwords can change and recommends keeping personal notes. Instead, this walkthrough shows the exact commands needed to retrieve each password during a live run.

This is also a good security practice: credentials should not be committed to a public Git repository.

## Level Progress

| Level | Main concept |
|---|---|
| 0 → 1 | SSH and reading a file |
| 1 → 2 | Special filename `-` |
| 2 → 3 | Spaces/special characters in filenames |
| 3 → 4 | Hidden files |
| 4 → 5 | `file` and human-readable data |
| 5 → 6 | `find`, size and permissions |
| 6 → 7 | Owner, group and filesystem-wide search |
| 7 → 8 | `grep` |
| 8 → 9 | `sort`, `uniq`, pipes |
| 9 → 10 | `strings` and binary data |
| 10 → 11 | Base64 decoding |
| 11 → 12 | ROT13 and `tr` |
| 12 → 13 | Hexdump + repeated compression |
| 13 → 14 | SSH private-key authentication |
| 14 → 15 | TCP, localhost, ports and netcat |

## Evidence / Screenshots

For a staff submission, I recommend adding one screenshot for each level showing:
1. the logged-in Bandit username,
2. the important command,
3. the successful result,
4. optionally the next SSH login.

Suggested names:

```text
screenshots/
├── level-00-01.png
├── level-01-02.png
├── level-02-03.png
...
└── level-14-15.png
```

## What I Learned

By completing these levels I practiced:

- Linux command-line navigation
- SSH authentication
- Linux filenames and shell parsing
- Hidden files and permissions
- File type identification
- Recursive file searching
- User/group ownership
- Error redirection
- Text searching and filtering
- Pipes and command composition
- Binary-file inspection
- Base64 decoding
- ROT13 decoding
- Hexdump reversal
- gzip/bzip2/tar extraction
- SSH private-key authentication
- Local TCP services
- Port-based communication with netcat

## Walkthrough

Each level has its own detailed document in the `walkthrough/` directory.
