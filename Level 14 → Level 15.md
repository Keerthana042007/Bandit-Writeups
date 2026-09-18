# Bandit Level 14 → Level 15

## Challenge

Login to Bandit Level 14 and find the password for Level 15.

## Commands Used

| Command | Meaning |
| ------- | ------- |
| `ssh` | Connect to a remote server |
| `cat` | Display file contents |
| `nc` | Connect to a network service |
| `exit` | Exit the current session |

## Solution

### Step 1: Connect to the Bandit Level 14 Server

I connected to the Bandit Level 14 server using SSH on port 2220.

```bash
ssh bandit14@bandit.labs.overthewire.org -p 2220
```

The username is `bandit14` and port `2220` is used to connect to the Bandit server.

I entered the password obtained from the previous level.

After entering the password, I successfully logged in to the Bandit Level 14 server.

### Step 2: Read the Password File

The password for Level 15 was stored in the `bandit14` password file.

I used the `cat` command to display its contents.

```bash
cat /etc/bandit_pass/bandit14
```

The command displayed the password for the `bandit14` user.

I copied the password to use for the next step.

### Step 3: Connect to the Network Service

The password needed to be submitted to a service running on port `30000`.

I used the `nc` command to connect to the service.

```bash
nc localhost 30000
```

After connecting, I entered the password obtained from the `/etc/bandit_pass/bandit14` file.

The service verified the password and displayed the password required to log in to Level 15.

I copied the password and used it for the next level.

**Screenshot:**

![Level 14 → Level 15 Password](level14-15.jpeg)

### Step 4: Exit the Current SSH Session

After obtaining the password, I exited the current SSH session using the `exit` command.

```bash
exit
```

### Step 5: Login to Level 15

Next, I connected to the Bandit Level 15 server.

```bash
ssh bandit15@bandit.labs.overthewire.org -p 2220
```

When asked for the password, I entered the password obtained from the network service and successfully connected to the Bandit Level 15 server.

## What I Learned

- `ssh` is used to connect to a remote server.
- `cat` is used to display the contents of a file.
- `/etc/bandit_pass/bandit14` contains the password for the `bandit14` user.
- `nc` (Netcat) is used to connect to network services.
- Port `30000` is used by the service in this level.
- A password can be sent to a network service for verification.
- `exit` is used to close an SSH session.

## Result

Bandit Level 14 → Level 15 completed successfully.
