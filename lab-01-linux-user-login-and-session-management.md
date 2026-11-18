## Linux User Login and Session Management

## 1. Overview

This lab focuses on essential Linux user login and session management tasks using Ubuntu Linux.

The purpose of this practical exercise is to understand how users interact with a Linux system, manage terminal sessions, maintain password security, and establish secure remote connections using SSH.

## 2. Objectives

- Understand Linux user login and logout.
- Identify the currently logged-in user.
- Explore Linux user and group information.
- Understand password management and security.
- Learn how to manage terminal sessions.
- Understand SSH fundamentals.
- Establish and terminate a local SSH connection.

## 3. Environment

| Component | Details |
|---|---|
| Operating System | Ubuntu Linux |
| Environment | Virtual Machine |
| Interface | Linux Terminal |
| Tools | OpenSSH |
| Level | Beginner |

## 4. Practical Exercises

### Exercise 1 – Identify the Logged-in User

**Commands:**

```bash
whoami
id
hostname
```

**Learning outcome:**

- `whoami` identifies the current user.
- `id` displays user and group IDs.
- `hostname` displays the system hostname.

**Screenshot:** `01-user-identification.png`

### Exercise 2 – View User Information

**Commands:**

```bash
who
w
id $USER
groups
```

**Learning outcome:**

These commands help identify logged-in users, session activities, user IDs, and group memberships.

**Screenshot:** `02-user-information.png`

### Exercise 3 – Password Management

**Command:**

```bash
passwd
```

**Learning outcome:**

The `passwd` command allows a user to change their account password.

Password security practices:

- Use strong and unique passwords.
- Never share login credentials.
- Avoid storing passwords in plain-text files.
- Never upload passwords to GitHub.

**Screenshot:** `03-password-management.png`

### Exercise 4 – Terminal Session Management

**Commands:**

```bash
tty
echo "Linux Session Management Lab"
date
exit
```

**Learning outcome:**

- `tty` identifies the current terminal.
- `echo` displays a message.
- `date` displays the system date and time.
- `exit` terminates the current shell.

**Screenshot:** `04-terminal-session.png`

### Exercise 5 – SSH Fundamentals

SSH (Secure Shell) is a protocol used to establish encrypted remote connections between computers.

**Install OpenSSH Server:**

```bash
sudo apt update
sudo apt install openssh-server -y
```

**Start SSH Service:**

```bash
sudo systemctl start ssh
```

**Check SSH Service Status:**

```bash
sudo systemctl status ssh
```

**Connect to the Local Ubuntu System:**

```bash
ssh $USER@localhost
```

**Verify the Connection:**

```bash
whoami
hostname
```

**Terminate the SSH Connection:**

```bash
exit
```

**Learning outcome:**

Successfully established and terminated a local SSH connection using OpenSSH.

**Screenshots:**
- `05-ssh-connection.png`
- `06-ssh-logout.png`

### 5. Important Linux Commands

| Command | Description |
|---|---|
| `whoami` | Displays current username |
| `id` | Displays user and group IDs |
| `hostname` | Displays system hostname |
| `who` | Displays logged-in users |
| `w` | Displays user session activity |
| `groups` | Displays user group memberships |
| `passwd` | Changes account password |
| `tty` | Displays terminal information |
| `date` | Displays system date and time |
| `ssh` | Establishes a secure remote connection |
| `exit` | Terminates the current shell or SSH session |

### 6. Security Best Practices

- Protect user account credentials.
- Use strong passwords.
- Never share SSH credentials.
- Connect only to authorized remote systems.
- Prefer SSH key authentication for remote administration.
- Avoid uploading sensitive information or passwords to public repositories.

### 7. Challenges and Learning

During this practical exercise, I explored Linux user identification, account information, terminal session management, password security, and SSH connectivity.

I also learned the difference between closing a terminal shell and disconnecting from an SSH session.

### 8. Conclusion

This lab provided practical experience with fundamental Linux user and session management concepts using Ubuntu.

These skills form an important foundation for Linux system administration, cloud computing, and cybersecurity.

---

**Author:** Linux Learning Journal  
**Lab:** 01 – Linux User Login and Session Management  
**Platform:** Ubuntu Linux
