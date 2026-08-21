# 🔍 Week 2: Footprinting & Reconnaissance

This module covers passive information gathering and reconnaissance against a live target using standard Kali Linux utilities. The goal is to enumerate domain ownership, DNS records, server technologies, HTTP headers, and defensive controls without engaging in active exploitation.

---

## 🛠️ Tasks & Findings

### 🔹 Task 1: Domain Registration Enumeration (`whois`)
* **Objective:** Identify the registrar, creation/expiration timeline, abuse contacts, and authoritative name servers.
* **Key Finding:** Revealed domain registration through GoDaddy and hosting delegation to HostGator name servers (`NS56135.HOSTGATOR.COM` / `NS56136.HOSTGATOR.COM`).

<div align="center">
  <img width="624" height="289" alt="image" src="https://github.com/user-attachments/assets/cdadf47b-78d9-4708-bde7-fd939b3a7df2" />
  <p><em>Figure 1: WHOIS lookup output displaying GoDaddy registration, status flags, and HostGator name servers.</em></p>
</div>

---

### 🔹 Task 2: Web Technology Fingerprinting (`whatweb`)
* **Objective:** Fingerprint backend servers, content management systems (CMS), plugins, and UI frameworks.
* **Key Finding:** Identified an Apache web server, WordPress 7.0.4 CMS, WordPress Download Manager (v3.3.58), jQuery 3.7.1, and an administrative contact email.

<div align="center">
  <img width="624" height="425" alt="image" src="https://github.com/user-attachments/assets/73aa9f1d-8997-49ee-ba59-a5a58af2d036" />
  <p><em>Figure 2: WhatWeb scan output identifying Apache, WordPress version, plugins, and server IP address.</em></p>
</div>

---

### 🔹 Task 3: DNS Address Resolution (`nslookup`)
* **Objective:** Map the target domain name to its direct public IPv4 address.
* **Key Finding:** Successfully resolved `networkwalks.com` to host IP `192.232.216.135`.

<div align="center">
  <img width="624" height="251" alt="image" src="https://github.com/user-attachments/assets/71fda73b-d711-4e37-83ab-2796d207dc53" />
  <p><em>Figure 3: DNS resolution query using nslookup returning host IP 192.232.216.135.</em></p>
</div>

---

### 🔹 Task 4: HTTP Response Header Analysis (`curl -I`)
* **Objective:** Inspect HTTP response headers to uncover server software, caching layers, cookies, and hidden API routes.
* **Key Finding:** Discovered active HTTP/2 protocol, Apache server banner, Nginx caching (`x-nginx-cache: WordPress`), and exposed WordPress REST API endpoints (`/wp-json/`).

<div align="center">
  <img width="624" height="287" alt="image" src="https://github.com/user-attachments/assets/750376af-159d-4c89-a8ca-0e2f12f8eaaa" />
  <p><em>Figure 4: HTTP response headers revealing web server details, caching configuration, and REST API links.</em></p>
</div>

---

### 🔹 Task 5: Web Application Firewall Detection (`wafw00f`)
* **Objective:** Check if incoming web requests are monitored or filtered by a Web Application Firewall (WAF).
* **Key Finding:** Target site is actively protected by **ModSecurity (SpiderLabs) WAF**.

<div align="center">
  <img width="624" height="288" alt="image" src="https://github.com/user-attachments/assets/73a3909d-edad-4645-8db0-8f3592929900" />
  <p><em>Figure 5: WAF fingerprinting confirming active protection by ModSecurity (SpiderLabs).</em></p>
</div>

---

### 🔹 Task 6: Full DNS Footprinting (`dnsrecon`)
* **Objective:** Enumerate complete zone records including SOA, NS, MX, TXT (SPF), and service (SRV) endpoints.
* **Key Finding:** Mapped mail server routing (`mail.networkwalks.com`), Bind DNS version `9.16.23-RH`, SPF authentication policy, and multiple cPanel autodiscover SRV records.

<div align="center">
  <img width="624" height="542" alt="image" src="https://github.com/user-attachments/assets/f36c8dc8-73ac-4d66-bb43-fc14c1dd3075" />
  <p><em>Figure 6: Complete DNS record enumeration revealing MX, TXT (SPF), Bind versions, and SRV records.</em></p>
</div>
