# Bandit Level 01 → Level 02

## Challenge

Login to Bandit Level 1 and find the password for Level 2.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `ls` | List files and directories |
| `cat` | Display file contents |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 1 Server

I connected to the Bandit Level 1 server using SSH on port 2220.

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

The username is `bandit1` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 1 server.

### Step 2: List the Files

After logging in, I checked the files in the current directory using the `ls` command.

```bash
ls
```

The output showed a file named `-`.

```text
-
```

### Step 3: Read the `-` File

The filename is `-`, so I used `./-` to specify the file in the current directory.

```bash
cat ./-
```

The command displayed the password required to log in to Level 2.

I copied the password and used it for the next level.

### Step 4: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 5: Login to Level 2

Next, I connected to the Bandit Level 2 server:

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained from the `-` file and successfully connected to the Bandit Level 2 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `ls` is used to list files and directories.
- `cat` is used to display the contents of a file.
- `./-` is used to access a file named `-` in the current directory.
- `exit` is used to close an SSH session.

## Result

Bandit Level 01 → Level 02 completed successfully.
