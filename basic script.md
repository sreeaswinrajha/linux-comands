
# Extract IP Address from `ping` Output (Linux & Python)

This guide explains how to extract IP addresses from a `ping` command output using **Linux shell tools** and **Python**.  
It is written in clean **Markdown** format, suitable for **GitHub README / documentation**.

---



## 📄 Sample Input File (`ip.txt`)

```
64 bytes from 192.168.43.126: icmp_seq=1 ttl=64 time=2.3 ms
64 bytes from 192.168.43.126: icmp_seq=2 ttl=64 time=2.1 ms
Request timeout for icmp_seq 3
```

---

## 🛠️ Solution Using Linux Commands

### Command
```bash
cat ip.txt | grep "64 bytes" | cut -d " " -f 4 | tr -d ":"
```

### Command Breakdown

- **`cat ip.txt`**  
  Reads the file content

- **`grep "64 bytes"`**  
  Filters only lines containing successful ping replies

- **`cut -d " " -f 4`**  
  - `-d " "` → Space is the delimiter  
  - `-f 4` → Extracts the 4th field (IP address with colon)

- **`tr -d ":"`**  
  Removes the colon (`:`) from the IP address

### Output
```
192.168.43.126
192.168.43.126
```


## ⚡ Alternative One-Liner (Linux)

```bash
grep "64 bytes" ip.txt | awk '{gsub(":", "", $4); print $4}'
```

