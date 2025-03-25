# 🌐 Networking Basics — Detailed Explanations

---

## ✅ Step 1: Finding Local IP Address & Default Gateway

### ➡️ Windows (Command Prompt / PowerShell)

**Command:**
```powershell
ipconfig
```

**Example Output:**
```
Ethernet adapter Wi-Fi:
   IPv4 Address. . . . . . . . . . . : 192.168.1.100
   Default Gateway . . . . . . . . . : 192.168.1.1
```

**Key Information:**
- **IPv4 Address** → Your device’s local IP address on the network.
- **Default Gateway** → Your router’s IP address.

---

### ➡️ Raspberry Pi (Linux Terminal)

**Command to check local IP:**
```bash
ip a
```
**Example Output:**
```
3: wlan0: <UP,BROADCAST,RUNNING,MULTICAST> mtu 1500
    inet 192.168.1.150/24 brd 192.168.1.255 scope global dynamic wlan0
```
**Command to check default gateway:**
```bash
ip route | grep default
```
**Example Output:**
```
default via 192.168.1.1 dev wlan0
```

**Key Information:**
- **inet** → Raspberry Pi’s IP address.
- **default via** → The router (gateway) IP address.

---

### ✅ My Network Information

| Device        | Local IP        | Default Gateway |
|---------------|-----------------|-----------------|
| Windows       | `192.168.x.x`   | `192.168.x.1`   |
| Raspberry Pi  | `192.168.x.x`   | `192.168.x.1`   |

---

## ✅ Step 2: Testing Network Connectivity (Ping)

### ➡️ Windows
**Ping router:**
```powershell
ping [Your-Gateway-IP]
```
**Ping internet:**
```powershell
ping google.com
```

### ➡️ Raspberry Pi (Linux)
**Ping router:**
```bash
ping [Your-Gateway-IP]
```
**Ping internet:**
```bash
ping google.com
```

**Why use ping?**  
- To test if your computer can reach another device or website.  
- **How it helps:** Confirms if your network or internet connection is up.  
- **When to use:** When facing connection issues or verifying connectivity.  
- **Stop pinging:** Press `Ctrl + C` to stop.

---

## ✅ Step 3: DNS Resolution (nslookup)

### ➡️ Windows
**Command:**
```powershell
nslookup google.com
```

### ➡️ Raspberry Pi (Linux)
**Install if needed:**
```bash
sudo apt-get install dnsutils -y
```
**Command:**
```bash
nslookup google.com
```

**Why use nslookup?**  
- To check if DNS servers are translating domain names into IP addresses.  
- **How it helps:** Diagnoses DNS problems.  
- **When to use:** When websites don't load or DNS issues are suspected.

---

## ✅ Step 4: Advanced Networking Tools

---

### ➡️ `tracert` (Windows) / `traceroute` (Linux)

- **Why use this?** Shows each hop from your machine to the destination server.
- **How it helps:** Finds delays or failures in the network path.
- **When to use:** When websites are slow or unreachable.

**Windows:**
```powershell
tracert google.com
```
**Raspberry Pi:**
```bash
traceroute google.com
```
> Install with:
```bash
sudo apt-get install traceroute
```

---

### ➡️ `netstat`

- **Why use this?** Lists active network connections and listening ports.
- **How it helps:** Helps monitor active connections or security issues.
- **When to use:** For diagnostics or checking which ports are open.

**Windows:**
```powershell
netstat -an
```
**Raspberry Pi:**
```bash
netstat -tuln
```
> Install with:
```bash
sudo apt-get install net-tools
```

---

### ➡️ `curl`

- **Why use this?** Sends HTTP requests from the terminal.
- **How it helps:** Tests if websites or APIs respond.
- **When to use:** Verifying web server or API connectivity.

**Command (both systems):**
```bash
curl google.com
```

---

### ➡️ `dig` (Linux only)

- **Why use this?** Performs detailed DNS queries.
- **How it helps:** Provides more control and detailed DNS record info.
- **When to use:** For professional DNS diagnostics or advanced troubleshooting.

**Command:**
```bash
dig google.com
```
> Install with:
```bash
sudo apt-get install dnsutils
```

---

✨ **Continue adding commands and explanations as your networking knowledge grows!**
