
# Linux Permissions, Users, and Groups

## File Permissions

- **r** → read  
- **w** → write  
- **e** → execute  

The privileges allowed show what operations can be performed.

```bash
ls -l
```

### Example

```
drwxr-xr-x
```

Three groups in permissions:

- **rwx** → owner  
- **r-x** → group of user  
- **r-x** → all users  

---

## /tmp Directory

```text
/tmp
```

Has full access.

---

## Change File Permissions

```bash
chmod
```
Used to change the mode of operation (file access permissions).

### Example

```bash
chmod 777 helo.txt
```

Gives read, write, and execute permissions to all users.

---

## User Management

### Add User

```bash
adduser aswin
```

Creates a new user named `aswin`.

### Delete User

```bash
userdel aswin
```

Deletes the user `aswin`.

---

## Group Management

```bash
sudo groupadd family
```

Adds a new group named `family`.

---

## Important System Files

```text
/etc/passwd
```
Shows all users.

```text
/etc/shadow
```
Stores passwords in hash format.

```text
/etc/group
```
View group details.

---

## User and Group Commands

```bash
adduser
```
Used to create a new user and group.

```bash
useradd
```
Add user to a group.

```bash
sudo passwd ironman
```
Assigns password to the user `ironman`.

```bash
usermod
```
Used to modify user settings.

---

## Sudo Permissions

```bash
sudo visudo
```

Used to change user permissions.
