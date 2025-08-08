# OSINT-Project
To experience OSINT and basic penetration process, including target basic information gathering, sub-domain enumeration, identifying open services and ports, web application vulnerability scanning, risk assessment, and recommendations.

*Target*: xxxcat.com

*Scope*: All sub-domain under xxxcat.com without their supplier assets.

*Highlight*: Total 8 hosts(sub-domain) under xxxcat.com are active at 26/May/2025 14:00. A total <u>53</u> vulnerabilities found include Info in terms of Nessus (ver: 10.8.4), **1 high risk**(CVSS 7.5); **4 medium**(CVSS 6.5/5.3) and **1 low** vulnerabilities, identified over 8 host,  nil known exploited vulnerabilities.



**Methodology**

- Recon Approach: Passive and Active
- Tools Used: subfinder, httpx, nmap, nessus, projectdiscovery, rocketreach.co, leakpeek.com

**OSINT Finding**

**Infrastructure &amp; Technical Footprint**

- Domains: 42 assets
- Host: 24
- IP: 32 Ips
- Open Ports: 80/443/8080/8443/3000
- Status code: 403(18 assets)/200(11 assets)/301(4 assets)/302(4 assets)/404(4 assets)/530(1 assets)
- WAF: Cloudflare
- OS: CentOS Linux 7 Linux Kernel 3.10 / Microsoft Windows Server 2012 R2
- HTTP Encryption: TLS 1.2
- Web Application: nginx(1.18.0), fwebserver/ Microsoft-IIS(10.0)/PRTG

**Summary of Key Findings**

**Description**: SSL Medium Strength Cipher Suites Supported (CVSS 7.5) - The remote host supports the use of SSL ciphers that offer medium strength encryption. Nessus regards medium strength as any encryption that uses key lengths at least 64 bits and less than 112 bits, or else that uses the 3DES encryption suite.

**Solution:**  Reconfigure the affected application, if possible, to avoid the use of medium-strength ciphers.

**Recommended Actions:**

- To fix 1 high vulnerability (SSL Medium Strength Cipher Suites Supported (SWEET32) within 7 days
- Work with the digital certificate provider and IT team to upgrade SSL signature in 1 month
- Mitigate the risk of info disclosure from web application, service itself within 3 months

**Next Steps:**

- Rescan all domains after 3 months to review the performance
- Update related procedure and policy to comply with relevant ISO 270001 Technological Controls
- Deliver security awareness training to internal staff and 3rd party vendors

