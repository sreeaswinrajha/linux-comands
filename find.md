# 🔍 Linux `find` Command Cheat Sheet

The `find` command helps you locate files and directories in a filesystem using flexible options and conditions.

---

## 📁 Command Syntax

```bash
find [path] [options] [expression]
```

- **path**: Directory to begin the search (e.g., `.` or `/var`)
- **options**: Filters like `-name`, `-type`, `-size`, etc.
- **expression**: Actions to take on matched files (e.g., `-exec`, `-delete`)

---

## 🔹 Basic Usage Examples

| Command | Description |
|--------|-------------|
| `find . -name "file.txt"` | 🔍 Find `file.txt` in current and subdirectories |
| `find /etc -type f` | 📄 Find all files in `/etc` |
| `find /var/log -type d` | 📁 Find all directories in `/var/log` |
| `find . -iname "*.jpg"` | 🎨 Case-insensitive search for `.jpg` files |
| `find / -name "*.conf" 2>/dev/null` | 🔇 Ignore permission-denied errors |

---

## 🔹 Name-Based Search

| Option | Description | Example |
|--------|-------------|---------|
| `-name` | Case-sensitive match | `find . -name "test.txt"` |
| `-iname` | Case-insensitive match | `find . -iname "Test.TXT"` |
| `! -name` / `-not -name` | Exclude files | `find . ! -name "*.sh"` |

---

## 🔹 Type-Based Search

| Option | Description | Example |
|--------|-------------|---------|
| `-type f` | Regular files | `find . -type f` |
| `-type d` | Directories | `find . -type d` |
| `-type l` | Symbolic links | `find . -type l` |

---

## 🔹 Size-Based Search

| Syntax | Description | Example |
|--------|-------------|---------|
| `+n` | Greater than n units | `find . -size +10M` |
| `-n` | Less than n units | `find . -size -100k` |
| `n` | Exactly n units | `find . -size 512c` |

📏 **Units**:
- `c` = bytes  
- `k` = kilobytes  
- `M` = megabytes  
- `G` = gigabytes  

---

## 🔹 Time-Based Search

| Option | Description | Example |
|--------|-------------|---------|
| `-mtime +7` | Modified more than 7 days ago | `find . -mtime +7` |
| `-mtime -3` | Modified within last 3 days | `find . -mtime -3` |
| `-atime n` | Accessed exactly *n* days ago | `find . -atime 1` |
| `-ctime n` | Changed status *n* days ago | `find . -ctime 2` |

---

## 🔹 Permission-Based Search

| Command | Description |
|---------|-------------|
| `find . -perm 644` | Exact permission match |
| `find . -perm -u=x` | Files with execute permission for user |
| `find . -perm /111` | Any execute permission for user, group, or others |

---

## 🔹 Executing Commands on Results

| Command | Description |
|---------|-------------|
| `find . -name "*.log" -exec rm {} \;` | 🧹 Delete all `.log` files |
| `find . -type f -exec chmod 644 {} \;` | 🔐 Change permissions |
| `find . -exec md5sum {} \;` | 🔢 Generate MD5 checksums |

---

## 🔹 Logical Operations

| Symbol | Description | Example |
|--------|-------------|---------|
| `-a` | AND (default) | `find . -type f -name "*.sh" -a -size +1k` |
| `-o` | OR | `find . -name "*.jpg" -o -name "*.png"` |
| `!` / `-not` | NOT | `find . ! -name "*.txt"` |
| `\( \)` | Group expressions | `find . \( -name "*.log" -o -name "*.bak" \) -delete` |

---

## 🔹 Advanced Examples

```bash
find /home -type f -size +1G
# 🔍 Files larger than 1GB in /home

find . -name "*.zip" -mtime -30
# 🗃️ ZIP files modified in the last 30 days

find . -type f -empty
# 📭 Find empty files

find . -name "*.c" -exec gcc {} -o output \;
# 🛠️ Compile all C files

find . -name "*.log" -delete
# 🧹 Delete all log files

find . -type f -print0 | xargs -0 md5sum
# 🔄 Fast MD5 hashing using xargs
```

---

## ✅ Pro Tips

- Always use `-print` before `-exec` or `-delete` to verify results.
- Combine `find` with `xargs` for faster batch processing.
- Use `2>/dev/null` to suppress permission errors when searching across system directories.

---

📘 **Note**: Mastering the `find` command is essential for system administrators, penetration testers, and DevOps engineers. Keep experimenting!

---
