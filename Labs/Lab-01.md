Networking-Basics
Here’s an interactive and engaging version of your `README.md` file section for the image you shared, with Markdown formatting and emojis to guide the reader:

---

## 🧪 Cisco Lab 01 - Basic Network Topology

![Network Topology](./624c9e09-9cbb-4736-84f8-92d40f5f4ab1.png)

### 🖥️ Lab Overview

This lab demonstrates a basic network topology using Cisco Packet Tracer. It showcases how two separate LANs communicate through a central router.

---

### 🔧 Network Configuration
                      <img width="846" height="415" alt="image" src="https://github.com/user-attachments/assets/9d5a1ec9-7198-4c00-ad3a-2cc497f0ebd1" />

| Device | Interface | IP Address     | Description          |
| ------ | --------- | -------------- | -------------------- |
| Router | G0/0      | `192.168.1.1`  | Gateway for LAN 1    |
| Router | G0/1      | `192.168.2.1`  | Gateway for LAN 2    |
| PC0    | Fa0       | `192.168.1.10` | Connected to Switch0 |
| PC1    | Fa0       | `192.168.1.11` | Connected to Switch0 |
| PC2    | Fa0       | `192.168.2.10` | Connected to Switch1 |
| PC3    | Fa0       | `192.168.2.11` | Connected to Switch1 |

---

### 🌐 Logical Layout

* **Left Side (LAN 1)**:

  * PC0 and PC1 connect to **Switch0**
  * Switch0 uplinks to router’s **G0/0 (192.168.1.1)**

* **Right Side (LAN 2)**:

  * PC2 and PC3 connect to **Switch1**
  * Switch1 uplinks to router’s **G0/1 (192.168.2.1)**

---

### 🛠️ How It Works

1. **Router provides routing** between two different subnets: `192.168.1.0/24` and `192.168.2.0/24`.
2. Devices in each LAN can **communicate within their subnet**.
3. With correct configuration, **PCs from different LANs can communicate** via the router.

---

### 🧪 Try It Yourself!

```bash
# On PC0
ping 192.168.1.11   # Should succeed (same LAN)
ping 192.168.2.10   # Should succeed (via router)

# On PC2
ping 192.168.2.11   # Should succeed (same LAN)
ping 192.168.1.10   # Should succeed (via router)
```
                       <img width="535" height="101" alt="image" src="https://github.com/user-attachments/assets/f9f1007c-2671-4114-9fd4-66357d15ef08" />

---

### ✅ Learning Objectives

* ✔️ Understand basic LAN-to-LAN communication
* ✔️ Practice assigning static IPs
* ✔️ Configure a router for inter-VLAN routing
* ✔️ Learn network segmentation using switches

---

Let me know if you want to add **routing commands**, **subnetting explanation**, or **export the .pkt file** reference too.
