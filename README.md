# 🛡️ Windows PowerShell Commands for Cybersecurity

![PowerShell](https://img.shields.io/badge/Shell-PowerShell-blue)
![Level](https://img.shields.io/badge/Level-Beginner-green)
![Focus](https://img.shields.io/badge/Focus-Cybersecurity-red)

---

## 📖 Overview

This repository contains my **beginner-friendly notes on essential Windows PowerShell commands**, focused on **cybersecurity fundamentals**.

It covers real-world commands used for:

- 📂 File navigation and management  
- 📄 Viewing and analyzing file contents  
- 💻 System information gathering  
- 🌐 Networking and connectivity checks  
- ⚙️ Process and service monitoring  
- 👤 User and permission enumeration  
- 🔍 Searching for sensitive data  

Each command includes **clear explanations and practical outputs** to help with learning, revision, and hands-on practice.

---

## 🚀 Why This Matters

PowerShell is widely used in:
- 🔴 Red Teaming (Enumeration & Exploitation)
- 🔵 Blue Teaming (Monitoring & Investigation)
- 🟡 System Administration

Understanding these commands is essential for **real-world cybersecurity scenarios**.

---

# 🧾 Commands & Examples

---

## 📌 BASIC NAVIGATION & FILE HANDLING

```bash
Get-Location
```
```bash
Path
----
C:\Users\Student
```

```bash
Set-Location Desktop
```

```bash
Get-ChildItem
```
```bash
Directory: C:\Users\Student\Desktop
Mode   LastWriteTime     Length Name
----   -------------     ------ ----
-a---- 01-04-2026        1200   notes.txt
```

```bash
Get-ChildItem -Force   # Show hidden files
```

```bash
New-Item file.txt
Copy-Item file.txt copy.txt
Move-Item file.txt Documents\
Remove-Item file.txt
```

---

## 📌 VIEWING FILE CONTENTS

```bash
Get-Content file.txt
```
```bash
username: admin
password: 123456
```

```bash
type file.txt
cat file.txt
```

---

## 📌 SYSTEM INFORMATION

```bash
systeminfo
```
```bash
OS Name: Microsoft Windows 10
System Type: x64-based PC
```

```bash
hostname
```
```bash
DESKTOP-AB12CD
```

```bash
whoami
```
```bash
student-pc\student
```

```bash
Get-ComputerInfo
```

---

## 📌 NETWORKING BASICS

```bash
ipconfig
```
```bash
IPv4 Address : 192.168.1.10
```

```bash
ipconfig /all
```

```bash
ping google.com
```
```bash
Reply from 142.xxx.xxx.xxx: time=20ms
```

```bash
tracert google.com
nslookup google.com
```
```bash
Name: google.com
Address: 142.xxx.xxx.xxx
```

---

## 📌 PROCESSES & SERVICES

```bash
Get-Process
```
```bash
Id   ProcessName
1234 notepad
```

```bash
tasklist
```

```bash
Stop-Process -Name notepad
```

```bash
Get-Service
Start-Service servicename
Stop-Service servicename
```

---

## 📌 USERS & PERMISSIONS

```bash
net user
```
```bash
Administrator  Guest  student
```

```bash
net user student
```

```bash
whoami /priv
whoami /groups
```

---

## 📌 SEARCHING & FILTERING

```bash
Select-String "password" file.txt
```
```bash
file.txt: password: 123456
```

```bash
Get-ChildItem -Recurse
Get-ChildItem -Recurse | Select-String "password"
```

---

## 📌 NETWORK CONNECTIONS

```bash
netstat -ano
```
```bash
TCP 0.0.0.0:80 LISTENING 1234
```

---

## 📌 DOWNLOADING FILES

```bash
Invoke-WebRequest -Uri "http://example.com/file.txt" -OutFile "file.txt"
```

---

## 📌 COMMAND HISTORY

```bash
Get-History
```
```bash
1 ipconfig
2 Get-Process
```

```bash
Clear-History
```

---

## 📌 BASIC UTILITIES

```bash
cls
clear
exit
```

---

## 🎯 Key Takeaways

- PowerShell is powerful for **system enumeration**
- Many commands are useful in **CTFs and real-world labs**
- Helps build a strong **Windows security foundation**

---

## 📌 Future Improvements

- Add advanced PowerShell scripting ⚡  
- Include real-world attack scenarios 🧠  
- Document detection techniques (Blue Team) 🔵  

---

## 👨‍💻 Author

**Deependu Mondal**  
Cybersecurity Learner 🚀  

---

⭐ *I’ll keep updating this repository as I progress in my cybersecurity journey.*