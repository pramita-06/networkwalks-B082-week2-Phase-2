# networkwalks-B082-week2-Phase-2
Network scanning and topology analysis using Zenmap and nmap
🔐 Network Scanning with Zenmap
📌 Project Overview
Network Scanning with Zenmap is a cybersecurity project focused on discovering live hosts within a local network and visualizing the network topology.
Zenmap is the official graphical user interface (GUI) for Nmap. It makes Nmap easier for beginners to use while also providing advanced scanning capabilities for experienced users. Zenmap can be used to save frequently used scans as profiles and run them repeatedly.

In this project, a Ping Scan was performed on an authorized local/virtual network to identify active hosts.

🎯 Project Objectives

The main objectives of this project are:

1. Install and configure Zenmap on Windows.
2. Find the local IP address of the computer.
3. Identify the LAN subnet.
4. Discover live hosts within the subnet.
5. Determine the number of live hosts.
6. Identify the IP addresses of live hosts.
7. Identify the MAC address of the live host.
8. Generate and save a network topology in PDF format.

🛠️ Tools and Technologies

Tool           | Purpose
Zenmap         | Graphical interface for Nmap
Nmap           | Network discovery and scanning
Windows CMD    | Network configuration and MAC address identification
ipconfig       | Finds IPv4 address, subnet mask and gateway
ipconfig /all  | Provides detailed adapter information including MAC address

🔎 Project Methodology

The project was completed in the following stages:

Zenmap Installation
        ↓
Identify Local IP Address
        ↓
Identify LAN Subnet
        ↓
Perform Ping Scan
        ↓
Identify Live Hosts
        ↓
Identify IP Address
        ↓
Identify MAC Address
        ↓
Generate Network Topology
        ↓
Save Topology as PDF

1️⃣ Zenmap Installation

Zenmap was downloaded from the official Nmap website and installed on a Windows computer.
After installation, Zenmap was opened and used to perform the network scan.

Example:
After launching Zenmap, the interface provides:

- Target
- Command
- Profile
- Nmap Output
- Hosts
- Services
- Topology
- Host Details

For this project, the Ping Scan profile was selected.

2️⃣ Finding the Local IP Address

Windows Command Prompt was used to identify the local network configuration.

The following command was executed:
ipconfig

Example output
Ethernet adapter Ethernet 2:

IPv4 Address    : xxx.xxx.xx.x
Subnet Mask     : xxx.xxx.xxx.x

From the subnet mask:

xxx.xxx.xxx.x

the corresponding CIDR notation is:

/24

Therefore, the LAN subnet used for this project was:

xxx.xxx.xx.x/24

Project Result

Local IP Address: "xxx.xxx.xx.x"

Subnet Mask: " xxx.xxx.xxx.x"

LAN Subnet: xxx.xxx.xx.x/24"

«Note: The example values shown in the assignment may differ from the actual network configuration. The project uses the values obtained from the local system.»

3️⃣ Finding Live Hosts

After identifying the subnet, Zenmap was used to discover active hosts.

Target

xxx.xxx.xx.x/24

Profile

Ping scan

Zenmap generated the following Nmap command:

nmap -sn xxx.xxx.xx.x/24

The "-sn" scan performs host discovery without performing a normal port scan.

Why Ping Scan?

A Ping Scan is useful for determining which IP addresses in the selected network are responding.

Instead of checking only one computer, the entire:

xxx.xxx.xx.x/24

network was scanned.

4️⃣ Number of Live Hosts

The completed Zenmap scan reported:

Nmap done: 256 IP addresses (1 host up) scanned

Therefore:

Result

Number of live hosts: 1

The scan identified one responding host within the scanned subnet.

5️⃣ IP Address of the Live Host

The Zenmap output displayed:

Nmap scan report for xxx.xxx.xx.x
Host is up.

Therefore, the live host identified during the scan was:

xxx.xxx.xx.x

Result

Live Host IP Address: xxx.xxx.xx.x"

6️⃣ Finding the MAC Address

