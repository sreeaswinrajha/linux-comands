
# Linux File Creation, Movement, Copying & Editing Commands

This document covers **basic Linux file operations**, **editing tools**, and **useful utilities**, written in clean **Markdown (`.md`)** format suitable for GitHub.

---

## 📁 Create, Move & Copy Operations

### Create a New File
```bash
touch file.txt
```
Creates an empty file.

### Create a New Directory
```bash
mkdir newdir
```

### Move or Rename Files / Directories
```bash
mv info.txt information.txt
```
- Moves a file OR renames it

```bash
mv file.txt Downloads/
```
Moves file to another directory.

---

### Remove Files

```bash
rm file.txt
```
Deletes a file.

### Remove Multiple Files by Extension
```bash
rm *.php
```
Deletes all files ending with `.php`.

⚠️ **Warning:** Deleted files cannot be recovered.

---

## 📝 Editing & Viewing Files

### Graphical Editor
```bash
gedit file.txt
```
Opens file in GUI editor.

### Terminal Editors

| Command | Description |
|------|------------|
| `nano` | Simple terminal editor |
| `vim` | Advanced editor (exit using `:q`) |
| `cat` | View file content |

---

## 🔍 File Viewing & Processing Tools

After using `cat`, output can be piped to:

- `more` → Paginated view
- `less` → Scrollable view
- `head` → First 10 lines
- `tail` → Last 10 lines
- `sort` → Sort content
- `grep` → Search text
- `cut` → Extract columns
- `column` → Align output

Example:
```bash
cat file.txt | grep "error"
```

---

## 🔢 Word Count

```bash
wc file.txt
```
Counts:
- Lines
- Words
- Characters

---

## 📢 Echo Command

### Create a File with Content
```bash
echo "hello" > he.txt
```

### Append Content
```bash
echo "world" >> he.txt
```

---

## 🔎 Find Command

Used to search for files in directories.

```bash
find ./directory/ -name filename
```

Example:
```bash
find ./Documents -name notes.txt
```

---

## ✅ Notes

- Use `nano` for beginners
- Use `vim` for advanced editing
- Combine commands using pipes (`|`) for power usage
