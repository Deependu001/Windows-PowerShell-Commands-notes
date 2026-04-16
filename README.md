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


# 🛡️ PowerShell Commands 


📌 BASIC NAVIGATION & FILE HANDLING

Get-Location  
Output:  
Path  
----  
C:\Users\Student  

Set-Location Desktop  

Get-ChildItem  
Output:  
Directory: C:\Users\Student\Desktop  
Mode   LastWriteTime     Length Name  
----   -------------     ------ ----  
-a---- 01-04-2026        1200   notes.txt  

Get-ChildItem -Force  (Shows hidden files)

New-Item file.txt  
Copy-Item file.txt copy.txt  
Move-Item file.txt Documents\  
Remove-Item file.txt  

━━━━━━━━━━━━━━━━━━━━━━━

📌 VIEWING FILE CONTENTS

Get-Content file.txt  
Output:  
username: admin  
password: 123456  

type file.txt  
cat file.txt  

━━━━━━━━━━━━━━━━━━━━━━━

📌 SYSTEM INFORMATION

systeminfo  
Output (short):  
OS Name: Microsoft Windows 10  
System Type: x64-based PC  

hostname  
Output:  
DESKTOP-AB12CD  

whoami  
Output:  
student-pc\student  

Get-ComputerInfo  

━━━━━━━━━━━━━━━━━━━━━━━

📌 NETWORKING BASICS

ipconfig  
Output:  
IPv4 Address : 192.168.1.10  

ipconfig /all  

ping google.com  
Output:  
Reply from 142.xxx.xxx.xxx: time=20ms  

tracert google.com  

nslookup google.com  
Output:  
Name: google.com  
Address: 142.xxx.xxx.xxx  

━━━━━━━━━━━━━━━━━━━━━━━

📌 PROCESSES & SERVICES

Get-Process  
Output:  
Id   ProcessName  
1234 notepad  

tasklist  

Stop-Process -Name notepad  

Get-Service  

Start-Service servicename  
Stop-Service servicename  

━━━━━━━━━━━━━━━━━━━━━━━

📌 USERS & PERMISSIONS

net user  
Output:  
Administrator  Guest  student  

net user student  

whoami /priv  
whoami /groups  

━━━━━━━━━━━━━━━━━━━━━━━

📌 SEARCHING & FILTERING

Select-String "password" file.txt  
Output:  
file.txt: password: 123456  

Get-ChildItem -Recurse  

Get-ChildItem -Recurse | Select-String "password"  

━━━━━━━━━━━━━━━━━━━━━━━

📌 NETWORK CONNECTIONS

netstat -ano  
Output:  
TCP 0.0.0.0:80 LISTENING 1234  

━━━━━━━━━━━━━━━━━━━━━━━

📌 DOWNLOADING FILES

Invoke-WebRequest -Uri "http://example.com/file.txt" -OutFile "file.txt"  

━━━━━━━━━━━━━━━━━━━━━━━

📌 COMMAND HISTORY

Get-History  
Output:  
1 ipconfig  
2 Get-Process  

Clear-History  

━━━━━━━━━━━━━━━━━━━━━━━

📌 BASIC UTILITIES

cls / clear  (Clear terminal)  
exit         (Close PowerShell)  

━━━━━━━━━━━━━━━━━━━━━━━

📌 NOTES

- These commands are part of TryHackMe Cyber Security 101  
- Focus is on basic navigation, enumeration, and networking  
- Useful for beginners starting with Windows environments  

━━━━━━━━━━━━━━━━━━━━━━━

I’ll keep documenting more as I continue my cybersecurity journey 🚀