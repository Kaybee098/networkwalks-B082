# OSINT Footprinting with Maltego

A hands-on demonstration of configuring Maltego Desktop and performing passive Open Source Intelligence (OSINT) reconnaissance on a target domain.

---

## 🛠️ Setup & Configuration

### 1. Data Source Synchronization
Completed the setup wizard and synchronized the built-in transform hub and standard entities.

<img width="1274" height="974" alt="Screenshot 2026-08-23 142512" src="https://github.com/user-attachments/assets/36a083ea-49ff-42d2-87f6-735264215d28" />

---

### 2. Privacy Mode
* **Normal Mode (Selected):** Allows retrieving entity images and favicons for graph completeness during lab training.
* **Stealth Mode:** Prevents local IP outbound requests for sensitive investigations.

<img width="1180" height="438" alt="Screenshot 2026-08-23 142647" src="https://github.com/user-attachments/assets/aee23475-dd2b-4cdc-8b9e-d0b06e6a5b18" />

---

## 🔍 Domain Footprinting

### Target: `networkwalks.com`

1. **Entity Placement:** Added the target `Domain` entity (`networkwalks.com`).
2. **Transform:** Executed `[Utilities] To Emails @domain [Search Engine]`.
3. **Results:**
   * Harvested contact email: `info@networkwalks.com`.
   * Mapped linked search result nodes.

<img width="1918" height="1011" alt="Screenshot 2026-08-23 144126" src="https://github.com/user-attachments/assets/ef6efa6c-0bc9-4b41-9c0e-10e28718ce78" />

---

## ⚠️ Disclaimer
*For educational and authorized security research purposes only.*
