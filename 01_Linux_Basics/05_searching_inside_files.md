# Linux Search Basics

## 1. Introduction

Linux search commands help users find files, locate commands, and search for specific words inside files.

In this section, I practiced basic search commands using Kali Linux.

## 2. Commands Learned

### 1. `find`

**Description:** Searches for files and directories by name or other conditions.

**Syntax:**
```bash
find path -name "filename"
```

**Example:**
```bash
find . -name "notes.txt"
```

**Use:** Searches for `notes.txt` in the current directory and its subdirectories.

### 2. `locate`

**Description:** Quickly searches for files using a database of file locations.

**Syntax:**
```bash
locate filename
```

**Example:**
```bash
locate notes.txt
```

**Use:** Finds matching paths using the locate database. Results may not include very recently created files until the database is updated.

### 3. `which`

**Description:** Shows the path of a command that can be found through the current `PATH`.

**Syntax:**
```bash
which command_name
```

**Example:**
```bash
which python
which ls
```

**Use:** Helps identify the executable path for a command.

### 4. `whereis`

**Description:** Shows the locations of a command's binary, source files, and manual pages when available.

**Syntax:**
```bash
whereis command_name
```

**Example:**
```bash
whereis ls
```

**Use:** Helps locate command-related files and documentation.

### 5. `grep`

**Description:** Searches for matching text inside files.

**Syntax:**
```bash
grep "word" file.txt
```

**Example:**
```bash
grep "error" notes.txt
```

**Use:** Displays lines containing the specified word or pattern.

### 6. `egrep`

**Description:** Searches text using extended regular expressions. On modern Linux systems, `grep -E` is the recommended form.

**Syntax:**
```bash
grep -E "pattern" file.txt
```

**Example:**
```bash
grep -E "error|warning" notes.txt
```

**Use:** Searches for more complex patterns, such as either `error` or `warning`.

### 7. `grep -i`

**Description:** Searches without distinguishing uppercase and lowercase letters.

**Syntax:**
```bash
grep -i "word" file.txt
```

**Example:**
```bash
grep -i "linux" notes.txt
```

**Use:** Matches words such as `Linux`, `LINUX`, and `linux`.

### 8. `grep -r`

**Description:** Searches recursively through files inside a directory and its subdirectories.

**Syntax:**
```bash
grep -r "word" /path/to/folder
```

**Example:**
```bash
grep -r "error" ./logs
```

**Use:** Searches for matching text throughout the specified folder.

### 9. `grep -n`

**Description:** Displays the line number for each matching line.

**Syntax:**
```bash
grep -n "word" file.txt
```

**Example:**
```bash
grep -n "Linux" notes.txt
```

**Use:** Helps identify the line where a match appears.

## 3. Evidences

Screenshots of my practical Linux search exercises will be stored in the `Evidence_image` folder.

### Screenshot 1: Linux Terminal

![Image 1](../Evidence_image/image8.png)

### Screenshot 2: Linux Terminal

![Image 2](../Evidence_image/image9.png)


## 4. What I Learned

- How to search for files and directories.
- How to locate command paths and related files.
- How to search for words inside files.
- How to use `grep` options for case-insensitive, recursive, and line-number searches.

---

**Learning Status:** Practiced

**Operating System:** Kali Linux

**Category:** Linux Fundamentals
