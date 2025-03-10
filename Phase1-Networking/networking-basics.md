# 🌐 Networking Basics

## 📌 Step 1: Finding Local IP Address & Default Gateway  

### 🖥️ **Windows (Command Prompt / PowerShell)**  
To check the **local IP address** and **default gateway** on Windows, run:  

```powershell
ipconfig
```

📌 **Output Example:**  
```
Ethernet adapter Wi-Fi:
   IPv4 Address: 192.168.1.100
   Default Gateway: 192.168.1.1
```

📌 **Key Information:**  
- **IPv4 Address** → Your device’s **local** network IP.  
- **Default Gateway** → Your **router’s IP**, used to communicate with external networks.  

---

### 🍓 **Raspberry Pi (Linux Terminal)**  
To check the **local IP address** on Raspberry Pi, run:  

```bash
ip a
```

📌 **Output Example:**  
```
3: wlan0: <UP,BROADCAST,RUNNING,MULTICAST> mtu 1500
   inet 192.168.1.150/24 brd 192.168.1.255 scope global dynamic wlan0
```

To find the **default gateway**, run:  
```bash
ip route | grep default
```
📌 **Output Example:**  
```
default via 192.168.1.1 dev wlan0
```

📌 **Key Information:**  
- **inet** → Raspberry Pi’s **local** network IP.  
- **Default Gateway** → The router’s IP (e.g., `192.168.1.1`).

---

### ✅ **My Network Information**  
| Device       | Local IP        | Default Gateway |
|-------------|----------------|----------------|
| Windows     | `192.168.x.x`   | `192.168.x.1`  |
| Raspberry Pi | `192.168.x.x`   | `192.168.x.1`  |

📌 **These addresses are used to identify devices on the same network and troubleshoot connectivity issues.**

---

🚀 **Next Step:** [Testing Network Connectivity (Step 2)]  
```
