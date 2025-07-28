# 🖥️ Step 1: Virtualization & OS Deployment

## ✅ Objective
This lab demonstrates my ability to work with virtualization technologies

---

## 🔧 Tools Used
- **VirtualBox** (Type-2 Hypervisor)
- **Windows 10 ISO** (Evaluation Version)
- **Ubuntu Desktop ISO**

---

## 🏗️ Overview of What I Did
I created two virtual machines:
- `Win10-Lab` running Windows 10
- `Ubuntu-Lab` running Ubuntu Linux

Each VM is configured with two types of virtual network adapters:
1. **NAT (Network Address Translation)** – allows outbound internet access from the VM via the host.
2. **Host-Only Adapter** – allows communication between VMs and the host machine, but isolates traffic from the external network (secure for lab simulations).

---

### 🔹 NAT Adapter
- **Purpose:** Allows the VM to access the internet.
- **How it works:** The VM shares the host’s IP address to reach external networks.
- **Example Use Case:** Download updates or software from the internet.

### 🔸 Host-Only Adapter
- **Purpose:** Enables communication between the host and VMs, and between VMs themselves, without internet access.
- **How it works:** A virtual network is created by VirtualBox, often with IP ranges like `192.168.56.x`.
- **Example Use Case:** Isolated test environment or private file sharing.

---

## 🔍 Key Commands & Tests

| Test                         | Command                        | OS         | Result                                 |
|------------------------------|---------------------------------|------------|----------------------------------------|
| Check IP Address             | `ipconfig /all` or `ip a`       | Both       | Confirms network adapters assigned     |
| Ping Internet (Google DNS)   | `ping 8.8.8.8`                  | Both       | Validates NAT adapter functionality    |
| Ping Host from VM            | `ping [host IP]`                | Both       | Verifies host-only adapter is working  |
| Ping VM-to-VM                | `ping [other VM's host-only IP]`| Both       | Confirms inter-VM communication        |

---

## 📸 Included Files
- `vm-settings.png` – Screenshots of VM and network adapter settings
- `ping-test.png` – Successful ping results for verification
- `ipconfig.txt` – Windows IP config output
- `ifconfig.txt` – Ubuntu IP config output

---

➡️ [Next lab: Storage & Partitioning](../02-Storage/)
