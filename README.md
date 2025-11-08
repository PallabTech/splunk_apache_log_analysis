# 🧾 Apache Log Analysis & Malicious Activity Detection using Splunk

### 🔍 Project Overview
This project demonstrates how to monitor, analyze, and detect security events from **Apache web server logs** using **Splunk Enterprise (v10.1.2507.10)**.  
The system identifies abnormal traffic patterns, web attacks, and potential security risks through automated SPL-based dashboards.

---

## 🚀 Dashboards Developed

### 1️⃣ Apache Web Traffic Monitoring
- Tracks total web requests, top IPs, and HTTP status code trends.
- Includes a **global traffic map** showing user origins.
- SPL examples:
  ```spl
  index=main sourcetype=_json | stats count by status
  index=main | iplocation ip | geostats count by Country
