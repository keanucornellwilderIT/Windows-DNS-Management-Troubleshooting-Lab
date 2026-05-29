# 🌐 DNS Management Lab

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

<img width="974" height="509" alt="image" src="https://github.com/user-attachments/assets/0e2afe57-0fcc-4d35-ac0c-d3bd8f152e3d" />

<img width="750" height="526" alt="image" src="https://github.com/user-attachments/assets/8b52785d-4a9a-476e-98ba-164373919499" />

<img width="975" height="387" alt="image" src="https://github.com/user-attachments/assets/bc0f6d1b-cdeb-438e-9a48-420da3541101" />

<img width="472" height="234" alt="image" src="https://github.com/user-attachments/assets/e8f40eb4-4713-44ae-a039-b92918a0d896" />

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

<img width="752" height="522" alt="image" src="https://github.com/user-attachments/assets/f9c678cc-38e1-406c-9a7d-b860f60ed560" />

<img width="976" height="508" alt="image" src="https://github.com/user-attachments/assets/7b72cf0b-0059-4db3-a747-50b0782e56ab" />

<img width="543" height="224" alt="image" src="https://github.com/user-attachments/assets/c723d966-273b-4c34-814c-9e33a66c845b" />

<img width="478" height="223" alt="image" src="https://github.com/user-attachments/assets/fd7f2ee2-561d-4589-a33f-e93a57b87005" />

<img width="564" height="541" alt="image" src="https://github.com/user-attachments/assets/979fb5f3-276c-45b4-9440-7b83e16faaf4" />

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

<img width="747" height="527" alt="image" src="https://github.com/user-attachments/assets/a063cdb0-71a3-4978-95c1-a1fbfc0e780f" />

<img width="546" height="538" alt="image" src="https://github.com/user-attachments/assets/03c4e27a-2584-4bb2-b13d-5e94ab092e3f" />

<img width="764" height="326" alt="image" src="https://github.com/user-attachments/assets/3a0f026d-b95b-48e7-b78f-fb59d61eb2df" />

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
