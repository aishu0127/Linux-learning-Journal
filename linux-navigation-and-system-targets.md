# Linux Navigation, Root Access & System Targets

## Objective

Practice essential Linux commands for navigating the filesystem, viewing directory contents, identifying the current user, accessing the root user's home directory, and switching between system targets.

## Environment

- Operating System: Ubuntu Linux
- Shell: Bash
- Service Manager: systemd

## Commands Practiced

### 1. Display the Current Directory

```bash
pwd
```

**Purpose:** Prints the absolute path of the current working directory.

Example output:

```text
/home/aishwarya
```

### 2. List Files and Directories

```bash
ls -la
```

**Purpose:**
- `-l`: Displays detailed file information.
- `-a`: Includes hidden files and directories.

Example output:

```text
drwxr-xr-x  5 user user 4096 Nov  5 20:00 .
drwxr-xr-x  3 root root 4096 Nov  5 19:00 ..
-rw-r--r--  1 user user  220 Nov  5 19:00 .bash_logout
```

### 3. Navigate to the Root User's Home Directory

```bash
cd /root
```

**Purpose:** Changes the current directory to `/root`, the root user's home directory.

A regular user may receive a permission-denied message. To access it, open a root login shell:

```bash
sudo -i
cd /root
pwd
```

Exit the root shell when finished:

```bash
exit
```

**Security note:** Use root privileges only when necessary.

### 4. Identify the Current User

```bash
whoami
```

**Purpose:** Displays the effective username of the current session.

Example output:

```text
aishwarya
```

After entering a root shell, the output will typically be:

```text
root
```

### 5. Switch to Multi-User Text Mode

```bash
sudo systemctl isolate multi-user.target
```

**Purpose:** Switches the system to the multi-user target, typically without a graphical desktop.

This target supports multiple users and system services but does not require a graphical login.

**Caution:** Running this command from a graphical desktop may terminate your desktop session. Save your work first.

### 6. Switch to Graphical Mode

```bash
sudo systemctl isolate graphical.target
```

**Purpose:** Switches the system to the graphical target, which provides the graphical login and desktop environment when configured.

This command may return you to a graphical login screen.

## Practice Exercise

1. Open the Ubuntu terminal.
2. Run `pwd` and record the output.
3. Run `ls -la` and identify one hidden file.
4. Run `whoami` and record your username.
5. Try `cd /root` and observe the result.
6. If necessary, use `sudo -i` to access `/root`, then exit the root shell.
7. Save your work and test the multi-user target.
8. Return to the graphical target if your Ubuntu installation supports it.

## Troubleshooting

| Issue | Possible explanation | Solution |
|---|---|---|
| Permission denied when entering `/root` | Regular users cannot normally access the root home directory | Use `sudo -i` when appropriate |
| `systemctl` command not found | systemd tools may be unavailable in the environment | Verify that Ubuntu is running with systemd |
| Graphical session closes | Switching to `multi-user.target` can stop the display manager | Save work before switching; use a TTY or VM console |
| Graphical target does not start | The graphical environment or display manager may not be installed or configured | Check the installation and display manager status |

## Key Learnings

- Navigated Linux directories using `pwd` and `cd`.
- Inspected hidden files and directory metadata using `ls -la`.
- Identified the current user with `whoami`.
- Learned about root privileges and protected directories.
- Practiced switching between systemd targets.

## Evidence

Add screenshots of your terminal outputs to the repository's `screenshots/` directory and link them here.

Example:

```markdown
![Current directory and directory listing](screenshots/navigation-and-listing.png)
```
