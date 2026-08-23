# OSINT Footprinting with Maltego

A hands-on demonstration of configuring Maltego Desktop and performing passive Open Source Intelligence (OSINT) reconnaissance on a target domain.

---

## 🛠️ Setup & Configuration

### 1. Prerequisites & Installation
* **Java Runtime:** Installed Java 17 (Eclipse Temurin JRE) as required by Maltego Desktop.
* **Maltego Setup:** Executed the installer and completed the initial setup wizard.

---

### 2. Account Registration & Activation
* Selected **Maltego ID (Online Activation)**.
* Accepted the License Agreement and completed browser-based OAuth authentication to activate the Community Edition license.

---

### 3. Data Source Synchronization
Synchronized the built-in transform hub and initialized standard entities and local transform sets.

<img width="1274" height="974" alt="Screenshot 2026-08-23 142512" src="https://github.com/user-attachments/assets/36a083ea-49ff-42d2-87f6-735264215d28" />

---

### 4. Privacy Mode Selection
* **Normal Mode (Selected):** Allows retrieving entity images and favicons for visual graph completeness during training.
* **Stealth Mode:** Prevents outbound requests from the local client IP to target infrastructure for sensitive investigations.

<img width="1180" height="438" alt="Screenshot 2026-08-23 142647" src="https://github.com/user-attachments/assets/aee23475-dd2b-4cdc-8b9e-d0b06e6a5b18" />

---

## 🔍 Domain Footprinting

### Target: `networkwalks.com`

1. **Entity Placement:** Created a new graph, added a `Domain` entity, and set the value to `networkwalks.com`.
2. **Transform Execution:** Executed `[Utilities] To Emails @domain [Search Engine]`.
3. **Reconnaissance Results:**
   * Harvested organization contact email: `info@networkwalks.com`.
   * Mapped linked search result nodes and child entities.

<img width="1918" height="1011" alt="Screenshot 2026-08-23 144126" src="https://github.com/user-attachments/assets/ef6efa6c-0bc9-4b41-9c0e-10e28718ce78" />

---

## ⚠️ Disclaimer
*For educational and authorized security research purposes only.*
