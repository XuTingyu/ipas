# 資訊安全技術概論
```
1.網路與通訊安全
2.作業系統與應用程式安全

3.資安維運技術

4.新興科技安全:雲端+行動+IOT
```
### 注意事項:

請務必時時看看[分類題庫](https://github.com/MyDearGreatTeacher/IPAS/blob/master/%E8%B3%87%E8%A8%8A%E5%AE%89%E5%85%A8%E6%8A%80%E8%A1%93/%E5%88%86%E9%A1%9E%E9%A1%8C%E5%BA%AB.md)

# 1.網路與通訊安全
```

  1.1.網路安全Network Security
    1.1.1.網路概論
    1.1.2.網路協定
    1.1.3.網路封包分析---使用wireshark
    1.1.4.網路攻擊手法分析
    1.1.5.網路防御實戰(1)---防火牆技術(Firewall)
    1.1.6.網路防御實戰(2)---入侵偵測系統實戰(intrusion detection system|snort)
  1.2.通訊安全Communications Security (COMSEC)
    1.2.1 無線網路
    1.2.2.無線網路攻擊手法分析
```
```
網路基本知識:
IP addressing: Classful vs classlessful
classful的定義: A B C D E
網路遮罩(subnet mask)有何用處?
子網路切割:

192.168.0.0/24網段切割成4個子4網段? Howto  原理
```
# 2.作業系統與應用程式安全
```  
  2.1.作業系統安全:windows作業系統| Linux作業系統 
     2.1.1.windows作業系統|Windows指令|Sysinternals|Powershell技術
     2.1.2.windows作業系統安全--Windows XP滲透測試
     2.1.3.Linux作業系統與The Linux Command Line
     2.1.4.Linux作業系統安全--Metasploitable 2滲透測試
     
  2.2.作業系統與應用程式 (含資料庫與網頁)攻擊手法
    2.2.1.作業系統攻擊手法分析:rootkits vs anti-rootkits
       https://recover.pixnet.net/blog/post/4535973-anti-rootkits-%E5%B7%A5%E5%85%B7%E6%95%B4%E8%A3%A1%E5%8C%85
    2.2.2.網站安全--
        網頁攻擊手法分析:OWASP TOP 10====網站十大類型漏洞
        SQL injection攻擊手法分析 
        XSS 攻擊手法分析
    2.2.3.程式與開發安全
        a.程式漏洞分析: Buffer overflow
          常見的程式漏洞(不含網站類型漏洞): 大部分指c/c++程式
          (1)Buffer overflow
          (2)format string vuln.
          (3)integer overflow
          (4)heap overflow
        b.SDLC vs SSDLC
```
### Rootkits
```
Rootkits: Subverting the Windows Kernel

Rootkit 的定義：
A rootkit is a tool that is designed to hide itself and other processes、 data and/or activity on a system。
引用於此： The definition of a rootkit

維基百科上的解釋：
A rootkit is a set of software tools intended to conceal running processes， files or system data from the operating system。
Rootkits have their origin in benign applications， 
but in recent years have been used increasingly by malware 
to help intruders maintain access to systems while avoiding detection。
```
### Anti-Rootkits 工具
```
針對 Linux 環境：
Rootkit Hunter
chkrootkit

tkmru/awesome-linux-rootkits
https://github.com/tkmru/awesome-linux-rootkits

通過chkrootkit學習如何在linux下檢測RootKit
chkrootkit | grep INFECTED
https://www.itread01.com/content/1545168977.html

針對 Windows 環境：
偵測用免費工具：
Windows Sysinternals RootkitRevealer
System Virginity Verifier (SVV)
Rootkit Unhooker
ThreatFire
GMER

防毒軟體廠商的免費工具：
TrendMicro Rootkit Buster
McAfee Rootkit Detective
Sophos Anti-Rootkit
Panda Anti-Rootkit
F-Secure BlackLight

中國大陸的免費工具：
冰刃 IceSword
DarkSpy Anti-Rootkit

其他族繁不及備載的工具：
Rootkit Detection & Removal Software
```
### 程式安全實戰: Protostar
```
https://exploit-exercises.lains.space/protostar/
解答: https://github.com/z3tta/Exploit-Exercises-Protostar
```
```
https://exploit-exercises.lains.space/nebula/level00/

Nebula Shell Exploits (Solutions 00-09)
Shell-based exploit exercises

```
### 系統安全實戰
```
1.如何確認遠端電腦存在(LIVE)
2.如何確認遠端電腦的作業系統及版本
3.如何找出該系統的漏洞
4.如何確認該系統的漏洞
5.如何進行安全(攻擊)測試
6.如何控制遠端電腦
```
```
1.	如何確認遠端電腦存在(LIVE)
掃整個網段的IP
Ipscan superscan 
Nmap 
netdiscover
單一 IP: ping

CLT 1: Local Network Scanning with netdiscover | Kali Linux [ Command Line Tips ]
https://www.youtube.com/watch?v=6D400-nphqw

WINDOWS
ipconfig /?
ipconfig /all
2.	如何確認遠端電腦的作業系統及版本
nmap -O  <<IP>>

Starting Nmap 7.70 ( https://nmap.org ) at 2020-04-13 08:16 EDT
Nmap scan report for 10.0.2.4
Host is up (0.00030s latency).
Not shown: 997 closed ports
PORT    STATE SERVICE
135/tcp open  msrpc
139/tcp open  netbios-ssn
445/tcp open  microsoft-ds
MAC Address: 08:00:27:56:6E:8B (Oracle VirtualBox virtual NIC)
Device type: general purpose
Running: Microsoft Windows XP|2003
OS CPE: cpe:/o:microsoft:windows_xp cpe:/o:microsoft:windows_server_2003
OS details: Microsoft Windows XP SP2 or SP3, or Windows Server 2003
Network Distance: 1 hop

OS detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 2.59 seconds

3.	如何找出該系統的漏洞
CVE
MS
XP ===  ms-08-067
WINDOWS 10 == ms17-010
Smb v3
SMBv3 Vulnerability
CVE-2020-0796: Microsoft SMBv3 Remote Code Execution Vulnerability Analysis
https://blog.rapid7.com/2020/03/12/cve-2020-0796-microsoft-smbv3-remote-code-execution-vulnerability-analysis/

4.	如何確認該系統的漏洞
XP == ms-08-067 ? ms17-010? CVE-2020-0796
Nmap nse 
nmap --script smb-vuln-ms08-067.nse -p445   <<IP>>
nmap -p445 --script smb-vuln-ms17-010  <<IP>>
locate *.nse
ls /usr/share/nmap/scripts/ | grep smb

smb2-capabilities.nse
smb2-security-mode.nse
smb2-time.nse
smb2-vuln-uptime.nse
smb-brute.nse
smb-double-pulsar-backdoor.nse
smb-enum-domains.nse
smb-enum-groups.nse
smb-enum-processes.nse
smb-enum-services.nse
smb-enum-sessions.nse
smb-enum-shares.nse
smb-enum-users.nse
smb-flood.nse
smb-ls.nse
smb-mbenum.nse
smb-os-discovery.nse
smb-print-text.nse
smb-protocols.nse
smb-psexec.nse
smb-security-mode.nse
smb-server-stats.nse
smb-system-info.nse
smb-vuln-conficker.nse
smb-vuln-cve2009-3103.nse
smb-vuln-cve-2017-7494.nse
smb-vuln-ms06-025.nse
smb-vuln-ms07-029.nse
smb-vuln-ms08-067.nse
smb-vuln-ms10-054.nse
smb-vuln-ms10-061.nse
smb-vuln-ms17-010.nse
smb-vuln-regsvc-dos.nse

pr4jwal/CVE-2020-0796
wget https://raw.githubusercontent.com/pr4jwal/CVE-2020-0796/master/cve-2020-0796.nse
5.      如何進行安全(攻擊)測試
6.      如何控制遠端電腦

```
# 3.資安維運技術
```        
  3.1.惡意程式防護與弱點管理(vulnerability management)
    3.1.1.惡意程式malware
    3.1.2.惡意程式分析
    3.1.3.惡意程式防護
         防毒軟體
         防駭軟體
         防火牆
         
    3.1.4.系統弱點及其管理
       如何偵測系統弱點---漏洞掃描
    3.1.5.網站弱點及其管理
       如何偵測網站弱點---漏洞掃描
 ```
 ```
  3.2.資料安全(data Security)及備份管理(backup)
     https://en.wikipedia.org/wiki/Data_security
    3.2.1.資料安全(data Security)
    3.2.2.資料安全(data Security)技術:
          Disk encryption(硬碟加密)
          Software versus hardware-based mechanisms for protecting data
          Data masking(資料)
    3.2.3.資料安全(data Security)標準:
          ISO/IEC 27001:2013 and ISO/IEC 27002:2013
          General Data Protection Regulation (GDPR) 
          
    3.2.4.備份管理(backup)基本觀念    https://en.wikipedia.org/wiki/Backup
    3.2.5.備份方法|種類(Backup methods):
            Full Backup |Incremental Backup|Differential backup|選擇式備份
            冷備份|熱備份
     3.2.6.備份儲存(Storage media): RAID  SAN NAS
            RAID 0+1 vs RAID 1+0   RAID 5+0
           https://zh.wikipedia.org/wiki/RAID#RAID_10/01 
     3.2.7.備份管理(backup)類型:Online | Near-line | Off-line | Off-site data protection | Backup site
 ```
 ```
  3.3.日誌管理
    3.3.1.日誌log|日誌管理|日誌分析
    3.3.2.windows作業系統日誌及其管理
    3.3.3.Linux作業系統日誌及其管理
    3.3.4.Apache網站伺服器日誌及其管理
    
OWASP Top 10 Proactive Controls 2018   
The OWASP Top Ten Proactive Controls describes the most important control and control categories 
that every architect and developer should absolutely, 100% include in every project
https://owasp.org/www-project-proactive-controls/

C1: Define Security Requirements
C2: Leverage Security Frameworks and Libraries
C3: Secure Database Access
C4: Encode and Escape Data
C5: Validate All Inputs
C6: Implement Digital Identity
C7: Enforce Access Controls
C8: Protect Data Everywhere
C9: Implement Security Logging and Monitoring
C10: Handle All Errors and Exceptions
    
```
# 4.新興科技安全
```
  4.1.雲端安全概論cloud security
    4.1.1.雲端運算cloud computing:Iaas Paas Saas  
    4.1.2.雲端運算實戰>>>visualizationv虛擬化技術 vs docker(雲端容器技術container)
          '兩種虛擬化技術:Type 1 vs Type 2
    4.1.3.雲端系統漏洞分析
       OWASP Cloud-Native Application Security Top 10
       OWASP Top 10 Cloud Security Risk
       https://www.owasp.org/images/3/3f/OWASP_Cloud_Top_10.pdf
       The Serverless Security Top 10 Most Common Weaknesses Guide(2018)
       OWASP Cloud Testing Guide [https://www.owasp.org/images/a/aa/OWASPCloudTestingMar19.pdf]
  ```
  ```
  4.2.行動裝置安全概論Mobile security
    4.2.1.行動裝置安全
    4.2.2.Mobile 攻擊手法分析:OWASP Mobile Top 10(2016)
      https://www.gss.com.tw/images/stories/epaper_GSS_security/pdf/epaper_gss_security_0132.pdf
    4.2.3.OWASP Mobile Security Project
          Mobile Security Testing Guide
          Mobile Application Security Verification Standard
          Mobile Security Checklist
 ```
 ```
  4.3.物聯網安全概論IOT security
   4.3.1.物聯網 IOT(Internet of Thing)==>Internet of Threat
   4.3.2.物聯網攻擊手法分析:OWASP IOT TOP 10(2018)
```
