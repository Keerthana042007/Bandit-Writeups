# Bandit Level 05 → Level 06

## Challenge

Login to Bandit Level 5 and find the password for Level 6.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `ls` | List files and directories |
| `cd` | Change the current directory |
| `find` | Search for files and directories |
| `cat` | Display file contents |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 5 Server

I connected to the Bandit Level 5 server using SSH on port 2220.

```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
```

The username is `bandit5` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 5 server.

### Step 2: List the Files

After logging in, I checked the files in the current directory using the `ls` command.

```bash
ls
```

The output showed a directory named `inhere`.

```text
inhere
```

### Step 3: Enter the `inhere` Directory

I entered the `inhere` directory using the `cd` command.

```bash
cd inhere
```

### Step 4: Find the Correct File

There were many directories and files inside `inhere`. The required file was a regular file with a specific size and without execute permission.

I used the `find` command to search for the file.

```bash
find -type f -size 1033c ! -executable
```

The command found the required file:

```text
./maybehere07/.file2
```

### Step 5: Read the File

I used the `cat` command to display the contents of the file.

```bash
cat ./maybehere07/.file2
```

The command displayed the password required to log in to Level 6.

I copied the password and used it for the next level.

**Screenshot:**

<img width="1079" height="176" alt="WhatsApp Image 2026-09-18 at 8 08 51 AM" src="https://github.com/user-attachments/assets/2699e0b6-61c3-4387-bc88-413157ac3187" />


### Step 6: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 7: Login to Level 6

Next, I connected to the Bandit Level 6 server.

```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained from the `.file2` file and successfully connected to the Bandit Level 6 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `ls` is used to list files and directories.
- `cd` is used to change the current directory.
- `find` is used to search for files and directories based on different conditions.
- `-type f` searches for regular files.
- `-size 1033c` searches for a file with a size of 1033 bytes.
- `! -executable` excludes executable files.
- `cat` is used to display the contents of a file.
- `exit` is used to close an SSH session.

## Result

Bandit Level 05 → Level 06 completed successfully.
