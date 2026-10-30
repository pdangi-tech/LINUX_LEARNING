# Linux Process Management

## 1. Introduction

Process management in Linux allows users to view, monitor, control, and manage running processes.

A process is a program that is currently running in the operating system. Linux provides different commands to check running processes, change process priority, and stop unwanted processes.

In this section, I practiced basic Linux process management commands using Kali Linux.

## 2. Commands Learned

### 1. `top`

**Description:** Displays a dynamic, real-time view of running processes and system resource usage.

**Syntax:**
```bash
top
```

**Example:**
```bash
top
```

**Use:** Monitors running processes, CPU usage, memory usage, and system performance in real time.

### 2. `htop`

**Description:** Provides an interactive and user-friendly interface for monitoring running processes.

**Syntax:**
```bash
htop
```

**Example:**
```bash
htop
```

**Use:** Displays running processes, CPU usage, memory usage, and process information. It also allows users to interact with and manage processes.

### 3. `nice`

**Description:** Starts a process with a specific priority value.

**Syntax:**
```bash
nice -n priority_value command
```

**Example:**
```bash
nice -n 10 sleep 100
```

**Use:** Starts a new process with a selected nice value. A higher nice value means lower scheduling priority, while a lower nice value means higher scheduling priority.

**Note:** Nice values range from `-20` (highest priority) to `19` (lowest priority).

### 4. `renice`

**Description:** Changes the priority of an already running process.

**Syntax:**
```bash
renice -n priority_value -p PID
```

**Example:**
```bash
renice -n 10 -p 1234
```

**Use:** Adjusts the scheduling priority of a running process using its Process ID (PID).

### 5. `kill`

**Description:** Sends a signal to a running process to stop or control it.

**Syntax:**
```bash
kill PID
```

**Example:**
```bash
kill 1234
```

**Use:** Sends the default termination signal (SIGTERM) to a process, requesting it to stop gracefully.

### 6. `kill -9`

**Description:** Forcefully terminates a running process using the SIGKILL signal.

**Syntax:**
```bash
kill -9 PID
```

**Example:**
```bash
kill -9 1234
```

**Use:** Immediately terminates a process without allowing it to handle the termination signal.

**Note:** Use `kill -9` only when a process does not stop normally.

### 7. `ps`

**Description:** Displays information about currently running processes.

**Syntax:**
```bash
ps
```

**Examples:**
```bash
ps
ps -ef
```

**Use:** Displays information about processes, including their PID, terminal, and execution status.

### 8. `ps aux`

**Description:** Displays detailed information about all running processes on the system.

**Syntax:**
```bash
ps aux
```

**Example:**
```bash
ps aux
```

**Use:** Displays detailed process information, including the user, PID, CPU usage, memory usage, and running commands.

---

## 3. What I Learned

- How to monitor running processes using the `top` command.
- How to interactively monitor processes using `htop`.
- How to start a process with a specific priority using `nice`.
- How to change the priority of a running process using `renice`.
- How to terminate a process using the `kill` command.
- How to forcefully stop a process using `kill -9`.
- How to list running processes using the `ps` command.
- How to view detailed process information using `ps aux`.
- How to understand basic Linux process management.

---

**Learning Status:** Practiced

**Operating System:** Kali Linux

**Category:** Linux Fundamentals