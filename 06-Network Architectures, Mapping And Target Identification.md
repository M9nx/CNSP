



`Nmap 101` 

# What is nmap?


is a robust open source network probe tool. It is used to find hosts, ports, and services on a computer network.
Zenmap is a graphical user interface (GUI) for Nmap that provides a user-friendly interface to visualize and interact with scan results. It offers various views, filtering options, and graphing capabilities, making it easier to analyze and interpret the data collected by Nmap.


# The Working

Users choose a list of targets on a network about which they wish to learn more.
Users can specify the depth of each scan in addition to the range of objects that will be examined. For instance, a quick or restricted scan can reveal which ports are open and which ones the firewall has blocked. Additional information that may be gathered by more thorough scans includes the kind of devices using those ports, the operating systems they are using, and even the services that are now executing on them. Nmap may also unearth more detailed information, such as the version of certain services. This makes it the ideal tool for identifying vulnerabilities and supporting patch management initiatives. Another option is to scan every network port, but it might take a long time and use up a lot of the available bandwidth. Zenmap graphical user interface. It is a great tool for beginners.



# Syntax


`nmap <Scan Type(s)><Options> <target specification>`

**A. Scan Type(s):** You can specify one or more scan types to perform. Some common scan types include:

`**-sT:** TCP connect scan`

`**-sU:** UDP scan`

`**-sS:** SYN scan`

`**-sF:** FIN scan`

`**-sX:** Xmas scan`

`**-sA:** ACK scan`

`**-sP:** Ping scan (host discovery)`

`**-sV:** Version detection`

**B. Options:** Nmap provides numerous options to customize your scan. Here are a few commonly used options:

`**-p <port ranges>:** Specifies the port(s) to scan, e.g., -p 201–500 or -p 80,443`

`**-A:** Enables aggressive scanning options (OS detection, version detection, script scanning, and traceroute)`

`**-O:** Enables operating system detection`

`**-sC:** Executes default NSE scripts for target scanning`

`**-v:** Increases verbosity level`

`**-oN <file>:** Saves results in normal format to a file`

`**-oX <file>:** Saves results in XML format to a file`

`**-iL <file>:** Specifies a file containing target IP addresses/hostnames for bulk scanning`


**C. target specification:** You can specify the target(s) you want to scan using one or more of the following:

`IP addresses: e.g., 192.168.5.1, 10.0.0.0/24`

`Hostnames: e.g., qwerty.com, [www.qwerty.com](http://www.qwerty.com)`

`CIDR notation: e.g., 192.140.0.0/16`

`IP ranges: e.g., 192.168.1.100–200`



# Nmap Scripting Engine (NSE)

NSE (Nmap Scripting Engine), which provides extra functionalities in the Nmap scan process by enabling scripts for additional tasks like brute force, vulnerability discovery, or exploitation, is another significant aspect of nmap.

NSE scripts are located at `/usr/share/nmap/scripts`

**NSE categorization:**

## The first classification

based primarily on the time of operation, includes four script types:

1. Scripts called `prerules`, such as those used to create new targets, are run before to any Nmap scan phase.

2. During the scan process, **host scripts** are executed.

3. **Service scripts,** like host scripts, are run after each batch of hosts is scanned.

4. `Postrule` scripts** are run after the scan and can exploit a vulnerability discovered during the scan.


## The second classification 
is determined by the **goals and safety** of the script. Scripts are arranged in categories based on this standard. The categories include

1. **Broadcast**: These scripts allow to discover hosts by broadcasting the local network.

2. **Authentication**: This category includes scripts that are helpful for handling authentication. You can find scripts that get around authentication procedures in this area, such as http-method-tamper, which allows you to get around password-protected resources by altering HTTP verbs. If there is no array of routes to check, the check will be made against any password-protected resources that are discovered when crawling the webserver.

3. **Default:** This category consists of scripts that adhere to the standards for usefulness, reliability, reliability, intrusiveness, and privacy. This type of script has two requirements: it must finish quickly, and it must provide useful information on the target. The output must be readable and restricted to truthful data. Less suitable for this category are intrusive scripts that could crash the target system or service.

4. **Malware**: Malware scripts are designed to detect the possible malware or backdoors presence on the target.

Example:

`auth-spoof`

Checks for an identd (auth) server which is spoofing its replies.

`smb-double-pulsar-backdoor`

Checks if the target machine is running the Double Pulsar SMB backdoor.

**5. Discovery:** This group of scripts tries to learn more about the target by scouring directories, public sources, SNMP-capable devices, etc.

Example:

`dns-ip6-arpa-scan`

Performs a quick reverse DNS lookup of an IPv6 network using a technique which analyzes DNS server response codes to dramatically reduce the number of queries needed to enumerate large networks.

`http-errors`

This script crawls through the website and returns any error pages.

6. **Brute**: Scripts for brute force attacks are found in this category.

Example:

`ldap-brute`

Attempts to brute-force LDAP authentication. By default it uses the built-in username and password lists. In order to use your own lists use the userdb and passdb script arguments.

`mongodb-brute`

Performs brute force password auditing against the MongoDB database.

**7. DOS:** These scirpts can crash a vulnerable system or service, however they are useful for testing targets for vulnerabilities prior to DOS attacks.

`smb-flood`

Exhausts a remote SMB server’s connection limit  by opening as many connections as we can. Most implementations of SMB have a hard global limit of 11 connections for user accounts and 10 connections for anonymous. Once that limit is reached, further connections are denied. This script exploits that limit by taking up all the connections and holding them.

**8. Fuzzer:** A buffer overflow, DOS (denial of service), cross-site scripting, or SQL injection vulnerability can be found using scripts in the category known as “fuzzer,” which sends out random fields in large quantities.

9. **Exploit:** Scripts in this category are used to exploit vulnerabilities on targets.

Example:

`http-dlink-backdoor`

Detects a firmware backdoor on some D-Link routers by changing the User-Agent to a “secret” value. Using the “secret” User-Agent bypasses authentication and allows admin access to the router.



# Supplemental

It is difficult to determine which scripts are the most popular when there are over 600 of them available. Because of this, the Nmap team created the **‘-sC’** option, which enables you to execute all of the top Nmap scripts at once.

Example:

`nmap -sC sample.com`

A simple script scan using the default set of scripts.

`nmap -sn -sC sample.com`

A script scan without a port scan; only host scripts are eligible to run.

`nmap -Pn -sn -sC sample.com`

A script scan without host discovery or a port scan. All hosts are assumed up and only host scripts are eligible to run.

`nmap — script smb-os-discovery — script-trace sample.com`

Execute a specific script with script tracing.

`nmap — script snmp-sysdescr — script-args creds.snmp=admin sample.com`

Run an individual script that takes a script argument.

`nmap — script mycustomscripts,safe sample.com`

Execute all scripts in the mycustomscripts directory as well as all scripts in the safe category.


-----
----
