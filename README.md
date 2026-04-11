# Internship Journal Entries – Cybersecurity Risk Assessment & Policy Development

## Reflection #1
(Midway Internship Reflection – Vulnerability Assessment Project)

This internship has already provided invaluable real-world cybersecurity experience. From the start, the responsibility to drive the vulnerability assessment was placed on my team and I, and I took initiative early by stepping into a leadership role to help organize our approach and guide discussions.

One of the key areas I contributed to was project management and team coordination. I developed structured meeting templates to guide the flow of our discussions and ensure we stayed aligned on objectives. In addition, I created a vulnerability assessment template, which we are now using to begin drafting our final deliverable. This required researching how security professionals document their work and understanding how frameworks are applied in real-world assessments.

Our team consists of individuals with varying technical backgrounds, which I saw as an advantage. I actively collaborated with teammates by leveraging their strengths and perspectives to deepen our analysis. Together, we developed a comprehensive set of assessment questions across multiple security domains, including:
- Business continuity and resilience
- Application architecture and infrastructure
- Authentication and identity management
- Authorization and access control
- Applicant data privacy and protection
- API security
- Third-party services
- Logging and monitoring
- Vulnerability management

During our discussions with the company, I also identified a lack of clarity in the scope of the vulnerability assessment. To address this, I took the initiative to ask targeted questions to better define expectations. Specifically, I asked whether the assessment should:
- Be conducted solely through interviews and documentation review
- Include hands-on access to systems such as AWS for configuration analysis
- Involve the use of vulnerability scanning tools
- Require the creation of security policies aligned with industry standards

By clarifying these points, we were able to align expectations with the company, and they confirmed that our team would be moving forward with a comprehensive and in-depth assessment approach.

Currently, I am working on outlining the next steps and creating a structured plan to guide our team toward completing the final deliverable. This includes defining responsibilities, organizing our findings, and ensuring we are aligned with security frameworks and best practices.

This experience has been valuable not only in strengthening my cybersecurity knowledge, but also in developing my leadership, communication, and project management skills. I’ve had the opportunity to lead discussions, coordinate team efforts, and contribute to a real-world security assessment in a meaningful way. I’m excited to continue building on this momentum as we move into the next phase of the project.

##  Reflection #2


During my cybersecurity internship, I worked as part of a team conducting a structured security assessment of a SaaS platform. The engagement focused on evaluating the organization’s current security posture through stakeholder interviews and identifying gaps across key security domains.

### Key Findings

Through our assessment, we identified several critical security gaps:

- Multi-Factor Authentication (MFA) was not enforced for administrative accounts
- Encryption controls for sensitive data stored in AWS S3 were not clearly defined or validated
- No centralized logging or SIEM solution was in place for monitoring and detection
- No formal vulnerability management process existed
- Patch management procedures were not implemented
- No incident response plan had been established
- No documented review of third-party compliance (e.g., Stripe) was confirmed
- Uploaded files were not scanned for malware
- Data backup and redundancy practices were not clearly defined

### Framework Alignment

To address these risks, we aligned our recommendations with established industry frameworks, including:

- NIST Cybersecurity Framework (NIST CSF)
- PCI DSS
- SOC 2

### Policy Development

Based on our findings, we developed over 20 security policies covering key areas such as:

- Access control and MFA enforcement  
- Encryption and data protection  
- Logging and monitoring  
- Vulnerability and patch management  
- Incident response planning  
- Security awareness and training  
- Password and authentication policies  
- Token management and session control  
- Secure payment handling practices  

Each policy included:
- The associated risk
- A summary of the control objective
- Specific, actionable requirements

All policies and recommendations were documented in a centralized Google Sheets deliverable to support visibility, prioritization, and future implementation.

This experience reinforced the importance of security policies as a foundation for protecting sensitive data and maintaining business continuity. It also highlighted how many organizations, especially growing SaaS companies, may lack formalized security controls despite handling critical data.

Additionally, I gained hands-on experience in:
- Translating technical risks into business-impact language
- Mapping real-world gaps to industry frameworks
- Developing structured, scalable security policies

We are currently awaiting confirmation on whether a vulnerability scan will be conducted to further validate our findings through technical testing.
