# Linux File Permissions

## 1. Introduction

File permissions in Linux control who can read, write, and execute files and directories.

Linux provides different methods to manage file permissions. The `chmod` command is used to change permissions.

In this section, I practiced symbolic and numeric permission methods using Kali Linux.

## 2. `chmod`

**Description:** Changes file and directory permissions in Linux.

**Syntax:**
```bash
chmod permissions filename
```

**Example:**
```bash
chmod 755 notes.txt
```

**Use:** Changes the permissions of the specified file or directory.

## 3. Symbolic Method

**Description:** The symbolic method changes file permissions using letters and symbols instead of numbers.

**Permission Categories:**

- `u` = User (Owner)
- `g` = Group
- `o` = Others
- `a` = All

**Permission Operators:**

- `+` = Add permission
- `-` = Remove permission
- `=` = Set exact permission

**Syntax:**
```bash
chmod [who][operator][permission] filename
```

**Examples:**

**1. Add execute permission for the owner.**
```bash
chmod u+x filename
```
**Use:** Adds execute permission for the file owner.

**2. Remove write permission from the group.**
```bash
chmod g-w filename
```
**Use:** Removes write permission from the group.

**3. Add execute permission for everyone.**
```bash
chmod a+x filename
```
**Use:** Adds execute permission for the owner, group, and others.

**4. Set read, write, and execute permissions for the owner.**
```bash
chmod u=rwx filename
```
**Use:** Sets the owner's permissions to read, write, and execute.

## 4. Numeric Method

**Description:** The numeric method changes file permissions using numbers instead of letters.

**Syntax:**
```bash
chmod numeric_value filename
```

**Permission Values:**

| Permission | Number |
|---|---:|
| Read (r) | 4 |
| Write (w) | 2 |
| Execute (x) | 1 |
| No Permission (-) | 0 |

**Examples:**

**1. `chmod 755`**
```bash
chmod 755 filename
```
**Use:**
- Owner: Read, Write, Execute
- Group: Read, Execute
- Others: Read, Execute

**2. `chmod 644`**
```bash
chmod 644 filename
```
**Use:**
- Owner: Read, Write
- Group: Read only
- Others: Read only

**3. `chmod 600`**
```bash
chmod 600 filename
```
**Use:**
- Owner: Read, Write
- Group: No permission
- Others: No permission

**4. `chmod 777`**
```bash
chmod 777 filename
```
**Use:**
- Owner: Full permission
- Group: Full permission
- Others: Full permission

**Note:** Avoid using `777` unless necessary because it gives everyone full access to the file.

---

## 5. Evidences

Screenshots of my practical Linux file permission exercises are stored in the `Evidence_image/` directory.

### Screenshot 1: Linux Terminal

![Image 1](../Evidence_image/image16.png)

### Screenshot 2: Linux Terminal

![Image 2](../Evidence_image/image17.png)

---

## 6. What I Learned

- How to change file permissions using the `chmod` command.
- How to use the symbolic permission method.
- How to use the numeric permission method.
- How to understand read, write, and execute permissions.
- How to add and remove permissions using symbolic operators.
- How to assign permissions using numeric values.
- How to understand user, group, and others permissions.

---

**Learning Status:** Practiced

**Operating System:** Kali Linux

**Category:** Linux Fundamentals