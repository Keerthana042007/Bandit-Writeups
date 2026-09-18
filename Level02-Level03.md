# Bandit Level 02 → Level 03

## Challenge

Login to Bandit Level 2 and find the password for Level 3.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `ls` | List files and directories |
| `cat` | Display file contents |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 2 Server

I connected to the Bandit Level 2 server using SSH on port 2220.

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```

The username is `bandit2` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 2 server.

### Step 2: List the Files

After logging in, I checked the files in the current directory using the `ls` command.

```bash
ls
```

The output showed a file with spaces in its name.

```text
spaces in this filename
```

### Step 3: Read the File

Since the filename contains spaces, I used quotation marks around the filename.

```bash
cat "spaces in this filename"
```

The command displayed the password required to log in to Level 3.
<img width="592" height="84" alt="WhatsApp Image 2026-09-10 at 10 51 58 PM (1)" src="https://github.com/user-attachments/assets/1787f82f-521b-469b-bb68-1d291e02b426" />


I copied the password and used it for the next level.

### Step 4: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 5: Login to Level 3

Next, I connected to the Bandit Level 3 server:

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained from the `spaces in this filename` file and successfully connected to the Bandit Level 3 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `ls` is used to list files and directories.
- `cat` is used to display the contents of a file.
- Quotation marks can be used to handle filenames containing spaces.
- `exit` is used to close an SSH session.

## Result

Bandit Level 02 → Level 03 completed successfully.
