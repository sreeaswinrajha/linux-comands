
# Generating and Accessing a Website Using Python HTTP Server

This document explains how to **create a simple website server**, **access it**, and **interact with it using command-line tools** like `curl` and `wget`.  
Written in a clear, human‑friendly way for GitHub documentation.

---

## 🌐 Generate a Website Using Python

Python provides a built-in HTTP server module that can quickly host files from the current directory.

### Start the Server
```bash
python3 -m http.server
```

- Starts a web server in the **current directory**
- Default port: **8000**
- All files in the directory become accessible via browser

---

## 🔗 Access the Server Using Browser

```text
http://localhost:8000
```

- `localhost` → your own system
- `8000` → port number
- Displays the directory contents as a webpage

---

## 🔢 Use a Custom Port

You can assign your own port number:

```bash
python3 -m http.server 8080
```

Now access it using:
```text
http://localhost:8080
```

---

## 📂 What the Server Shows

- It displays **the directory where the command is run**
- HTML files open as web pages
- Other files can be downloaded

---

## 🧪 Access the Server Without a Browser

### Using `curl`

`curl` is used to access websites from the terminal.

```bash
curl localhost:8080
```

- Fetches and displays website content
- Useful for testing servers

---

## ⬇️ Download Files Using curl

```bash
curl -o hlo.html localhost:8080/hlo.html
```

- `-o` → output to file
- Downloads `hlo.html` from the server
- Saves it locally

---

## 📡 Check Website Communication (Headers)

```bash
curl -I localhost:8080
```

- Shows **HTTP response headers**
- Used to understand how the website communicates with the client
- Displays status codes, server type, content type, etc.

---

## 🔍 Verbose Mode (Detailed Communication)

```bash
curl -v localhost:8080
```

- `-v` → verbose
- Shows:
  - Request headers
  - Response headers
  - Connection details
- Useful for debugging and learning HTTP

---

## ⬇️ Download Files Using wget

```bash
wget localhost:8080
```

- Downloads files from a URL
- Saves content directly to local directory
- Often used for mirroring or bulk downloads

---

## 🧠 Summary

- `python3 -m http.server` → quick local web server
- `curl` → access and test websites via terminal
- `wget` → download files from websites
