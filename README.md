# 🌐 DNS Management & Troubleshooting Lab

## 📌 Overview
This lab demonstrates DNS management and troubleshooting in a Windows Active Directory environment. The project focuses on creating and modifying DNS records, testing name resolution, analyzing DNS cache behavior, and configuring CNAME records.

The lab simulates real-world troubleshooting tasks commonly performed in IT support, systems administration, and network administration roles.

---

# 🧰 Technologies Used
- Microsoft Azure
- Windows Server
- Windows 10/11
- Active Directory
- DNS
- Command Prompt
- TCP/IP Networking

---

# 🖥️ Lab Environment

| Device | Role |
|---|---|
| `dc-1` | Domain Controller / DNS Server |
| `client-1` | Domain Joined Client |

- Domain: `helpdesklab.local`
- Virtual Network: `hd-vnet`
- Resource Group: `hd-lab`

---

# 🔬 Lab Activities

## A-Record Configuration & Testing

### Objective
Create and test a DNS A-record for hostname resolution.

### Tasks Performed
- Attempted to ping `mainframe` from `client-1`
- Verified DNS resolution failure using `nslookup`
- Created a DNS A-record on `dc-1`
- Configured `mainframe` to point to the domain controller’s private IP address
- Verified successful hostname resolution from `client-1`

### Commands Used
```powershell
ping mainframe
nslookup mainframe
```

### Screenshot
(Add screenshot here)

---

## Local DNS Cache Troubleshooting

### Objective
Analyze and clear the local DNS resolver cache.

### Tasks Performed
- Modified the `mainframe` DNS record to `8.8.8.8`
- Verified cached DNS results from `client-1`
- Displayed the local DNS cache
- Cleared the DNS cache
- Verified updated DNS resolution after cache flush

### Commands Used
```powershell
ipconfig /displaydns
ipconfig /flushdns
ping mainframe
```

### Screenshot
(Add screenshot here)

---

## CNAME Record Configuration

### Objective
Configure and test a DNS CNAME record.

### Tasks Performed
- Created a CNAME record named `search`
- Configured the CNAME record to point to `www.google.com`
- Tested hostname resolution from `client-1`
- Verified CNAME resolution using `nslookup`

### Commands Used
```powershell
ping search
nslookup search
```

### Screenshot
(Add screenshot here)

---

# 🛠️ Troubleshooting Scenarios

## DNS Resolution Troubleshooting
- Diagnosed failed hostname resolution
- Verified DNS record creation and propagation
- Tested DNS functionality from the client machine

---

## DNS Cache Troubleshooting
- Analyzed cached DNS records
- Verified stale DNS entries
- Flushed the local DNS cache to update name resolution

---

## CNAME Resolution Testing
- Configured alias-based hostname resolution
- Verified successful DNS alias functionality
- Tested external hostname mapping through DNS

---

# 💡 Skills Demonstrated
- DNS administration
- A-record configuration
- CNAME configuration
- DNS troubleshooting
- DNS cache management
- Name resolution testing
- Active Directory networking
- Command-line troubleshooting

---

# 👨‍💻 Author
Keanu  
Aspiring Network / Cloud Administrator