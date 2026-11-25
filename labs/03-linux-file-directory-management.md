
# Lab 03 – Linux File and Directory Management

## Objective
To understand and practice Linux file and directory management using:
- mkdir
- touch
- cp
- mv
- rm

## 1. mkdir – Create Directories

The mkdir command creates new directories.

Commands:
```bash
mkdir linux-file-management
mkdir documents projects backups
mkdir -p projects/linux/lab03
```

## 2. touch – Create Files

The touch command creates empty files.

Commands:
```bash
touch notes.txt
touch file1.txt file2.txt file3.txt
```

## 3. cp – Copy Files and Directories

The cp command copies files and directories.

Commands:
```bash
cp documents/notes.txt backups/
cp documents/todo.txt backups/todo-backup.txt
cp -r documents documents-backup
```

## 4. mv – Move and Rename

The mv command moves or renames files and directories.

Commands:
```bash
mv file1.txt renamed-file.txt
mv file2.txt documents/
mv projects projects-backup
```

## 5. rm – Remove Files and Directories

The rm command removes files and directories.

Commands:
```bash
rm file3.txt
rmdir empty-folder
rm -r documents-backup
```

**Warning:** The rm command permanently removes files in normal Linux usage. Verify paths before execution.

## 6. Final Practical Exercise

Commands:
```bash
mkdir final-project
cd final-project
mkdir source backup
touch source/index.html
touch source/style.css
cp source/index.html backup/
mv source/style.css source/main.css
ls -R
```

## Learning Outcomes

- Created directories using mkdir.
- Created empty files using touch.
- Copied files and directories using cp.
- Moved and renamed files using mv.
- Removed files and directories using rm.
- Practiced basic Linux filesystem management.

## Conclusion

Successfully completed Lab 03 and learned essential Linux file and directory management commands.
