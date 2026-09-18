# Bandit Level 12 → Level 13

## Challenge

Login to Bandit Level 12 and find the password for Level 13.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `ls` | List files and directories |
| `mkdir` | Create a new directory |
| `cp` | Copy files |
| `xxd` | Convert hexadecimal dump back to binary |
| `file` | Identify the type of a file |
| `mv` | Move or rename a file |
| `gzip` | Compress or decompress files |
| `bzip2` | Compress or decompress BZIP2 files |
| `tar` | Create or extract TAR archives |
| `cat` | Display file contents |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 12 Server

I connected to the Bandit Level 12 server using SSH on port 2220.

```bash
ssh bandit12@bandit.labs.overthewire.org -p 2220
```

The username is `bandit12` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 12 server.

### Step 2: List the Files

After logging in, I checked the files in the current directory using the `ls` command.

```bash
ls
```

The output showed a file named `data.txt`.

```text
data.txt
```

### Step 3: Create a Temporary Directory

Since the file needed to be repeatedly converted and extracted, I created a temporary directory in `/tmp`.

```bash
mkdir /tmp/bandit12
```

I then copied the `data.txt` file into the temporary directory.

```bash
cp data.txt /tmp/bandit12/
```

### Step 4: Enter the Temporary Directory

I changed to the temporary directory.

```bash
cd /tmp/bandit12
```

### Step 5: Convert the Hexdump Back to Binary

The `data.txt` file contained a hexadecimal dump. I used `xxd` with the `-r` option to convert it back into its original binary form.

```bash
xxd -r data.txt data
```

### Step 6: Identify the File Type

I used the `file` command to identify the type of the resulting file.

```bash
file data
```

The output showed that the file was compressed.

I repeatedly used `file` to identify the compression format and renamed the file with the appropriate extension before decompressing it.

### Step 7: Extract the Compressed Files

For a GZIP compressed file, I used:

```bash
mv data data.gz
```

```bash
gzip -d data.gz
```

For a BZIP2 compressed file, I used:

```bash
mv data data.bz2
```

```bash
bzip2 -d data.bz2
```

For a TAR archive, I used:

```bash
mv data data.tar
```

```bash
tar -xf data.tar
```

I repeated the process of checking the file type and extracting it until the final file was obtained.

### Step 8: Read the Password

After extracting the final file, I used the `cat` command to display its contents.

```bash
cat data
```

The command displayed the password required to log in to Level 13.

I copied the password and used it for the next level.

**Screenshot:**

![Level 12 → Level 13 Password](level12-13.jpeg)

### Step 9: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 10: Login to Level 13

Next, I connected to the Bandit Level 13 server.

```bash
ssh bandit13@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained from the extracted file and successfully connected to the Bandit Level 13 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `ls` is used to list files and directories.
- `mkdir` is used to create a new directory.
- `cp` is used to copy files.
- `xxd -r` is used to convert a hexadecimal dump back into binary data.
- `file` is used to identify the type of a file.
- `gzip` and `bzip2` are used to decompress compressed files.
- `tar` is used to extract TAR archives.
- `cat` is used to display the contents of a file.
- Compressed files may need to be repeatedly identified and extracted.
- `exit` is used to close an SSH session.

## Result

Bandit Level 12 → Level 13 completed successfully.
