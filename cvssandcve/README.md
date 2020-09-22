## All about CVSS and CVE
---

## [+] CVSS

CVSS stands for Common Vulnerability Scoring System which is maintained by FIRST(Forums of Incident Response and Security Team).

### History
The CVSS came into the play when it became diffcult to rate the severity of any vulnerabililty as most the cases vulnerabilities are subjective which creates
different severity level of same vulnerability in different situation.
In the year 2005 CVSS 1.0 was published to rate the severity of vulnerabilities.

However, organizations encountered significant issues when they tried to make use of CVSS 1.0. In the meantime, the already existing Forum of Incident Response and Security Teams (FIRST) became the custodian of CVSS.
This led to the quick development of CVSS version 2.0, released in 2007. 8 years later, further feedback of organizations resulted in the release of CVSS version 3.0.
The current version 3.1 (released in July 2019) clarifies concepts introduced in CVSS 3.0 and provides additional guidance. For instance, 3.1 explicitly states 
that CVSS measures “the severity of a vulnerability and should not be used alone to assess risk”.

### How to use :

It is important to understand the basic idea of CVSS. The final result of using CVSS 3.1 is a score and a vector string. Both are results of a calculation that is based on three different metrics:

- base metrics (obligatory)
- temporal metrics (optional)
- environmental metrics (optional)

The final score ranges from 0.0 (no vulnerability present) to 10.0 (extremely severe vulnerability).


## [+] CVE
CVE stands for Common Vulnerabilities and Exposures which is maintained by Mitre Corporation , a not-for-profit organization.

### History
Years ago, different organizations used different names for publicly-known vulnerabilities in software. There were no unique names or identifiers for vulnerabilities. This resulted in confusion. CVE is an open standard that offers globally unique identifiers for vulnerabilities to solve this problem.

In 1999, the Mitre Corporation presented the concept of a CVE system. Later that year, the initial list of 321 CVE entries was created. One year later, the first 29 organizations adapted the system to provide CVE-compatible identifiers for more than 40 products. Since 2002, the NIST (National Institute of Standards and Technology) recommends using CVE for US agencies. At the moment, there are nearly 115,000 registered CVE entries.

### How to Use
CVE identifiers are assigned by CVE Numbering Authorities (CNAs). The Mitre Corporation administers the whole CVE system, and oversees the different CNAs. As of April 2019, there are 94 CNAs in 16 different countries. Each CNA has a defined scope for which it can assign CVE identifiers. If the affected product is out-of-scope of all CNAs, the Mitre Corporation can be contacted to get a CVE identifier.

Nowadays, CVE identifiers consist of three parts:

- the “CVE” prefix
- year of application for the CVE identifier (e.g., “2019”)
- unique number that is reset each year (4 or more digits)
