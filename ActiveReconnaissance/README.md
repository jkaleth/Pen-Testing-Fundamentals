# PenTesting - Active Reconnaissance

## What is it?

Active reconnaissance in cybersecurity refers to the proactive and direct approach used by threat actors or security professionals to gather information about a target network or system. Unlike passive reconnaissance, which involves collecting publicly available data without directly interacting with the target, active reconnaissance involves actively probing and interacting with the target's infrastructure to gather more detailed information.

Here are some common techniques used in active reconnaissance:

**Port Scanning** This involves scanning the target system's ports to identify which ports are open and what services are running on those ports. It helps attackers or security professionals understand the potential vulnerabilities and services available on the target system.

Tools Used:
- NMAP- 
- **ZENMAP** - graphical interface for NMAP

**Network Scanning:** This technique involves scanning the network to identify active hosts, IP addresses, and their associated services. It helps in creating a map of the network topology, which can be exploited or secured depending on the intent.

Tools Used:
- NMAP- 
- **ZENMAP** - graphical interface for NMAP

**Vulnerability Scanning:** It involves using automated tools to identify potential vulnerabilities in the target system or network. These tools search for known security weaknesses, outdated software, misconfigurations, or other issues that could be exploited.

**Enumeration:** Enumeration involves actively querying the target system for specific information, such as user accounts, network shares, or system configurations. This helps attackers understand the structure and potential entry points of the system.

- **Hosts**
    - windows commands
        - net /?
        - arp -a - all other machines macs that have connected to host your on
        - ipconfig - displaydns
    - Linux
        - finger (usersame, homdir idle time
        - uname -a - OS version
        - env 
- Services
    - nmap scans
- Windows Domains
    - AD
    - Powersell - Get-NetDomain for curent users domain
    - Powersell - Get-NetLoggedOn - all users on computer

- Users 
    - Powersell - Get-NetGroupMember - all users members of the group
- URLS's
    - nmap --script=http-enum <target url>

## Website Reconnaissance
- Crawling websites
    - robots.txt tells crawler which paths canbe crawled and which can be ignored.
    - websiteurl/robots.txt
- Web Scraping/Harvesting
    - Cewl - Kali Linux - crawl a website for password cracking
- Comprehensive Tools
    - Burp Suite 

## Evading Defenses
- Load Balancing Detector - Kali Linux
- Firewall detection - Firewalk in Kali Linux
- WAF - Layer 7 Web Application Firewall

- Web App Brute Force with - [Dirbuster](https://macdownload.informer.com/dirbuster/) 

## Packet Crafting
- hping
- scapy

## Wardriving
- Driving around looking for insecure wifi
- Wigle.net

## Network Analysis
### Wireshark
- Layer 2 (Datalink) (Frame in Wireshark) - Mac Addresses 
- Layer 3 (Network) (Ethernet II in wireshark)- IP Addressese
- Layer 4 Transport (Transmission in Wireshark)
- Layer 5 (Small)
- Layer 6 (Presentation) 
- Layer 7(Application layer) (HTTP Protocal in Wireshark) - see broswer etc.. 

### tcpdump
- like wireshark 

### Vulnerability Scanning

- Web Applications - Nikto- https://www.cirt.net/nikto2/
- Server infrastructures- Nessus

## NMAP

- 

Active reconnaissance is a crucial phase in both offensive and defensive cybersecurity strategies. Ethical hackers or penetration testers might perform active reconnaissance as part of security assessments to identify and remediate vulnerabilities before malicious actors exploit them. However, when performed by malicious actors, active reconnaissance can lead to unauthorized access, data breaches, or system compromises.

## Reference

    










