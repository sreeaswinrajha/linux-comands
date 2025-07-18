# 🛠️ Linux Command Cheatsheet

## 📦 Installing Applications

```bash
sudo apt-get install <package-name>
```

> Installs a package using APT (Advanced Package Tool).

---

## 📁 Listing Files

| Command | Description                             |
| ------- | --------------------------------------- |
| `ls`    | Lists contents of the current directory |
| `ls -l` | Lists with detailed information         |

---

## 📖 Help & Documentation

| Command             | Description                                                            |
| ------------------- | ---------------------------------------------------------------------- |
| `man <command>`     | Opens the manual page for a command (Use `/` to search inside manual)  |
| `<command> --help`  | Shows brief help info on how to use a command                          |
| `help`              | Lists shell built-ins and basic command info                           |
| `apropos <keyword>` | Searches manual page descriptions for a keyword (e.g., `apropos list`) |
| `stat <file>`       | Displays detailed status about a file or filesystem                    |

---

## 🧠 Keyboard Shortcuts (Bash Shell)

| Shortcut   | Action         |
| ---------- | -------------- |
| `Ctrl + A` | Move cursor to |

| **start of the line** |                                         |
| --------------------- | --------------------------------------- |
| `Ctrl + E`            | Move cursor to **end of the line**      |
| `Ctrl + U`            | Delete everything **before the cursor** |
| `Ctrl + K`            | Delete everything **after the cursor**  |

---

## ✏️ File Editing with `echo`

**Overwrite contents:**

```bash
echo "password123" > passwords
```

> Replaces all contents of the `passwords` file with `password123`.

**Append to file:**

```bash
echo "hloworld" >> passwords
```

> Adds `hloworld` to the end of the `passwords` file, keeping existing content.

---

## 📂 Move Executable to Global Directory

To make a CLI tool (like `caido`) accessible from anywhere:

```bash
sudo mv caido /usr/local/bin/
```

> 🔒 `sudo` is required because `/usr/local/bin/` is a **system-wide** directory for executables.

---

> ✨ Keep this file updated with useful command-line tricks for easy reference!
