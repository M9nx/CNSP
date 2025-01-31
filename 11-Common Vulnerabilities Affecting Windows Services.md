


# Top 10 Windows 10 Vulnerabilities


### 10. Windows 10 Mount Manager Vulnerability (CVE-2015-1769, MS15-085)

This [vulnerability](https://www.upguard.com/blog/vulnerability) involves potential [escalation of privilege](https://www.upguard.com/blog/privilege-escalation) by inserting a USB device into the target system. Through this method, an attacker could write a malicious binary to disk and execute the code. [An update](https://docs.microsoft.com/en-us/security-updates/SecurityBulletins/2015/ms15-085) is available from Microsoft to patch this vulnerability.


### 9. Microsoft Edge Vulnerabilities (MS15-091)

The Edge browser's predecessor Internet Explorer was not the highest rated in terms of security, to say the least—and Edge seems to also be getting off to a rough start, security-wise. Various remote-code execution vulnerabilities and security feature bypass exploits can allow attackers to gain control over systems. 

### 8. Microsoft Graphics Component Vulnerabilities (MS15-080)

This grouping of vulnerabilities is related to various font and graphics memory-management flaws that could ultimately result in remote code execution if visiting an entrusted website with embedded fonts. Detailed patching information can be had on the [item's security bulletin](https://support.microsoft.com/en-us/help/3078662/ms15-080-vulnerabilities-in-microsoft-graphics-component-could-allow-r).


### 7. Internet Explorer Vulnerabilities (MS15-079)

Microsoft's famously maligned web browser has a slew of new vulnerabilities with Windows 10, the most serious of them allowing attackers to gain the system rights of the user. 

### 6. Microsoft Windows Journal Vulnerability (MS15-098)

This vulnerability could allow remote code execution to occur if users open a specially-crafted Journal file.


### 5. Re-Direct to SMB Vulnerability (CVE-2015-5143) 

This security flaw impacts all versions of Windows—including Windows 10—and primarily involves a core Windows API library and how Windows connects to SMB. This could result in Windows users being redirected to malicious SMB-based servers and having their encrypted login credentials stolen. The most effective way mitigate this [cyber threat](https://www.upguard.com/blog/cyber-threat) is to block [TCP ports 139 and 445 to disable SMB](https://www.upguard.com/blog/smb-port).



### 4. .NET Framework Escalation of Privilege Vulnerability (MS15-092)

Custom-crafted .NET applications can cause escalation of [privilege exploits](https://www.upguard.com/blog/privilege-escalation) to occur. However, users must be first convinced/tricked into running said applications. 



### 3. Microsoft Font Driver Vulnerability (MS15-078)

Windows Adobe Type Manager improperly handles specially-crafted OpenType fonts, which can result in a remote code execution vulnerability. This may lead to attackers gaining complete control of the system to install programs, view/change/delete data, and create new accounts. Though Microsoft has auto-patched this flaw in the wild, the patch can also be [manually downloaded and installed.](https://support.microsoft.com/en-us/help/3079904/ms15-078-vulnerability-in-microsoft-font-driver-could-allow-remote-cod)




### 2. Windows 10 WiFi Sense Contact Sharing

By default, Windows 10 will share your WiFi credentials to Outlook, Skype, and Facebook contacts—presumably to make WiFi and hot spot sharing easier. This makes it possible for any of these said contacts to hop onto your WiFi network—if in proximity—without authorization. While not necessarily a software vulnerability, this feature can lead to compromises, and should be remediated through the following steps:

- Change the WiFi network name/SSID to include the terms `“_nomap_optout,"` prior to upgrading to Windows 10
- Post-upgrade, change your Windows privacy settings  to disable WiFi Sense sharing.


### 1. Win 32 k Elevation of Privilege Vulnerability (CVE-2015-0057)

This vulnerability involving a flaw in a GUI component of Windows 10—namely the scrollbar element—allows a threat actor to gain complete control of a Windows machine through [privilege escalation](https://www.upguard.com/blog/privilege-escalation). Microsoft has made a [patch available](https://docs.microsoft.com/en-us/security-updates/SecurityBulletins/2015/ms15-010) for fixing this flaw.



## Infographic

![Top 10 Windows 10 Vulnerabilities](https://cdn.prod.website-files.com/5efc3ccdb72aaa7480ec8179/5f050e41fa2f9b7895cf44e6_top10-windows10_VULN.png)



----
