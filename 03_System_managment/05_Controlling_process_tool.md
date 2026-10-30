# Linux Controlling Processes Tools

## 1. Introduction

Process control in Linux allows users to manage running processes and background or foreground jobs.

Linux provides different commands to terminate processes, stop multiple processes, and control jobs running in the terminal.

In this section, I practiced basic Linux process control commands using Kali Linux.

## 2. Commands Learned

### 1. `kill`

**Description:** Sends a signal to a specific process to stop or control it.

**Syntax:**
```bash
kill PID
```

**Examples:**
```bash
kill 2023
kill -9 2023
```

**Use:** Sends a termination signal to the process with the specified Process ID (PID). The `-9` option forcefully terminates the process.

### 2. `killall`

**Description:** Terminates processes by their command name.

**Syntax:**
```bash
killall process_name
```

**Example:**
```bash
killall firefox
```

**Use:** Sends a termination signal to all matching processes with the specified name.

### 3. `bg`

**Description:** Resumes a stopped job in the background.

**Syntax:**
```bash
bg %job_number
```

**Example:**
```bash
bg %1
```

**Use:** Continues a stopped job in the background, allowing the terminal to be used for other commands.

### 4. `pkill`

**Description:** Sends a signal to processes based on their name or other matching criteria.

**Syntax:**
```bash
pkill process_name
```

**Examples:**
```bash
pkill firefox
pkill -9 firefox
```

**Use:** Finds and terminates matching processes without requiring their PID.

### 5. `jobs`

**Description:** Displays the jobs currently running or stopped in the current shell session.

**Syntax:**
```bash
jobs
```

**Example:**
```bash
jobs
jobs -l
```

**Use:** Lists background and stopped jobs started from the current shell. The `-l` option also displays their process IDs.

### 6. `fg`

**Description:** Brings a background or stopped job to the foreground.

**Syntax:**
```bash
fg %job_number
```

**Example:**
```bash
fg %1
```

**Use:** Brings the specified job to the foreground so it can interact with the terminal.

---

## 4. What I Learned

- How to terminate a process using the `kill` command.
- How to terminate multiple matching processes using `killall`.
- How to resume stopped jobs in the background using `bg`.
- How to terminate processes by name using `pkill`.
- How to view current shell jobs using the `jobs` command.
- How to bring background jobs to the foreground using `fg`.
- How to control foreground and background processes in Linux.

---

**Learning Status:** Practiced

**Operating System:** Kali Linux

**Category:** Linux Fundamentals