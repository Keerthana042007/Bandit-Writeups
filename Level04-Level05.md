# Bandit Level 04 → Level 05

## Challenge

Login to Bandit Level 4 and find the password for Level 5.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `ls` | List files and directories |
| `cd` | Change the current directory |
| `ls -al` | List all files, including hidden files |
| `cat` | Display file contents |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 4 Server

I connected to the Bandit Level 4 server using SSH on port 2220.

```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
```

The username is `bandit4` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 4 server.

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

I used the `ls -al` command to display all files, including hidden files, along with their details.

```bash
ls -al
```

The output showed several files with names such as `-file00`, `-file01`, and so on.

### Step 5: Read the Correct File

The required file was `-file07`. Since the filename begins with a hyphen, I used `./` before the filename to specify the file correctly.

```bash
cat ./-file07
```

The command displayed the password required to log in to Level 5.

I copied the password and used it for the next level.

Screenshot:

<img width="746" height="561" alt="WhatsApp Image 2026-09-18 at 8 01 24 AM" src="https://github.com/user-attachments/assets/3ecf3648-9f71-4ae6-94a3-78da0512c352" />


### Step 6: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 7: Login to Level 5

Next, I connected to the Bandit Level 5 server.

```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained from the `-file07` file and successfully connected to the Bandit Level 5 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `ls` is used to list files and directories.
- `cd` is used to change the current directory.
- `ls -al` is used to display all files, including hidden files, with detailed information.
- `cat` is used to display the contents of a file.
- `./` can be used to access a file whose name begins with `-`.
- `exit` is used to close an SSH session.

## Result

Bandit Level 04 → Level 05 completed successfully.
