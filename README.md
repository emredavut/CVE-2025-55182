### RSC/Next.js RCE Vulnerability Detector & PoC Chrome Extension

### CVE-2025-55182 & CVE-2025-66478

This repository contains a security research toolkit designed to **detect** and **demonstrate (PoC)** the recently disclosed RCE vulnerabilities affecting **React Server Components (RSC) / Next.js**.

The toolkit includes:

- **Chrome Extension** – Automatically detects vulnerable RSC/Next.js applications and provides a PoC trigger in authorized environments.
- **Shodan Detection Tool** – Searches for potentially vulnerable public hosts using Shodan scanning queries.
- **Proxy Helper (extension_proxy.py)** – Optional lightweight proxy to bypass CORS restrictions when interacting with remote targets during testing.

> ⚠️ **For educational and research purposes only.**  
> Do not use on systems you do not own or have explicit permission to test.

---

## Screenshots

![Screenshot 1](screen1.png)
![Screenshot 2](screen2.png)
![Screenshot 3](screen3.png)

---

## Installation & Usage

### **1. Load the Chrome Extension**

1. Open **chrome://extensions**
2. Enable **Developer Mode**
3. Click **Load unpacked**
4. Select the `chrome_extension/` folder

The extension will begin analyzing pages instantly.

---

### **2. (Optional but recommended) Run the CORS Proxy**

Some endpoints enforce strict CORS headers that block detection.  
Start the included proxy:

```bash
python extension_proxy.py
```

---

### **3. Use the Shodan Scanner**

```bash
python shodan_scanner.py
```

---

## mucq

---
