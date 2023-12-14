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

## OSINT Tools

### Censys
Censys is a widely used internet scanning platform that helps in discovering devices, networks, and services operating on the internet. It performs regular scans of the entire IPv4 address space, collecting data on hosts and websites. Censys gathers information such as open ports, SSL certificates, domain names, and protocols used by devices connected to the internet.

The platform offers a search engine that enables users to query this collected data to gain insights into devices, services, and security vulnerabilities present on the internet. Security professionals, researchers, and organizations use Censys for various purposes, including network monitoring, threat detection, and cybersecurity research.

Censys can be a valuable tool for understanding the internet's structure, identifying potential security risks, and improving overall network security by discovering and addressing vulnerabilities in systems and services.

Censys offers its services through its official website, where users can access the platform and its features. You can visit the Censys website at [Censys ](https://censys.io/) to sign up for an account or explore the available tools and services they provide.

### Recon-ng - Kali Linux 
Recon-ng is an open-source reconnaissance framework written in Python. It is specifically designed for information gathering, reconnaissance, and open-source intelligence gathering (OSINT). Recon-ng simplifies the process of gathering information about individuals, companies, or systems by providing a modular and extensible framework.

#### Reference
[Recon-ng Tutorial ](https://hackertarget.com/recon-ng-tutorial/)

#### Commands

Make sure to update first-  on Kali cli:

```
$ apt-get update && apt-get install recon-ng
```
Launch Recon-ng

```
$ recon-ng
```
Create New Workspace for the Current Project
```
[recon-ng][default] > workspaces create workspacename
```
Get Help
```
[recon-ng][workspacename] > help
```
### Shodan
Shodan is a search engine specifically designed to locate devices and systems connected to the internet. Unlike traditional search engines that crawl and index web pages, Shodan scans the internet for devices such as servers, routers, webcams, computers, IoT (Internet of Things) devices, and more. It collects information about these devices, including their operating systems, services, open ports, and sometimes even specific vulnerabilities.

Shodan allows users to search for devices based on various criteria like geographical location, device type, open ports, services running on those ports, and more. It's often used by security professionals, researchers, and hackers to discover internet-exposed devices and identify potential security weaknesses. However, it's crucial to note that while Shodan can be a valuable tool for security purposes, using it for unauthorized access or exploitation of vulnerabilities is illegal and unethical.

#### Link
[Shodan Site ](https://shodan.io)

### Metagoofil
Metagoofil is a Linux tool used for information gathering and metadata extraction from public documents. It's specifically designed to extract metadata (such as author names, email addresses, software versions, etc.) from various types of files like Word documents, PDFs, spreadsheets, and presentations that are available on the internet.

The tool works by using search engines like Google to find and download files based on specified parameters (file types, domains, etc.), and then it extracts metadata from those downloaded files. This information can sometimes reveal sensitive details or provide insight into the document's history or origin, which could be valuable for security auditing or intelligence gathering purposes.

However, it's important to note that using Metagoofil or any similar tool for extracting metadata should be done ethically and legally, respecting privacy and copyright laws and only for authorized and legitimate purposes. Unauthorized or unethical use of such tools could lead to legal consequences.

Metagoofil is a Python-based open-source tool, and it can be accessed and used through the command line interface. Here are the steps to access and use Metagoofil:

1. **Installation**:
   - Ensure you have Python installed on your system. Metagoofil requires Python to run.
   - Download Metagoofil from its official GitHub repository or source distribution.
   - Install any dependencies that Metagoofil requires. Typically, these dependencies include libraries for parsing document formats.

2. **Run Metagoofil**:
   - Open a terminal or command prompt.
   - Navigate to the directory where Metagoofil is installed.
   - Use the command-line interface to execute Metagoofil by specifying the desired options and parameters.

3. **Command Syntax**:
   - To use Metagoofil, you'll typically use a command structure like this:
     ```
     python metagoofil.py -d <domain> -t <filetype> -o <output_directory> -l <number_of_results>
     ```
     - `-d` specifies the target domain.
     - `-t` is used to specify the file type (e.g., pdf, doc, xls, ppt, etc.).
     - `-o` indicates the directory where Metagoofil will save the downloaded files and extracted metadata.
     - `-l` is used to set the number of results to retrieve from the search engine.

4. **Example**:
   - An example command might look like this:
     ```
     python metagoofil.py -d example.com -t pdf,doc,docx -o output_directory -l 50
     ```
     - This command will search for PDFs and Word documents from the domain "example.com", download them to the "output_directory", and extract metadata from the top 50 search results.

Please note that the specific command-line options and syntax might vary based on the version of Metagoofil you're using. Always refer to the tool's documentation or help section for accurate and updated information on how to use it effectively.

Remember, it's crucial to use tools like Metagoofil ethically and legally, respecting privacy and legal boundaries. Unauthorized or unethical use of such tools may lead to legal repercussions.

### Foca
Similar to Metagoofil but needs to be run on Windows

### The Harvester
The harvester in Kali Linux refers to a tool designed for gathering and enumerating information about email addresses, subdomains, hosts, employee names, open ports, and banners from different public sources like search engines, PGP key servers, and SHODAN computer database.

One of the most popular tools for harvesting information is "theHarvester," which is pre-installed in Kali Linux. It's a command-line tool used for gathering information like email addresses, subdomains, hosts, employee names, open ports, and banners from public sources using different search engines like Google, Bing, PGP key servers, and more.

It's often used in penetration testing and reconnaissance phases to collect information about a target as a part of ethical hacking or security testing.

To use theHarvester in Kali Linux, you can open a terminal and type:

```bash
theharvester -d domain.com -l 100 -b all
```

Replace `domain.com` with the domain you want to search for. `-l 100` indicates you want to limit the results to 100, and `-b all` specifies to use all available data sources.

Remember, when using tools like theHarvester or conducting any security testing, ensure that you have proper authorization and legal permission to perform these actions against the target domain or network. Unauthorized use could be illegal and against ethical standards.

### Maltego
Maltego is a widely used and powerful data visualization and link analysis tool used in the field of cybersecurity, threat intelligence, and digital forensics. It provides a platform for visualizing and correlating complex information gathered from various sources on the internet.

The tool allows users to gather information from diverse resources such as public databases, search engines, social media platforms, and other open-source intelligence repositories. It then analyzes this data to create graphical representations, commonly referred to as graphs, that display the relationships and connections between different entities like people, organizations, websites, IP addresses, domains, and more.

ou can obtain Maltego from its official website. Maltego offers both a commercial version and a community edition:

    Maltego Commercial Edition: This version comes with more advanced features and capabilities. You can purchase licenses for the commercial version directly from the Maltego website. The commercial version offers more functionalities and access to a broader range of data sources.

    Maltego Community Edition: The Community Edition is available for free and provides limited access to certain functionalities and data sources. It's a good starting point for individuals who want to explore and get familiar with the tool. You can download the Community Edition from the Maltego website after creating an account.

Visit the official Maltego website at [Maltego ](https://www.maltego.com), navigate to the "Products" section, and select the version (Commercial or Community) that suits your requirements. Follow the instructions provided to download and install Maltego on your system.

### DNS Information
- **A Record** - Links a hostname to an IPv4 address
- **AAAA Record** - Links a hostname to an IPv6 address
- **CNAME** - Canonical Name Record- Points a domain to another domain
- **MX Record** - Directs emails to a mail server
- **SOA** Start of Authority Record- Stores information about a domain name or zone.

### Central Ops
CentralOps.net is a website that provides various online network investigation tools and services. It offers a suite of tools that allow users to gather information about domain names, IP addresses, email addresses, and other related internet data.

Some of the tools available on CentralOps.net include:

    Domain Dossier: Provides information about a domain name, including registration details, DNS records, and network information.
    Traceroute: Shows the path that data packets take from your computer to a specified destination server or IP address.
    Email Dossier: Allows users to investigate an email address, revealing information about the mail server, sender domain, and more.
    IP Dossier: Provides information about an IP address, including geolocation, ASN (Autonomous System Number), and related domains.

These tools can be helpful for network administrators, cybersecurity professionals, website owners, and individuals looking to gather information about online entities or troubleshoot network-related issues.


## Summary
Passive reconnaissance is a critical initial phase in pentesting as it helps gather a comprehensive understanding of the target environment without alerting the target organization's security measures. It aids in identifying potential entry points, vulnerabilities, and information that can be leveraged for further analysis and planning in the subsequent active phases of the penetration test.

## Markdow Code Example

### Tables
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |


## Markdow Code Example

### Tables
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |





