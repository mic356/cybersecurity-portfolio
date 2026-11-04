NjikoTrade – External Website Security Assessment

Assessment Type: Preliminary External Security Assessment
Target: NjikoTrade
Domain: njikotrade.com
Tools Used: Nmap, SQLmap, cURL, nslookup, Linux Terminal
Assessment Date: November 2026
Assessment Status: Completed – Preliminary Assessment
Author: CyberLord

1. Project Overview

This project involved conducting a preliminary external security assessment of the NjikoTrade website to examine its publicly observable network and web security characteristics.

The assessment focused on domain reconnaissance, HTTP response analysis, port scanning, technology identification and preliminary SQL injection testing.

Testing was conducted with the website owner's permission.

2. Objectives

- Identify the website's publicly observable network information.
- Examine HTTP and HTTPS responses.
- Identify exposed network services.
- Review security-related HTTP headers.
- Perform preliminary SQL injection testing.
- Document observations and recommend further security checks.

3. Tools and Techniques

Tool| Purpose
Nmap| Network and port scanning
SQLmap| Preliminary SQL injection testing
cURL| HTTP response and header inspection
nslookup| DNS and domain resolution
Linux Terminal| Command-line investigation

4. Assessment Activities

A. DNS Reconnaissance

Used "nslookup" to examine domain resolution.

Observation: The domain resolved to a public IP address.

B. Network Scanning

Used Nmap to perform a top-100 TCP port scan.

Result:

- 100 ports reported as filtered.
- No open ports identified in the scan.

Interpretation: The scan did not identify accessible TCP services among the tested ports. Filtering may be caused by firewall or network security controls.

C. HTTP Header Analysis

Used:

"curl -I https://njikotrade.com"

Observations:

- HTTP/2 200 response.
- Cloudflare identified in the server response.
- Strict-Transport-Security header present.
- X-Content-Type-Options header present.
- Referrer-Policy header present.

These observations indicate that several security-related HTTP headers were configured.

D. Technology Identification

Inspected publicly accessible website source and resources.

Technologies and indicators observed:

- React
- Vite
- Lovable-related development indicators
- Cloudflare infrastructure

E. SQL Injection Testing

Used SQLmap for a preliminary test:

"sqlmap -u https://njikotrade.com"

Result:

- HTTP 403 response received.
- Possible web application firewall or security filtering.
- No URL parameters were supplied.
- No SQL injection vulnerability was confirmed.

Important: An HTTP 403 response does not prove that a website is vulnerable or that SQL injection exists.

5. Key Findings

1. The website resolved successfully through DNS.
2. The Nmap scan reported 100 filtered ports and no open ports.
3. The website returned an HTTP/2 200 response during header inspection.
4. Cloudflare was identified in the HTTP response.
5. Several security-related HTTP headers were present.
6. SQLmap received an HTTP 403 response, and no SQL injection vulnerability was confirmed.

6. Limitations

This was a preliminary external assessment.

The assessment did not include:

- Authenticated testing.
- Backend or database access.
- Source-code review.
- Hosting control-panel inspection.
- A complete manual web application penetration test.

Therefore, the results should not be interpreted as proof that the website is completely secure.

7. Recommendations

- Conduct regular vulnerability assessments.
- Review server and application security configurations.
- Maintain updated software dependencies.
- Review authentication and access-control mechanisms.
- Perform authorised authenticated testing when access is available.
- Review application logs and firewall configurations.

8. Conclusion

The preliminary assessment identified publicly observable infrastructure and security configurations but did not confirm an exploitable vulnerability.

Further testing with appropriate application and hosting access would be required to provide a more comprehensive security assessment.

Project Author: CyberLord
Field: Network Security and Web Application Penetration Testing
