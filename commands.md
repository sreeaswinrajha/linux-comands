
# Basic Linux Commands – Notes (GitHub Ready)

This document contains **basic Linux commands and shortcuts**, written in simple language for beginners.  
It is suitable for **GitHub README / Linux notes repository**.

---

## 📦 Installing an Application

```bash
sudo apt-get install <package-name>
```

- `sudo` → run command as administrator  
- `apt-get` → package manager  
- `<package-name>` → name of the software

---

## 📝 Creating a File

```bash
touch hlo.txt
```

Creates an empty file named `hlo.txt`.

---

## 📂 Listing Directory Contents

```bash
ls
```
- Lists files and folders in the current directory

```bash
ls -l
```
- Shows detailed information (permissions, size, owner, date)

---

## 🔗 Alias Command

Alias is used to create a **custom command**.

```bash
alias hlo="ls"
```

Now, typing `hlo` will execute `ls`.

---

## 📖 Help & Manual Commands

### `man` – Manual Pages
```bash
man ls
```
- Shows full manual of a command  
- Press `/` to search inside manual

### `--help`
```bash
ls --help
```
- Shows short help information

### `apropos`
```bash
apropos list
```
- Finds commands related to a keyword

### `stat`
```bash
stat file.txt
```
- Displays file or filesystem status

---

## ⌨️ Cursor Movement Shortcuts

| Shortcut | Action |
|--------|-------|
| `Ctrl + A` | Move cursor to start of line |
| `Ctrl + E` | Move cursor to end of line |
| `Ctrl + U` | Delete before cursor |
| `Ctrl + K` | Delete after cursor |

---

## ⚙️ Important Linux Directories

| Directory | Purpose |
|---------|--------|
| `/etc` | Configuration files |
| `/bin` | Common user commands |
| `/sbin` | System/admin commands |
| `/lib` | Shared libraries |

---

## 📁 Working with Directories

### Handling Spaces in Folder Names

```bash
cd exercise/file
```
(Used when folder name has space)

### Navigation Commands

```bash
cd ..
```
- Go back one directory

```bash
cd ../../
```
- Go back multiple directories

```bash
cd -
```
- Switch between last two directories

---

## 🛠️ File & Directory Operations

### Create Directory
```bash
mkdir newfolder
```

### Remove Empty Directory
```bash
rmdir newfolder
```

### Copy Files
```bash
cp rem.txt rem1.txt
```

### Move File
```bash
mv bug.py Downloads
```

### Rename File
```bash
mv Downloads/bug.py Downloads/new.py
```

---

## 📑 Working with Multiple Files

### Using Wildcards (`*`)

```bash
mv *.txt document/textfiles
```
- Moves all `.txt` files to target directory

---

## ❌ Delete Directory Recursively

```bash
rm -r text
```

- Deletes directory and all its contents  
⚠️ Use carefully – no undo!

---

