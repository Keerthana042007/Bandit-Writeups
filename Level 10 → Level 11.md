# Bandit Level 10 → Level 11

## Challenge

Login to Bandit Level 10 and find the password for Level 11.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `ls` | List files and directories |
| `base64` | Encode or decode Base64 data |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 10 Server

I connected to the Bandit Level 10 server using SSH on port 2220.

```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
```

The username is `bandit10` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 10 server.

### Step 2: List the Files

After logging in, I checked the files in the current directory using the `ls` command.

```bash
ls
```

The output showed a file named `data.txt`.

```text
data.txt
```

### Step 3: Decode the Base64 Data

The contents of `data.txt` were encoded using Base64.

I used the `base64 -d` command to decode the contents of the file.

```bash
base64 -d data.txt
```

The command decoded the Base64 data and displayed the password required to log in to Level 11.

I copied the password and used it for the next level.

**Screenshot:**

<img width="662" height="125" alt="WhatsApp Image 2026-09-18 at 11 32 30 AM" src="https://github.com/user-attachments/assets/78d9e9fa-5312-450d-8e99-4a56598d1ed2" />


### Step 4: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 5: Login to Level 11

Next, I connected to the Bandit Level 11 server.

```bash
ssh bandit11@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained by decoding the `data.txt` file and successfully connected to the Bandit Level 11 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `ls` is used to list files and directories.
- `base64` is used to encode and decode Base64 data.
- `base64 -d` is used to decode Base64 encoded data.
- `exit` is used to close an SSH session.

## Result

Bandit Level 10 → Level 11 completed successfully.
