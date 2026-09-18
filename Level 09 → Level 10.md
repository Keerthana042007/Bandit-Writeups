# Bandit Level 09 → Level 10

## Challenge

Login to Bandit Level 9 and find the password for Level 10.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `ls` | List files and directories |
| `strings` | Display readable text from binary files |
| `grep` | Search for specific text |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 9 Server

I connected to the Bandit Level 9 server using SSH on port 2220.

```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
```

The username is `bandit9` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 9 server.

### Step 2: List the Files

After logging in, I checked the files in the current directory using the `ls` command.

```bash
ls
```

The output showed a file named `data.txt`.

```text
data.txt
```

### Step 3: Find the Readable Text

The `data.txt` file contains binary data and some readable text.

I used the `strings` command to display readable text from the file and the `grep` command to search for the text containing several `=` characters.

```bash
strings data.txt | grep "==="
```

The command displayed the password required to log in to Level 10.

I copied the password and used it for the next level.

**Screenshot:**

![Level 09 → Level 10 Password](level9-10.jpeg)

### Step 4: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 5: Login to Level 10

Next, I connected to the Bandit Level 10 server.

```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained from the `data.txt` file and successfully connected to the Bandit Level 10 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `ls` is used to list files and directories.
- `strings` is used to display readable text from binary files.
- `grep` is used to search for specific text.
- `strings data.txt | grep "==="` searches readable text containing `===`.
- `exit` is used to close an SSH session.

## Result

Bandit Level 09 → Level 10 completed successfully.
