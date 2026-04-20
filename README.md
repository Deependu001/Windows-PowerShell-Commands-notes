# Windows PowerShell Commands notes 
This repository contains my beginner-friendly notes on essential Windows PowerShell commands learned. 

It covers the core commands used for: 

- File navigation and management 
- Viewing and analyzing file contents 
- System information gathering 
- Basic networking and connectivity checks 
- Process and service monitoring 
- User and permission enumeration 
- Searching for sensitive data  

Each command is documented with simple explanations and sample outputs to make learning and revision easier. 

These notes are designed for beginners who are starting their journey in cybersecurity and want a clear understanding of how PowerShell is used in real-world scenarios.

---

# 🛡️ PowerShell Commands  

## 📌 BASIC NAVIGATION & FILE HANDLING

```bash
Get-Location
```
Output:
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
Output:
```bash
Directory: C:\Users\Student\Desktop
Mode   LastWriteTime     Length Name
----   -------------     ------ ----
-a---- 01-04-2026        1200   notes.txt
```

```bash
Get-ChildItem -Force   # Shows hidden files
New-Item file.txt
Copy-Item file.txt copy.txt
Move-Item file.txt Documents\
Remove-Item file.txt
```

━━━━━━━━━━━━━━━━━━━━━━━

## 📌 VIEWING FILE CONTENTS

```bash
Get-Content file.txt
```
Output:
```bash
username: admin
password: 123456
```

```bash
type file.txt
cat file.txt
```

━━━━━━━━━━━━━━━━━━━━━━━

## 📌 SYSTEM INFORMATION

```bash
systeminfo
```
Output:
```bash
OS Name: Microsoft Windows 10
System Type: x64-based PC
```

```bash
hostname
```
Output:
```bash
DESKTOP-AB12CD
```

```bash
whoami
```
Output:
```bash
student-pc\student
```

```bash
Get-ComputerInfo
```

━━━━━━━━━━━━━━━━━━━━━━━

## 📌 NETWORKING BASICS

```bash
ipconfig
```
Output:
```bash
IPv4 Address : 192.168.1.10
```

```bash
ipconfig /all
ping google.com
```
Output:
```bash
Reply from 142.xxx.xxx.xxx: time=20ms
```

```bash
tracert google.com
nslookup google.com
```
Output:
```bash
Name: google.com
Address: 142.xxx.xxx.xxx
```

━━━━━━━━━━━━━━━━━━━━━━━

## 📌 PROCESSES & SERVICES

```bash
Get-Process
```
Output:
```bash
Id   ProcessName
1234 notepad
```

```bash
tasklist
Stop-Process -Name notepad
Get-Service
Start-Service servicename
Stop-Service servicename
```

━━━━━━━━━━━━━━━━━━━━━━━

## 📌 USERS & PERMISSIONS

```bash
net user
```
Output:
```bash
Administrator  Guest  student
```

```bash
net user student
whoami /priv
whoami /groups
```

━━━━━━━━━━━━━━━━━━━━━━━

## 📌 SEARCHING & FILTERING

```bash
Select-String "password" file.txt
```
Output:
```bash
file.txt: password: 123456
```

```bash
Get-ChildItem -Recurse
Get-ChildItem -Recurse | Select-String "password"
```

━━━━━━━━━━━━━━━━━━━━━━━

## 📌 NETWORK CONNECTIONS

```bash
netstat -ano
```
Output:
```bash
TCP 0.0.0.0:80 LISTENING 1234
```

━━━━━━━━━━━━━━━━━━━━━━━

## 📌 DOWNLOADING FILES

```bash
Invoke-WebRequest -Uri "http://example.com/file.txt" -OutFile "file.txt"
```

━━━━━━━━━━━━━━━━━━━━━━━

## 📌 COMMAND HISTORY

```bash
Get-History
```
Output:
```bash
1 ipconfig
2 Get-Process
```

```bash
Clear-History
```

━━━━━━━━━━━━━━━━━━━━━━━

## 📌 BASIC UTILITIES

```bash
cls
clear
exit
```

━━━━━━━━━━━━━━━━━━━━━━━

## 📌 NOTES

- These commands are part of TryHackMe Cyber Security 101  
- Focus is on basic navigation, enumeration, and networking  
- Useful for beginners starting with Windows environments  

━━━━━━━━━━━━━━━━━━━━━━━

I’ll keep documenting more as I continue my cybersecurity journey 🚀