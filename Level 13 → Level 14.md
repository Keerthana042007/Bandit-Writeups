# Bandit Level 13 → Level 14

## Challenge

Login to Bandit Level 13 and find the password for Level 14.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `ls` | List files and directories |
| `ssh -i` | Connect using a private SSH key |
| `cat` | Display file contents |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 13 Server

I connected to the Bandit Level 13 server using SSH on port 2220.

```bash
ssh bandit13@bandit.labs.overthewire.org -p 2220
```

The username is `bandit13` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 13 server.

### Step 2: List the Files

After logging in, I checked the files in the current directory using the `ls` command.

```bash
ls
```

The output showed a file named `sshkey.private`.

```text
sshkey.private
```

### Step 3: Use the Private SSH Key

The `sshkey.private` file is a private SSH key that can be used to authenticate as the `bandit14` user.

I used the `ssh -i` command with the private key to connect to Level 14.

```bash
ssh -i sshkey.private bandit14@localhost
```

After entering the required confirmation, I successfully logged in as the `bandit14` user.

### Step 4: Find the Password

After logging in to Level 14, the password was stored in the following file.

```bash
cat /etc/bandit_pass/bandit14
```

The command displayed the password required for the next level.

I copied the password for use in the next level.

### Step 5: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

## What I Learned

- `ssh` is used to connect to a remote server.
- `ls` is used to list files and directories.
- A private SSH key can be used for authentication instead of a password.
- `ssh -i` is used to specify a private SSH key.
- `cat` is used to display the contents of a file.
- `/etc/bandit_pass/bandit14` contains the password for the `bandit14` user.
- `exit` is used to close an SSH session.

## Result

Bandit Level 13 → Level 14 completed successfully.
