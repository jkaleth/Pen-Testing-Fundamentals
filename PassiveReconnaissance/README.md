# Passive Reconnaissance

## What is it?

 Passive reconnaissance in the context of penetration testing (pentesting) refers to the process of gathering information about a target system or network without directly interacting with it or causing any noticeable actions or effects. It involves collecting data through publicly available sources, open-source intelligence, and passive observations without actively engaging the target's systems.

## Information Gathering

- Record Keeping- it's important to keep records of findings during your pen testing

     - Using Excel is a good method since data can be stored in rows and columns
    
        - Finding Method- Ex: Linkedin Resume 
        - Type of operatin systems running
        - Security tools being used by team
        - Is anything being run in the cloud? 
        - What tool we can use to pentest to go into teh enumeration phase. Ex: use an NMAP scan to scan the public IP space of the organization


- **Publicly available data:** This involves collecting information from sources such as websites, social media profiles, public databases, search engines, and other openly accessible resources. We're looking for:

    - Phone numbers
    - Email addresses
    - Contact names
    - Organizational charts
    - Types of operating systems used
    - Types of web servers

    **Where do we look?**
    - Linkedin is a great place to get information on types of systems beings used. 
    - Dupmester diving
    - Google searches
    - Fastpeoplesearch.com
    - Job posting by organizations.

- **Network traffic analysis:** Analyzing network traffic to gain insights into the types of systems, devices, IP addresses, and potential vulnerabilities without directly interacting with them. This can include monitoring public communications, DNS queries, or metadata analysis.

- **Social engineering and OSINT (Open Source Intelligence):** Leveraging information available from social media, forums, job postings, company websites, etc., to gather details about employees, organizational structure, technologies in use, and potential weak points.

## Types of Roles 

- **Pentester- Information Gathering** - Passive Reconnaissnce
- **Pentester- Vulnerability Scanning** - Take info from passive team to run scans to find vulnerabilities

## Summary
Passive reconnaissance is a critical initial phase in pentesting as it helps gather a comprehensive understanding of the target environment without alerting the target organization's security measures. It aids in identifying potential entry points, vulnerabilities, and information that can be leveraged for further analysis and planning in the subsequent active phases of the penetration test.
