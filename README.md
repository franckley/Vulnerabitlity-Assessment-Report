# **Vulnerability Assessment Report**

**1st Jan, 2024**

---

### System Description

The server hardware features a robust CPU processor and 128GB of memory. It operates on the latest version of the Linux operating system and hosts a MySQL database management system. The server is configured with a stable network connection using IPv4 addresses and communicates with other servers on the network. Security measures include SSL/TLS encrypted connections.

### Scope

The scope of this vulnerability assessment focuses on the current access controls of the system. The assessment spans a three-month period, from June 2024 to August 2024. NIST SP 800-30 Rev. 1 is used to guide the risk analysis of the information system.

### Purpose

The database server is a centralized computer system that stores and manages large amounts of data. It is used to store customer, campaign, and analytic data, which can later be analyzed to track performance and personalize marketing efforts. Securing this system is crucial due to its regular use in marketing operations.

### Risk Assessment

| Threat Source | Threat Event                                 | Likelihood | Severity | Risk |
|---------------|----------------------------------------------|------------|----------|------|
| Hacker        | Obtain sensitive information via exfiltration| 3          | 3        | 9    |
| Employee      | Disrupt mission-critical operations          | 2          | 3        | 6    |
| Customer      | Alter/Delete critical information            | 1          | 3        | 3    |

### Approach

Risks were assessed considering the data storage and management procedures of the business. Potential threat sources and events were determined based on the likelihood of a security incident given the open access permissions of the information system. The severity of potential incidents was evaluated against their impact on day-to-day operational needs.

### Remediation Strategy

To ensure only authorized users access the database server, the following measures will be implemented:

- **Authentication:** Strong passwords and multi-factor authentication.
- **Authorization:** Role-based access controls to limit user privileges.
- **Auditing:** Mechanisms to track and log access.
- **Encryption:** Use TLS for data in motion instead of SSL.
- **IP Allow-Listing:** Restrict access to corporate offices, preventing random internet users from connecting to the database.
