# Bandit Level 00 → Level 01

## Challenge

Login to Bandit Level 0 and find the password for Level 1.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `ls` | List files and directories |
| `cat` | Display file contents |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Server

I connected to the Bandit server using SSH on port 2220.

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

The username is `bandit0` and port `2220` is used to connect to the Bandit server.

The default password for Level 0 is:

```text
bandit0
```

After entering the password, I successfully logged in to the Bandit Level 0 server.

### Step 2: List the Files

After logging in, I checked the files in the current directory using the `ls` command.

```bash
ls
```

The output showed a file named `readme`.

```text
readme
```

### Step 3: Read the readme File

I used the `cat` command to display the contents of the `readme` file.

```bash
cat readme
```

The command displayed the password required to log in to Level 1.
<img width="788" height="225" alt="WhatsApp Image 2026-09-10 at 10 51 58 PM" src="https://github.com/user-attachments/assets/f67f54fa-079f-40d1-bde4-c50bdc9ac242" />


I copied the password and used it for the next level.

### Step 4: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 5: Login to Level 1

Next, I connected to the Bandit Level 1 server:

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained from the `readme` file and successfully connected to the Bandit Level 1 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `ls` is used to list files and directories.
- `cat` is used to display the contents of a file.
- `exit` is used to close an SSH session.

## Result

Bandit Level 00 → Level 01 completed successfully.
