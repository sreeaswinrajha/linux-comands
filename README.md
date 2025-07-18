# 🛠️ Linux Command Cheatsheet

## 📦 Installing Applications

```bash
sudo apt-get install <package-name>
```

> Installs a package using APT (Advanced Package Tool).

## 📄 Create a File

```bash
touch hlo.txt
```

> Creates a new empty file named `hlo.txt`.

---

## 📁 Listing Files

| Command | Description                             |
| ------- | --------------------------------------- |
| `ls`    | Lists contents of the current directory |
| `ls -l` | Lists with detailed information         |

---

## ⛓️ Aliases

```bash
alias hlo="ls"
```

> Creates a custom shortcut command `hlo` that performs `ls`.

---

## 📖 Help & Documentation

| Command             | Description                                                              |
| ------------------- | ------------------------------------------------------------------------ |
| `man <command>`     | Opens the manual page for a command (use `/` to search)                  |
| `<command> --help`  | Displays brief help for the command                                      |
| `help`              | Lists built-in shell commands and syntax                                 |
| `apropos <keyword>` | Searches command descriptions matching the keyword (e.g. `apropos list`) |
| `stat <file>`       | Shows detailed information about a file or filesystem                    |

---

## 🧠 Bash Shortcuts

| Shortcut   | Action                                  |
| ---------- | --------------------------------------- |
| `Ctrl + A` | Move cursor to **start** of the line    |
| `Ctrl + E` | Move cursor to **end** of the line      |
| `Ctrl + U` | Delete everything **before** the cursor |
| `Ctrl + K` | Delete everything **after** the cursor  |

---

## 📂 Important System Paths

| Path            | Description                       |
| --------------- | --------------------------------- |
| `/etc`          | Common system configuration files |
| `/bin`, `/sbin` | Essential user/system binaries    |
| `/lib`          | Shared library files              |

---

## 📁 Navigating Directories

* Use `cd` to change directory.
* To access a space-separated folder like `exercise file`, use:

  ```bash
  cd exercise\ file
  ```
* To go back one level:

  ```bash
  cd ..
  ```
* To go back two or more levels:

  ```bash
  cd ../../
  ```
* To switch between two directories:

  ```bash
  cd -
  ```

---

## 🗂️ File Operations

| Command                      | Description                                  |
| ---------------------------- | -------------------------------------------- |
| `mkdir newfolder`            | Create a new directory                       |
| `rmdir newfolder`            | Remove an empty directory                    |
| `cp file.txt backup.txt`     | Copy a file                                  |
| `mv file.txt folder/`        | Move file to folder                          |
| `mv oldname.txt newname.txt` | Rename a file                                |
| `mv *.txt folder/`           | Move all `.txt` files to a folder            |
| `rm -r folder/`              | Delete a folder and its contents recursively |

---

## 🧵 Process Management

| Command           | Description                        |
| ----------------- | ---------------------------------- |
| `ps -u <user>`    | List processes for a specific user |
| `pgrep <program>` | Find process ID of a program       |
| `kill <PID>`      | Kill a process by ID               |
| `pkill -9 <name>` | Force kill all processes by name   |
| `top`, `htop`     | Real-time process monitor          |
| `Ctrl + Z`        | Pause current foreground job       |
| `bg`              | Move paused job to background      |
| `fg`              | Bring background job to foreground |

---

## 🔒 File Permissions & Ownership

| Symbol | Meaning |
| ------ | ------- |
| `r`    | Read    |
| `w`    | Write   |
| `x`    | Execute |

Example output from `ls -l`:

```bash
drwxr-xr-x
```

* Owner: `rwx`
* Group: `r-x`
* Others: `r-x`

Change permissions:

```bash
chmod 777 file.txt
```

> Grants read, write, and execute to everyone.

---

## 👥 User & Group Management

```bash
adduser aswin         # Create new user
userdel aswin         # Delete user
sudo groupadd family  # Create new group
```

Important files:

* `/etc/passwd` → All users
* `/etc/shadow` → Passwords in hashed form
* `/etc/group` → Group details

Other Commands:

```bash
sudo passwd <username>  # Set password for a user
usermod <options>       # Modify user settings
sudo visudo             # Modify sudoers file for permissions
```

---

## 🌐 Hosting a Simple Website with Python

Start HTTP server:

```bash
python3 -m http.server 8000
```

* Access via browser: `http://localhost:8000`
* Change port by replacing `8000`

---

## 🌐 Interact with Web Servers from CLI

Use `curl` to access websites:

```bash
curl http://localhost:8080
```

Download files with `curl`:

```bash
curl -o file.html http://localhost:8080
```

Inspect response headers:

```bash
curl -I http://localhost:8080
```

Verbose (detailed request info):

```bash
curl -v http://localhost:8080
```

Use `wget` to download:

```bash
wget http://localhost:8080/file.txt
```

---

## 🧰 Common Hacking Tools

| Tool     | Purpose            |
| -------- | ------------------ |
| `crunch` | Generate wordlists |
| `hydra`  | Password cracking  |
| `john`   | Hash cracking      |

---

## 🧪 Extracting IPs from Ping Output (Example)

```bash
cat ip.txt | grep "64 bytes" | cut -d " " -f 4 | tr -d ":"
```

> Extracts clean IP addresses from `ping` output in `ip.txt`

---



## 📂 Move Executable to Global Directory

To make a CLI tool (like `caido`) accessible from anywhere:

```bash
sudo mv caido /usr/local/bin/
```

> 🔒 `sudo` is required because `/usr/local/bin/` is a **system-wide** directory for executables.

---