To identify the MAC address, the following Windows command was used:

ipconfig /all

The relevant network adapter was:

Ethernet adapter Ethernet 2

This adapter contained:

IPv4 Address    : xxx.xxx.xx.x
Physical Address: xx-xx-xx-xx-xx-xx

The Physical Address represents the MAC address of the network adapter.

Result

MAC Address:
xx-xx-xx-xx-xx-xx

7️⃣ Network Topology

Zenmap's Topology feature was used to visualize the discovered network.

The topology displayed:

localhost
    |
    |
xxx.xxx.xx.x

The topology visualization showed the relationship between the local system and the discovered host.

The Legend was also viewed to understand the meaning of the different topology symbols.

💾 Saving the Topology

The topology graphic was saved in PDF format.

File name used

nmap_result.pdf

The generated PDF can be included with the project documentation and final submission.

📊 Final Results

Parameter            | Result
Tool                 |  Zenmap / Nmap
Scan Type            | Ping Scan
Local IPv4 Address   | "xxx.xxx.xx.x"
Subnet Mask          | "xxx.xxx.xxx.x"
LAN Subnet           | "xxx.xxx.xx.x/24"
IP Addresses Scanned | xxx
Live Hosts           | 1
Live Host IP         | "xxx.xxx.xx.x"
MAC Address          | "xx-xx-xx-xx-xx-xx"
Topology             | Saved as PDF

🖥️ Example of the Nmap Scan

The command used by Zenmap was:

nmap -sn xxx.xxx.xx.x/24

Example result

Starting Nmap 7.991

Nmap scan report for xxx.xxx.xx.x
Host is up.

Nmap done: 256 IP addresses (1 host up) scanned

This result demonstrates that the subnet was successfully scanned and one host responded.

📁 Project Structure

The GitHub repository can be organized as follows:

Network-Scanning-with-Zenmap/
│
├── README.md
│
├─ Zenmap/
|   |--ipconfig.png
|   |--zenmap_scanning.png
│   
└── Report.pdf

📸 Evidence and Screenshots

The project documentation should contain screenshots demonstrating:
Screenshot 1 — IP Configuration

Shows the output of:

ipconfig

and identifies the IPv4 address and subnet mask.

Screenshot 2 — Zenmap Ping Scan

Shows:

Target: xxx.xxx.xx.x/24
Profile: Ping scan

and the completed Nmap output.

🔐 Ethical Considerations

Network scanning should only be performed on networks, systems, and devices that you own or have explicit authorization to assess.

Unauthorized scanning of external networks can violate organizational policies, terms of service, or applicable laws.

This project was performed for educational purposes on an authorized local/virtual network.

📚 Learning Outcomes

Through this project, the following cybersecurity concepts were practiced:

- Understanding local IP addressing
- Understanding subnet notation
- Using CIDR notation
- Network host discovery
- Using Nmap through Zenmap
- Performing Ping Scans
- Identifying active hosts
- Identifying MAC addresses
- Understanding network topology
- Documenting cybersecurity activities
- Saving and presenting scan results

📌 Conclusion

This project demonstrated how Zenmap can be used to perform basic network discovery and visualize network topology.

The local network:

xxx.xxx.xx.x/24
was scanned using a Ping Scan. The scan examined 256 IP addresses and identified one live host, "xxx.xxx.xx.x".

The corresponding MAC address was identified using Windows "ipconfig /all", and the discovered network relationship was visualized using Zenmap's Topology feature.

The topology was then saved in PDF format for project documentation.

🔗 Reference

Networkwalks — Network Scanning with Zenmap

Nmap / Zenmap Official Website

This project follows the procedure and tasks provided in the Week 2 Project Module 5 assignment.


👩‍💻 Project Type

Cybersecurity | Network Scanning | Network Discovery | Nmap | Zenmap

Purpose: Educational cybersecurity and network analysis

👩‍💻 Author
Pramita Shetty

Cybersecurity | Network Security | Ethical Hacking


