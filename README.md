# Foundations_Lab_Final
**Student Name:** [Isabelli duran]
**Course:** Cybersecurity Foundations Intensive: Night 4
**Date:** February 26, 2026
**Instructor:** [George]

---

## Technical Overview
Hello World. This repository serves as the primary workbench for the Foundations Lab.
# Foundations Lab Final: Professional Identity & Workbench 

---

## Case Study: Chinese Surveillance Network Data Breach (June 2025)

### Technical Analysis
* **Incident Summary:** A misconfigured Elasticsearch database resulted in the exposure of approximately **4 billion records** (631 GB) of surveillance data.
* **CIA Triad Failure:** **Confidentiality.** The data was publicly accessible due to a total lack of encryption and access controls.
* **AAA Breakdown:** **Authentication.** The system failed at the first pillar of AAA; there was no password challenge or multi-factor authentication (MFA) required to access the administrative layer.
* **Governance Gap:** **Access Control Policy.** The organization failed to implement a "Deny-All" default posture. The gap was a lack of basic authentication mechanisms rather than a failure of granular least-privilege permissions.

### Professional Recommendations
To remediate this vulnerability, the organization must:
1. Implement **Mandatory MFA** for all database administrative interfaces.
2. Deploy a **Web Application Firewall (WAF)** to restrict traffic to known IP ranges.
3. Conduct automated **Cloud Configuration Audits** to detect publicly facing assets.

### References
Buckman, B. (2025, October 3). *27 biggest data breaches globally (+ lessons)*. Huntress. https://www.huntress.com/blog/biggest-data-breaches
