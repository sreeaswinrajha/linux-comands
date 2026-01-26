
# Network Commands in Linux

## View IP Address

```bash
ip a
```

```bash
ifconfig
```

---

## Network Connections

```bash
netstat
```
Used to see what connections are ON and connected  
(example: sending or receiving data)

```bash
route
```
Shows connection routes (where it can connect)

---

## Network Management

Turn ON networking:
```bash
sudo nmcli networking on
```

NetworkManager service:
```bash
sudo service NetworkManager start
sudo service NetworkManager restart
sudo service NetworkManager stop
```

Change adapter connection:
- NAT
- Bridge

---

## Open Ports and Connections

```bash
netstat -nano
```
Shows:
- Open ports
- Active connections

---

## Add IP and DNS Entry

```bash
echo "ip dns" | sudo tee -a /etc/hosts
```

`tee` is run with `sudo`, while redirection (`>`) is handled by the shell before `sudo` is applied.

