# Find Command in Linux

The `find` command is used to find files saved in the system.

---

## Basic Find Command

```bash
find -name hlo.txt
```

This command will show where `hlo.txt` is located.  
If the file exists in any user or directory, it will be displayed.

---

## Locate Command

`locate` is used to find files in the same directory.

---

## Avoiding Permission Denied Errors

To avoid `permission denied` errors, we can use:

```bash
2>/dev/null
```

Here, `null` acts like a dustbin where errors are discarded.

### Example

```bash
find -name hlo.txt 2>/dev/null
```

⚠️ There should be **no space** between `2>`.

---

## Search from Root Directory

```bash
find / -name hlo.txt
```

Searches for the file from the root (`/`) directory.

---

## Find All Text Files

```bash
find -name *.txt
```

Shows all `.txt` files.

---

## Command Summary

| Command | Result |
|-------|--------|
| `find` | Search for files |
| `/` | Search everywhere |
| `-name` | Search for specific name |
| `2>/dev/null` | Throw away errors |

