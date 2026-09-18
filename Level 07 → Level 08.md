# Bandit Level 07 → Level 08

## Challenge

Login to Bandit Level 7 and find the password for Level 8.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `ls` | List files and directories |
| `cat` | Display file contents |
| `grep` | Search for specific text |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 7 Server

I connected to the Bandit Level 7 server using SSH on port 2220.

```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
```

The username is `bandit7` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 7 server.

### Step 2: List the Files

After logging in, I checked the files in the current directory using the `ls` command.

```bash
ls
```

The output showed a file named `data.txt`.

```text
data.txt
```

### Step 3: Search for the Password

The password for Level 8 was stored in `data.txt` next to the word `millionth`.

I used the `grep` command to search for the word `millionth`.

```bash
cat data.txt | grep "millionth"
```

The command displayed the line containing `millionth` and the password required to log in to Level 8.

I copied the password and used it for the next level.

**Screenshot:**

<img width="511" height="110" alt="WhatsApp Image 2026-09-18 at 11 27 34 AM" src="https://github.com/user-attachments/assets/fafe7ced-a747-4760-9756-0c3d2f80fe01" />


### Step 4: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 5: Login to Level 8

Next, I connected to the Bandit Level 8 server.

```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained from the `data.txt` file and successfully connected to the Bandit Level 8 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `ls` is used to list files and directories.
- `cat` is used to display the contents of a file.
- `grep` is used to search for specific text.
- `cat data.txt | grep "millionth"` searches for the word `millionth` inside `data.txt`.
- `exit` is used to close an SSH session.

## Result

Bandit Level 07 → Level 08 completed successfully.
