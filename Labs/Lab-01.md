
---

## Cisco Lab 01 - Basic Network Topology


### Lab Overview

This lab demonstrates a basic network topology using Cisco Packet Tracer. It showcases how two separate LANs communicate through a central router.

---

### Network Configuration
<img width="846" height="415" alt="image" src="https://github.com/user-attachments/assets/9d5a1ec9-7198-4c00-ad3a-2cc497f0ebd1" />

| Device | Interface | IP Address     | Description          |
| ------ | --------- | -------------- | -------------------- |
| Router | G0/0      | `192.168.1.1`  | Gateway for LAN 1    |
| Router | G0/1      | `192.168.2.1`  | Gateway for LAN 2    |
| PC0    | Fa0       | `192.168.1.10` | Connected to Switch0 |
| PC1    | Fa0       | `192.168.1.11` | Connected to Switch0 |
| PC2    | Fa0       | `192.168.2.10` | Connected to Switch1 |
| PC3    | Fa0       | `192.168.2.11` | Connected to Switch1 |

### Router Configuration Setup
<img width="634" height="339" alt="image" src="https://github.com/user-attachments/assets/d1bc9ab4-6b5e-4448-bf41-b698c8d6d2dd" />

### Router Configuration Commands
Router> enable

* **Enter global configuration mode**:
*Router# configure terminal
*Enter configuration commands, one per line. End with CNTL/Z.

* **Configure GigabitEthernet0/0 for LAN 1 with IP 192.168.1.1/24**:
*Router1(config)# interface GigabitEthernet0/0
*Router1(config-if)# ip address 192.168.1.1 255.255.255.0
*Router1(config-if)# no shutdown   # Activates the interface
*Router1(config-if)# exit

* **Configure GigabitEthernet0/1 for LAN 1 with IP 192.168.2.1/24**:
   * Router1(config)# interface GigabitEthernet0/1
   *Router1(config-if)# ip address 192.168.2.1 255.255.255.0
*Router1(config-if)# no shutdown   # Activates the interface
*Router1(config-if)# exit

* **Exit configuration mode**:
Router1(config)# end

* **(Optional) Save your configuration to NVRAM**:
Router1# write memory

---

### Logical Layout

* **Left Side (LAN 1)**:

  * PC0 and PC1 connect to **Switch0**
  * Switch0 uplinks to router’s **G0/0 (192.168.1.1)**

* **Right Side (LAN 2)**:

  * PC2 and PC3 connect to **Switch1**
  * Switch1 uplinks to router’s **G0/1 (192.168.2.1)**

---

### How It Works

1. **Router provides routing** between two different subnets: `192.168.1.0/24` and `192.168.2.0/24`.
2. Devices in each LAN can **communicate within their subnet**.
3. With correct configuration, **PCs from different LANs can communicate** via the router.

---

### Testing On PC1

<img width="699" height="381" alt="image" src="https://github.com/user-attachments/assets/000f5e9d-663f-4be3-8dee-ee3855eeaa5c" />


## Sending messages
<img width="535" height="101" alt="image" src="https://github.com/user-attachments/assets/349529e6-0b61-469b-b15e-3a0b104fdc54" />



---

### ✅ Learning Objectives

* ✔️ Understand basic LAN-to-LAN communication
* ✔️ Practice assigning static IPs
* ✔️ Configure a router for inter-VLAN routing
* ✔️ Learn network segmentation using switches

---

