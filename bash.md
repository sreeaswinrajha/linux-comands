# 🐚 Bash Scripting Cheat Sheet

## 🧱 Basic Syntax

```bash
#!/bin/bash   # Shebang to specify Bash shell
# This is a comment
```

## 📦 Variables

```bash
name="John"
echo "Hello, $name"
```

- No space around `=`
- Access with `$name`
- Use `{}` for clarity: `${name}`

## 📝 User Input

```bash
read -p "Enter your name: " username
echo "Hi, $username"
```

## 🔁 Loops

### For Loop

```bash
for i in 1 2 3
do
  echo "Number: $i"
done
```

### While Loop

```bash
count=1
while [ $count -le 5 ]
do
  echo "Count: $count"
  ((count++))
done
```

### Until Loop

```bash
num=1
until [ $num -gt 3 ]
do
  echo "Until $num"
  ((num++))
done
```

## 🔂 Conditional Statements

### If-Else

```bash
if [ $age -ge 18 ]; then
  echo "Adult"
else
  echo "Minor"
fi
```

### Else If (elif)

```bash
if [ $x -lt 10 ]; then
  echo "Less than 10"
elif [ $x -eq 10 ]; then
  echo "Equal to 10"
else
  echo "Greater than 10"
fi
```

## 🔣 Operators

### Arithmetic

```bash
a=5
b=3
echo $((a + b))   # 8
echo $((a * b))   # 15
```

### Comparison

| Operator | Meaning         |
|----------|------------------|
| `-eq`    | Equal            |
| `-ne`    | Not equal        |
| `-gt`    | Greater than     |
| `-lt`    | Less than        |
| `-ge`    | Greater or equal |
| `-le`    | Less or equal    |

```bash
if [ "$a" -gt "$b" ]; then
  echo "$a is greater"
fi
```

## 📁 File Test Operators

```bash
-f file   # True if file exists and is a regular file
-d dir    # True if directory exists
-e file   # True if file exists
-r file   # Readable
-w file   # Writable
-x file   # Executable
```

```bash
if [ -f myfile.txt ]; then
  echo "File exists"
fi
```

## 🧰 Functions

```bash
greet() {
  echo "Hello, $1"
}

greet "Sree"
```

## 📤 Output and 📥 Input Redirection

```bash
echo "Hello" > file.txt      # Write
echo "More" >> file.txt      # Append

cat < file.txt               # Input from file
```

## 🔧 Command Substitution

```bash
today=$(date)
echo "Today is $today"
```

## 🗃️ Arrays

```bash
fruits=("apple" "banana" "cherry")
echo ${fruits[1]}    # banana
echo ${fruits[@]}    # all elements
```

## 🔀 Case Statement

```bash
read -p "Enter option: " option

case $option in
  1) echo "Option 1";;
  2) echo "Option 2";;
  *) echo "Invalid option";;
esac
```

## 🧹 Useful Shortcuts

| Shortcut | Description           |
|----------|-----------------------|
| `Ctrl + C` | Kill running command |
| `Ctrl + D` | Logout/EOF           |
| `Ctrl + Z` | Pause process        |
| `!!`       | Repeat last command  |
| `!abc`     | Run last command starting with abc |

## 📚 Script Example

```bash
#!/bin/bash

read -p "Enter your name: " name

if [ -z "$name" ]; then
  echo "You didn’t enter anything!"
else
  echo "Hello, $name!"
fi
```
