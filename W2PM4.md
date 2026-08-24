

<img width="471" height="438" alt="Screenshot 2026-08-24 113319" src="https://github.com/user-attachments/assets/a57a2825-56ce-48a1-969c-beb6b094212c" />
<img width="478" height="432" alt="Screenshot 2026-08-24 113252" src="https://github.com/user-attachments/assets/c9ef738f-b484-4eee-9d78-9dbe0c61d761" />
<img width="464" height="431" alt="Screenshot 2026-08-24 112128" src="https://github.com/user-attachments/assets/6b68c402-34b4-4538-a3b1-f837badda9aa" />
<img width="469" height="416" alt="Screenshot 2026-08-24 111908" src="https://github.com/user-attachments/assets/7d2a0819-1960-4603-a63f-2163fdc63689" />
<img width="462" height="433" alt="Screenshot 2026-08-24 111852" src="https://github.com/user-attachments/assets/a99fb971-a2f5-4f7b-9eb6-768714806c90" />



# 🔍 Week 2 | Project Module 4: OSINT Footprinting with theHarvester

**Environment:** Kali Linux  
**Target:** `microsoft.com`  
**Category:** Passive Information Gathering / OSINT  

---

## 📌 Overview
This module demonstrates passive Open Source Intelligence (OSINT) footprinting using **theHarvester** on Kali Linux. The objective is to extract publicly exposed email addresses, subdomains, and host infrastructure details without directly interacting with the target's servers.

---

## 🛡️ Why Footprinting with theHarvester Matters

> theHarvester collects emails, sub-domains and hosts from dozens of public sources without ever touching the target directly. Each harvested email is a possible target for phishing and password attacks. Each sub-domain is another door into the organization that a defender may have forgotten about[cite: 3]. Because the tool only reads public data, the target never knows it is being studied, which is exactly why this kind of passive recon is so powerful and so hard to detect[cite: 3]. Defenders run the same tool on themselves to see what an attacker would see, and then reduce what they leak[cite: 3].

---

## 🛠️ Lab Setup & Preparation

### 🔹 Step 1: Launch theHarvester in Kali Linux
Open the Kali Linux application menu, search for **theHarvester**, and launch the tool[cite: 3].

<div align="center">
  <img width="462" height="433" alt="Screenshot 2026-08-24 111852" src="https://github.com/user-attachments/assets/a99fb971-a2f5-4f7b-9eb6-768714806c90" />
  <p><em>Figure 1: Locating and launching theHarvester from the Kali Linux applications menu[cite: 3].</em></p>
</div>

---

### 🔹 Step 2: Review Command Syntax & Options
Inspect the command options, query flags (`-d` for domain, `-l` for limit, `-b` for data source), and available search modules[cite: 3].

<div align="center">
  <img width="469" height="416" alt="Screenshot 2026-08-24 111908" src="https://github.com/user-attachments/assets/7d2a0819-1960-4603-a63f-2163fdc63689" />
  <p><em>Figure 2: Viewing theHarvester CLI help page and supported search engines[cite: 3].</em></p>
</div>

---

## 🚀 Tasks & Execution

### 🔹 Task 1: Search Emails & Subdomains Using Baidu
* **Objective:** Query `microsoft.com` using the Baidu search engine with a limit of 1000 results[cite: 3].
* **Command:**
  ```bash
  theHarvester -d microsoft.com -l 1000 -b baidu
