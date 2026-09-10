
# Bandit – Level 0

## Objective

The objective of Bandit Level 0 is to learn how to connect to the OverTheWire Bandit server using **SSH (Secure Shell)**.

The login details provided for Level 0 are:

- **Username:** `bandit0`
- **Password:** `bandit0`
- **Host:** `bandit.labs.overthewire.org`
- **SSH Port:** `2220`

After successfully logging in, the objective is to find the password required for **Level 1**.

---

## 🛠️ Tools and Commands Used

- SSH
- Linux Command Line
- `ls`
- `cat`

---

# Step 1 – Connect to the Bandit Server

The first step is to connect to the Bandit server using SSH.

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

## Command Explanation

The command can be understood as:

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
│   │       │                                │
│   │       │                                └── SSH port
│   │       └── Remote server
│   └── Username
└── Secure Shell command
```


ssh - stands for Secure Shell.

It is a network protocol and command used to securely connect to and control a remote computer.

SSH provides encrypted communication between the client and the remote server.

bandit0 :

bandit0 is the username used to log in to the Bandit server.

@ :

The @ symbol separates the username from the hostname.

username@hostname

bandit.labs.overthewire.org

This is the hostname of the OverTheWire Bandit server.

-p 2220

The -p option specifies the SSH port.

Normally, SSH uses port: 22

However, the OverTheWire Bandit server uses: 2220

Therefore, -p 2220 tells SSH to connect to port 2220.

# Step 2 – Enter the Password

After executing the SSH command, the terminal asks for the password:

bandit0@bandit.labs.overthewire.org's password:

Enter:

bandit0

## Password Explanation :

For Level 0, the username and password are both:

Username: bandit0
Password: bandit0

When entering a password in a Linux terminal, the characters are normally not displayed.

For example:

bandit0@bandit.labs.overthewire.org's password:

The cursor may appear to remain still while typing.

This is normal security behavior.

After successful authentication, a shell prompt similar to the following appears:

bandit0@bandit:~$

This confirms that the login was successful.

# Step 3 – List the Files

After logging in, the next step is to check what files are available in the current directory.

Use:

ls
## Command Explanation

ls stands for list.

It is used to display the files and directories in the current working directory.

Example:

bandit0@bandit:~$ ls
readme

The output shows:

readme

This means that a file named readme exists in the current directory.

Why did we use ls?

We do not know the exact location or name of the file containing the next password.

Therefore, we first inspect the current directory using ls.

# Step 4 – Read the readme File

After finding the readme file, we need to read its contents.

Use:

cat readme
## Command Explanation

cat is a Linux command used to display the contents of a file directly in the terminal.


The cat command reads and displays the contents of a file.

readme

readme is the name of the file we found using the ls command.

Therefore:

cat readme

means:

Display the contents of the readme file.

The output contains the password required for Bandit Level 1.
