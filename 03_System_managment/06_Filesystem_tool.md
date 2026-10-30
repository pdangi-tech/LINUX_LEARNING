# Linux File System Tools

## 1. Introduction

File system tools in Linux help users check, create, manage, repair, and resize file systems.

Linux provides different commands to check file system errors, view file system information, create new file systems, and manage file system settings.

In this section, I practiced basic Linux file system tools using Kali Linux.

## 2. Commands Learned

### 1. `fsck`

**Description:** Checks and repairs file system errors.

**Syntax:**
```bash
sudo fsck device_name
```

**Example:**
```bash
sudo fsck /dev/sdb1
```

**Use:** Checks the specified file system for errors and attempts to repair them when necessary.

### 2. `tune2fs`

**Description:** Adjusts and displays settings of ext2, ext3, and ext4 file systems.

**Syntax:**
```bash
sudo tune2fs -l device_name
```

**Example:**
```bash
sudo tune2fs -l /dev/sda1
```

**Use:** Displays detailed file system information, including the file system label, UUID, block count, and other settings.

### 3. `mkfs`

**Description:** Creates a new file system on a storage device or partition.

**Syntax:**
```bash
sudo mkfs -t filesystem_type device_name
```

**Example:**
```bash
sudo mkfs -t ext4 /dev/sdb1
```

**Use:** Creates an ext4 file system on the specified partition.

**Note:** This command can erase existing data on the selected partition. Always check the device name before using it.

### 4. `e2fsck`

**Description:** Checks and repairs ext2, ext3, and ext4 file systems.

**Syntax:**
```bash
sudo e2fsck device_name
```

**Example:**
```bash
sudo e2fsck /dev/sda1
```

**Use:** Checks an ext file system for errors and helps repair file system problems.

### 5. `dumpe2fs`

**Description:** Displays detailed information about ext2, ext3, and ext4 file systems.

**Syntax:**
```bash
sudo dumpe2fs device_name
```

**Example:**
```bash
sudo dumpe2fs /dev/sda1
```

**Use:** Displays file system details, including block size, inode information, group information, and superblock details.

### 6. `resize2fs`

**Description:** Resizes ext2, ext3, and ext4 file systems.

**Syntax:**
```bash
sudo resize2fs device_name
```

**Example:**
```bash
sudo resize2fs /dev/sda1
```

**Use:** Resizes the file system to use the available partition space. It can also resize a file system to a specified size.

**Example with a specific size:**
```bash
sudo resize2fs /dev/sda1 10G
```

---

## 3. What I Learned

- How to check and repair file system errors using `fsck`.
- How to view file system settings using `tune2fs`.
- How to create a new file system using `mkfs`.
- How to check ext file systems using `e2fsck`.
- How to view detailed file system information using `dumpe2fs`.
- How to resize file systems using `resize2fs`.
- How to understand basic Linux file system management.

---

**Learning Status:** Practiced

**Operating System:** Kali Linux

**Category:** Linux Fundamentals