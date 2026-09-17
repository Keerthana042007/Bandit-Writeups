# Bandit Level 03 → Level 04

## Challenge

Login to Bandit Level 3 and find the password for Level 4.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `ls` | List files and directories |
| `cd` | Change the current directory |
| `ls -la` | List all files, including hidden files |
| `cat` | Display file contents |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 3 Server

I connected to the Bandit Level 3 server using SSH on port 2220.

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

The username is `bandit3` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 3 server.

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

### Step 4: List All Files

The password file was hidden, so I used the `ls -la` command to display all files, including hidden files.

```bash
ls -la
```

The output showed a hidden file named `.hidden`.

```text
.hidden
```

### Step 5: Read the Hidden File

I used the `cat` command to display the contents of the hidden file.

```bash
cat .hidden
```

The command displayed the password required to log in to Level 4.

I copied the password and used it for the next level.

**Screenshot:**

![Level 03 → Level 04 Password](level3-4.jpeg)

### Step 6: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 7: Login to Level 4

Next, I connected to the Bandit Level 4 server.

```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained from the `.hidden` file and successfully connected to the Bandit Level 4 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `ls` is used to list files and directories.
- `cd` is used to change the current directory.
- `ls -la` is used to display all files, including hidden files.
- `cat` is used to display the contents of a file.
- Hidden files in Linux can begin with a `.`.
- `exit` is used to close an SSH session.

## Result

Bandit Level 03 → Level 04 completed successfully.
