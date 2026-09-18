# Bandit Level 06 → Level 07

## Challenge

Login to Bandit Level 6 and find the password for Level 7.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `find` | Search for files and directories |
| `cat` | Display file contents |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 6 Server

I connected to the Bandit Level 6 server using SSH on port 2220.

```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
```

The username is `bandit6` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 6 server.

### Step 2: Find the Correct File

The password for Level 7 was stored somewhere on the server.

I used the `find` command to search for a file owned by the user `bandit7` and the group `bandit6`.

```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

The command found the required file.

```text
/var/lib/dpkg/info/bandit7.password
```

### Step 3: Read the File

I used the `cat` command to display the contents of the file.

```bash
cat /var/lib/dpkg/info/bandit7.password
```

The command displayed the password required to log in to Level 7.

I copied the password and used it for the next level.

### Step 4: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 5: Login to Level 7

Next, I connected to the Bandit Level 7 server.

```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained from the `bandit7.password` file and successfully connected to the Bandit Level 7 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `find` is used to search for files based on specific conditions.
- `-user bandit7` searches for files owned by the `bandit7` user.
- `-group bandit6` searches for files belonging to the `bandit6` group.
- `-size 33c` searches for a file with a size of 33 bytes.
- `2>/dev/null` hides error messages from the terminal.
- `cat` is used to display the contents of a file.
- `exit` is used to close an SSH session.

## Result

Bandit Level 06 → Level 07 completed successfully.
