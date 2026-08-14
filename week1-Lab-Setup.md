# 🛡️ Cybersecurity & Ethical Hacking Lab Setup

---

## 📌 Phase 1: Environment & Kali Linux Setup

### 🔹 Step 1: Install 7-Zip
Download and install the latest version of **7-Zip** to extract archive files:
* **Download:** [7-Zip Official Site](https://7-zip.org/download.html)

---

### 🔹 Step 2: Install VirtualBox
Download and install **Oracle VM VirtualBox** on your host operating system:
* **Download:** [VirtualBox Downloads](https://www.virtualbox.org/wiki/Downloads)

---

### 🔹 Step 3: Configure VirtualBox NAT Network
Create an isolated **NAT Network** with the CIDR block `10.0.0.0/24` to allow inter-VM communication and controlled outbound internet access.

<div align="center">
  <img src="https://github.com/user-attachments/assets/f77d4031-82ca-42dc-8dc0-a6f4789bd2ec" alt="Configure 10.0.0.0/24 Subnet" width="85%" />
  <p><em>Figure 1: Configuring Subnet CIDR (10.0.0.0/24)</em></p>
</div>

<div align="center">
  <img src="https://github.com/user-attachments/assets/12285dbc-1410-4f5d-a79f-99082d1ec7d8" alt="Create NAT Network" width="85%" />
  <p><em>Figure 2: Creating the NAT Network</em></p>
</div>

---

### 🔹 Step 4: Import Kali Linux VM
Download the pre-built VirtualBox image for **Kali Linux** and import it (`.ova` / `.vbox`):
* **Download:** [Kali Linux Virtual Machines](https://kali.org/get-kali)

---

### 🔹 Step 5: Configure Kali Linux Network & IP
Attach the VM network adapter to your newly created **NAT Network** and verify IP assignment inside the guest system.

<div align="center">
  <img src="https://github.com/user-attachments/assets/b0dad2ee-72e7-474a-a387-75a9ef244f5d" alt="Kali VM Network Adapter Settings" width="85%" />
  <p><em>Figure 3: Setting Adapter to NAT Network</em></p>
</div>

<div align="center">
  <img src="https://github.com/user-attachments/assets/7847830e-2356-45a0-b767-157f2d0c8d11" alt="Kali IP Configuration Verification" width="50%" />
  <p><em>Figure 4: Verifying IP Assignment</em></p>
</div>

---

### 🔹 Step 6: Create a Base VM Snapshot
Take a snapshot of your clean Kali installation so you can revert back at any time.

<div align="center">
  <img src="https://github.com/user-attachments/assets/8a713348-ffb4-4521-8184-e943760be4cf" alt="Take VM Snapshot Action" width="65%" />
  <p><em>Figure 5: Initiating the Base Snapshot</em></p>
</div>

<div align="center">
  <img src="https://github.com/user-attachments/assets/4c565de3-7bb3-447b-9cea-4529f509c5ea" alt="Snapshot Tree and Overview" width="90%" />
  <p><em>Figure 6: Confirmed Snapshot in VirtualBox Manager</em></p>
</div>
