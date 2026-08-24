# 🔍 Week 2 | Project Module 4: OSINT Footprinting with theHarvester

**Environment:** Kali Linux  
**Target:** `microsoft.com`  
**Category:** Passive Information Gathering / OSINT  

---

## 📌 Overview
This module demonstrates passive Open Source Intelligence (OSINT) footprinting using **theHarvester** on Kali Linux. The objective is to extract publicly exposed email addresses, subdomains, and host infrastructure details without directly interacting with the target's servers.

---

## 🛡️ Why Footprinting with theHarvester Matters

> theHarvester collects emails, sub-domains and hosts from dozens of public sources without ever touching the target directly. Each harvested email is a possible target for phishing and password attacks. Each sub-domain is another door into the organization that a defender may have forgotten about. Because the tool only reads public data, the target never knows it is being studied, which is exactly why this kind of passive recon is so powerful and so hard to detect. Defenders run the same tool on themselves to see what an attacker would see, and then reduce what they leak.

---

## 🛠️ Tool Syntax & Options

Reviewing the CLI parameters and supported OSINT search modules:

    ```bash
  theHarvester -h

## 🚀 Tasks & Execution

### 🔹 Task 1: Search Emails & Subdomains Using Baidu
* **Objective:** Query `microsoft.com` using the Baidu search engine with a limit of 1000 results[cite: 3].
* **Command:**
  ```bash
  theHarvester -d microsoft.com -l 1000 -b baidu
<img width="462" height="433" alt="Screenshot 2026-08-24 111852" src="https://github.com/user-attachments/assets/a99fb971-a2f5-4f7b-9eb6-768714806c90" />

### 🔹 Task 2: Search Emails & Subdomains Using Baidu
* **Objective:** Query `microsoft.com` using the Baidu search engine with a limit of 1000 results[cite: 3].
* **Command:**
  ```bash
  theHarvester -d microsoft.com -l 50 -b baidu
<img width="464" height="431" alt="Screenshot 2026-08-24 112128" src="https://github.com/user-attachments/assets/6b68c402-34b4-4538-a3b1-f837badda9aa" />
