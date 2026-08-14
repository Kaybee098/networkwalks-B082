# 🛡️ Cybersecurity Lab Setup

---

## 📌 Phase 1: Kali Linux Setup

### 🔹 Step 1: Install 7-Zip
Download and install **7-Zip** to extract zipped files:
* **Link:** [Download 7-Zip](https://7-zip.org/download.html)

---

### 🔹 Step 2: Install VirtualBox
Download and install **VirtualBox** to run virtual machines on your computer:
* **Link:** [Download VirtualBox](https://www.virtualbox.org/wiki/Downloads)

---

### 🔹 Step 3: Create a NAT Network
Set up a private network (`10.0.0.0/24`) so your virtual machines can talk to each other safely.

<div align="center">
  <img src="https://github.com/user-attachments/assets/f77d4031-82ca-42dc-8dc0-a6f4789bd2ec" alt="Set Network Subnet" width="85%" />
  <p><em>1. Set the IPv4 Prefix to <code>10.0.0.0/24</code></em></p>
</div>

<div align="center">
  <img src="https://github.com/user-attachments/assets/12285dbc-1410-4f5d-a79f-99082d1ec7d8" alt="Add NAT Network" width="85%" />
  <p><em>2. Save and apply the new NAT Network</em></p>
</div>

---

### 🔹 Step 4: Download Kali Linux
Download the ready-to-use **Kali Linux** virtual machine file and open it in VirtualBox:
* **Link:** [Download Kali Linux VM](https://kali.org/get-kali)

---

### 🔹 Step 5: Connect Kali to the Network
Set Kali's network adapter to use your NAT Network, then start the machine and check that it receives an IP address.

<div align="center">
  <img src="https://github.com/user-attachments/assets/b0dad2ee-72e7-474a-a387-75a9ef244f5d" alt="Select NAT Network" width="85%" />
  <p><em>1. Set Adapter 1 to <b>NAT Network</b></em></p>
</div>

<div align="center">
  <img src="https://github.com/user-attachments/assets/7847830e-2356-45a0-b767-157f2d0c8d11" alt="Check IP Address" width="50%" />
  <p><em>2. Confirm you have a <code>10.0.0.x</code> IP address</em></p>
</div>

---

### 🔹 Step 6: Save a Snapshot
Take a snapshot of your fresh setup. This lets you restore Kali anytime if something breaks during practice.

<div align="center">
  <img src="https://github.com/user-attachments/assets/8a713348-ffb4-4521-8184-e943760be4cf" alt="Click Take Snapshot" width="65%" />
  <p><em>1. Click <b>Take</b> to create a snapshot</em></p>
</div>

<div align="center">
  <img src="https://github.com/user-attachments/assets/4c565de3-7bb3-447b-9cea-4529f509c5ea" alt="Snapshot Created" width="90%" />
  <p><em>2. Snapshot saved successfully</em></p>
</div>
