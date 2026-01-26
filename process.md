
# Process Management Commands in Linux

## View Running Processes

```bash
ps
```
Shows the working processes.

### Syntax
```bash
ps -u "user id"
```

### Example
```bash
ps -u kali
```

---

## Kill a Process

To kill a process, we use the `kill` command.

### Syntax
```bash
kill process_id
```

To get the process ID:
```bash
pgrep firefox
```

### Example
```bash
kill 1307353
```

---

## Process Monitoring

```bash
top
```

```bash
htop
```
Used to see the task bar of the process.

---

## Foreground and Background Processes

- **Foreground process** → can see what is happening
- **Background process** → can't see what is happening

Pause a process:
```bash
Ctrl + Z
```

Send process to background:
```bash
bg
```

Bring process to foreground:
```bash
fg
```

To stop a background process, bring it to foreground and stop it.

---

## Kill Without Process ID

```bash
pkill -9
```
Used to kill the process without the process ID.
