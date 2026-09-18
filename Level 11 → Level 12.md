# Bandit Level 11 → Level 12

## Challenge

Login to Bandit Level 11 and find the password for Level 12.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `ls` | List files and directories |
| `cat` | Display file contents |
| `tr` | Translate or replace characters |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 11 Server

I connected to the Bandit Level 11 server using SSH on port 2220.

```bash
ssh bandit11@bandit.labs.overthewire.org -p 2220
```

The username is `bandit11` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 11 server.

### Step 2: List the Files

After logging in, I checked the files in the current directory using the `ls` command.

```bash
ls
```

The output showed a file named `data.txt`.

```text
data.txt
```

### Step 3: Read the File

I used the `cat` command to display the contents of the file.

```bash
cat data.txt
```

The contents of the file were encrypted using a ROT13 substitution.

### Step 4: Decode the ROT13 Text

I used the `tr` command to replace each character with its ROT13 equivalent.

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

The command decoded the ROT13 text and displayed the password required to log in to Level 12.

I copied the password and used it for the next level.

**Screenshot:**

![Level 11 → Level 12 Password](level11-12.jpeg)

### Step 5: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 6: Login to Level 12

Next, I connected to the Bandit Level 12 server.

```bash
ssh bandit12@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained by decoding the `data.txt` file and successfully connected to the Bandit Level 12 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `ls` is used to list files and directories.
- `cat` is used to display the contents of a file.
- `tr` is used to translate or replace characters.
- ROT13 replaces each letter with another letter 13 positions away in the alphabet.
- `tr 'A-Za-z' 'N-ZA-Mn-za-m'` can be used to decode ROT13 text.
- `exit` is used to close an SSH session.

## Result

Bandit Level 11 → Level 12 completed successfully.
