# 🔐 Penetration Testing – Footprinting & Network Scanning

## 💻 Week 2 Cybersecurity Internship

This repository contains my **Week 2 practical work** completed as part of the **Cybersecurity Internship Program at Networkwalks**.

The project focuses on two penetration-testing phases:

* 🔎 Footprinting & Reconnaissance
* 🌐 Network Scanning & Network Discovery

## 🎯 Objectives

* 🧠 Understand the purpose of reconnaissance and footprinting.
* 🔍 Collect publicly available information using Kali Linux tools.
* 🌐 Identify web technologies and server information.
* 📡 Perform DNS enumeration.
* 📋 Inspect HTTP response headers.
* 🛡️ Identify Web Application Firewall information.
* 💻 Identify local network configuration.
* 🔎 Discover live hosts on an authorized local network.
* 📊 Document security observations and recommendations.

## 🛠️ Tools Used

### 🐧 Kali Linux

* 👤 WHOIS
* 🔬 WhatWeb
* 🌐 Nslookup
* 📡 cURL
* 🛡️ Wafw00f
* 🔎 DNSRecon

### 🪟 Windows / Network Scanning

* 💻 ipconfig
* 💻 ipconfig /all
* 🗺️ Zenmap (Nmap GUI)

## 🔎 Phase 1 – Footprinting & Reconnaissance

The following tools were used during the reconnaissance activity:

| 🛠️ Tool    | 🎯 Purpose                                      |
| ----------- | ----------------------------------------------- |
| 👤 WHOIS    | Domain registration and name-server information |
| 🔬 WhatWeb  | Web technology fingerprinting                   |
| 🌐 Nslookup | DNS resolution                                  |
| 📡 cURL     | HTTP response-header inspection                 |
| 🛡️ Wafw00f | WAF identification                              |
| 🔎 DNSRecon | DNS record enumeration                          |

### 💻 Commands Used

```bash
whois networkwalks.com
whatweb networkwalks.com
nslookup networkwalks.com
curl -I https://networkwalks.com
wafw00f networkwalks.com
dnsrecon -d networkwalks.com
```

## 🌐 Phase 2 – Network Scanning

Windows networking commands were used to identify the local network configuration.

```cmd
ipconfig
ipconfig /all
```

🗺️ **Zenmap** was then used to perform a **Ping Scan** against the authorized local LAN subnet.

The scan was used to:

* 🟢 Identify live hosts
* 📍 Record IP addresses
* 🔐 Record MAC addresses
* 🗺️ Visualize the network topology

## 📌 Key Findings

The reconnaissance activity demonstrated that publicly available information can reveal:

* 🌐 Domain registration information
* 🔬 Web technologies
* 🖥️ Server and HTTP information
* 📡 DNS infrastructure
* 🛡️ WAF information

The network scanning activity demonstrated how active devices can be identified within an authorized local network.

## ⚠️ Risk Observations

The assessment included observations related to:

* 🔎 Exposed web technology information
* 🌐 Identifiable server IP information
* 📋 HTTP technical information
* 🛡️ Identifiable WAF technology
* 📡 Exposed DNS infrastructure information
* 💻 Multiple live hosts on the local network

> ⚠️ These observations do not by themselves confirm vulnerabilities. Further authorized security testing would be required for validation.

## 💡 Recommendations

* 🔒 Minimize unnecessary disclosure of web-stack information.
* 🔄 Keep CMS platforms and plugins updated.
* 📋 Review HTTP response headers and reduce unnecessary technical information where appropriate.
* 📡 Regularly review DNS records.
* 🛡️ Keep the WAF enabled, properly configured and monitored.
* 🔎 Perform regular internal network discovery.
* ⚠️ Investigate unknown devices found during network scans.
* 🗺️ Maintain updated network topology documentation.
* ✅ Perform reconnaissance and scanning only within an authorized scope.

## ⚖️ Disclaimer

All activities in this repository were performed for **authorized educational and cybersecurity training purposes**.

Reconnaissance and scanning should only be performed against systems and networks where appropriate authorization has been obtained.

## 👨‍💻 Author

**Pramita Shetty**

🎓 Cybersecurity Intern – B082
🏢 Networkwalks Cybersecurity Internship

