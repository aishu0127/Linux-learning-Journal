# Basic Linux Commands

## Objective

To learn and practice basic Linux commands for viewing file contents and accessing command documentation.

## Commands Practiced

### 1. `cat` — Display File Contents

The `cat` command displays the contents of a file in the terminal.

**Example:**

```bash
cat notes.txt
```

To display multiple files:

```bash
cat file1.txt file2.txt
```

### 2. `head` — Display the Beginning of a File

The `head` command displays the first 10 lines of a file by default.

**Examples:**

```bash
head notes.txt
```

Display only the first 3 lines:

```bash
head -n 3 notes.txt
```

### 3. `tail` — Display the End of a File

The `tail` command displays the last 10 lines of a file by default.

**Examples:**

```bash
tail notes.txt
```

Display only the last 3 lines:

```bash
tail -n 3 notes.txt
```

Monitor a file as new lines are added:

```bash
tail -f notes.txt
```

Press `Ctrl + C` to stop monitoring.

### 4. `man` — Read Command Documentation

The `man` command opens the manual page for a Linux command.

**Examples:**

```bash
man cat
man head
man tail
```

Useful navigation keys:

- `Space` — Move forward one page
- `b` — Move backward one page
- `/word` — Search for a word
- `q` — Exit the manual

## Practice Exercise

1. Create a file named `notes.txt` containing at least 10 lines.
2. Display the entire file using `cat`.
3. Display the first 3 lines using `head`.
4. Display the last 3 lines using `tail`.
5. Open the manual page for `cat` using `man cat`.

## Learning Outcomes

- Learned to display file contents using `cat`.
- Practiced viewing the beginning and end of files using `head` and `tail`.
- Learned to access and navigate Linux command manuals using `man`.
