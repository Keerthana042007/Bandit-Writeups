# Bandit Level 08 → Level 09

## Challenge

Login to Bandit Level 8 and find the password for Level 9.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `ls` | List files and directories |
| `sort` | Sort lines of text |
| `uniq` | Display unique lines |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 8 Server

I connected to the Bandit Level 8 server using SSH on port 2220.

```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
```

The username is `bandit8` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 8 server.

### Step 2: List the Files

After logging in, I checked the files in the current directory using the `ls` command.

```bash
ls
```

The output showed a file named `data.txt`.

```text
data.txt
```

### Step 3: Find the Unique Line

The `data.txt` file contains many lines, but the password for Level 9 appears only once.

I used the `sort` and `uniq` commands to find the line that occurs only once.

```bash
sort data.txt | uniq -u
```

The command displayed the unique line, which was the password required to log in to Level 9.

I copied the password and used it for the next level.

**Screenshot:**

![Level 08 → Level 09 Password](level8-9.jpeg)

### Step 4: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 5: Login to Level 9

Next, I connected to the Bandit Level 9 server.

```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained from the `data.txt` file and successfully connected to the Bandit Level 9 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `ls` is used to list files and directories.
- `sort` is used to sort lines of text.
- `uniq -u` displays only lines that occur once.
- `sort data.txt | uniq -u` can be used to find a unique line in a file.
- `exit` is used to close an SSH session.

## Result

Bandit Level 08 → Level 09 completed successfully.
