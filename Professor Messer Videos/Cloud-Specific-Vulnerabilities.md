# Adoption of Cloud Applications

- In a relatively short period of time, companies have embraced cloud technology, leading to a scenario where practically every organization operates one or more applications in a public cloud.
- These cloud-based applications often handle a significant amount of data, including sensitive information that requires robust security measures.

## Security Practices and Vulnerabilities

- Despite the widespread adoption of cloud applications, many organizations do not follow best practices for security, which poses significant risks.
- For instance, it is estimated that 76% of organizations fail to implement multi-factor authentication for accessing their central cloud systems.
- Additionally, about 63% of the code in the cloud remains unpatched, which presents serious security vulnerabilities that can be exploited by attackers.
- These vulnerabilities are often rated with a Common Vulnerability Scoring System (CVSS) score of seven or higher, indicating a high level of risk.

## Threats from Public Cloud Accessibility

- The nature of public cloud applications allows anyone globally to attempt to connect to these services, which increases the risk of potential attacks.
- Attackers can launch various types of denial of service (DoS) attacks, including distributed denial of service (DDoS) attacks, from multiple devices across the internet.
- The authentication methods employed to access these applications are critical; weak or misconfigured authentication can lead to significant data breaches.

## Misconfigurations and Directory Traversal Risks

- Common misconfigurations, such as allowing directory traversal on web servers, can enable unauthorized users to navigate the server's file structure and access sensitive directories.
- If a system is unpatched, attackers may exploit existing vulnerabilities to execute remote code, potentially gaining full control over the cloud-based system.

## Importance of Regular Updates and Patching

- Maintaining updated operating systems and applications is essential for securing cloud environments against known vulnerabilities.
- Historical examples, such as vulnerabilities in Log4J and Spring Cloud, illustrate how easily attackers can exploit unpatched applications to gain deeper access to cloud systems.

## Exploitation Techniques and Attack Strategies

- Attackers may utilize various techniques, such as cross-site scripting, to exploit input validation failures in applications, allowing them to infiltrate systems.
- Out-of-bounds write vulnerabilities enable attackers to write unauthorized information into memory, which can lead to remote code execution or system crashes.
- Since applications in the cloud also store data in cloud databases, attackers often employ code injection methods like SQL injection to access sensitive data stored within these databases.

