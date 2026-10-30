# Linux Group Management

## 1. Introduction

Group management in Linux allows users to create, delete, modify, and manage groups. Groups help organize users and control access to files and system resources.

In this section, I practiced basic group management commands using Kali Linux.

## 2. Commands Learned

### 1. `groupadd`

**Description:** Creates a new group.

**Syntax:**
```bash
sudo groupadd group_name
```

**Example:**
```bash
sudo groupadd developers
```

**Use:** Creates a new group named `developers`.

### 2. `groupdel`

**Description:** Deletes an existing group.

**Syntax:**
```bash
sudo groupdel group_name
```

**Example:**
```bash
sudo groupdel developers
```

**Use:** Deletes the specified group. Make sure the group is no longer needed before removing it.

### 3. `groups`

**Description:** Shows the groups that a user belongs to.

**Syntax:**
```bash
groups username
```

**Example:**
```bash
groups john
```

**Use:** Displays the group memberships of the specified user.

### 4. `newgrp`

**Description:** Starts a new shell with a different current group.

**Syntax:**
```bash
newgrp group_name
```

**Example:**
```bash
newgrp developers
```

**Use:** Temporarily changes the current group for the new shell session, when the user is allowed to use that group.

### 5. `gpasswd`

**Description:** Manages group membership and group administrators.

**Syntax:**
```bash
sudo gpasswd -a username group_name
sudo gpasswd -d username group_name
```

**Examples:**
```bash
sudo gpasswd -a john developers
sudo gpasswd -d john developers
```

**Use:** Adds a user to a group with `-a` or removes a user from a group with `-d`.

### 6. `groupmod -g`

**Description:** Changes the numerical group ID (GID) of an existing group.

**Syntax:**
```bash
sudo groupmod -g new_GID group_name
```

**Example:**
```bash
sudo groupmod -g 1050 developers
```

**Use:** Changes the GID of the specified group. Choose an unused GID.

### 7. `groupmod -n`

**Description:** Changes the name of an existing group.

**Syntax:**
```bash
sudo groupmod -n new_group_name old_group_name
```

**Example:**
```bash
sudo groupmod -n programmers developers
```

**Use:** Renames the group from `developers` to `programmers`.

### 8. `cat /etc/group`

**Description:** Displays the local group information stored in the `/etc/group` file.

**Syntax:**
```bash
cat /etc/group
```

**Use:** Shows local group entries, including group names and GIDs.

### 9. `getent group`

**Description:** Displays group entries from the system's configured group database.

**Syntax:**
```bash
getent group
```

**Example:**
```bash
getent group developers
```

**Use:** Lists group entries or displays information about a specific group.

### 10. `id`

**Description:** Displays a user's UID, primary GID, and group memberships.

**Syntax:**
```bash
id username
```

**Example:**
```bash
id john
```

**Use:** Shows the user ID, group ID, and groups that the user belongs to.

---

## 3. Evidences

Screenshots of my practical Linux group management exercises are stored in the `Evidence_image/` directory.

### Screenshot 1: Linux Terminal

![Image 1](../Evidence_image/image10.png)

### Screenshot 2: Linux Terminal

![Image 2](../Evidence_image/image11.png)

### Screenshot 3: Linux Terminal

![Image 3](../Evidence_image/image12.png)


---

## 4. What I Learned

- How to create and delete Linux groups.
- How to check which groups a user belongs to.
- How to add users to and remove users from groups.
- How to change a group name and GID.
- How to view group information and group IDs.

---

**Learning Status:** Practiced

**Operating System:** Kali Linux

**Category:** Linux Fundamentals
