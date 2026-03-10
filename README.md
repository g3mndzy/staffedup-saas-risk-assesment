# staffedup-saas-risk-assesment


So you've landed your first cybersecurity internship — now what?

First, congratulations. Breaking into cybersecurity in today’s job market is no small accomplishment. But landing the internship is only the beginning.

Many students focus heavily on offensive security labs and hacking tools. While those skills are valuable, most entry-level security roles focus on something different: understanding systems, identifying risks, and recommending improvements.

When preparing for my internship, I realized success isn’t just about knowing tools. It’s about understanding how modern systems work and how security frameworks can be used to evaluate and protect them.

Let's be real, you don't want to be the intern that is sitting down idly twiddling your thumbs. An exceptional intern asks questions, is naturally curious, and makes connections. These qualities come from calculated preparation. So let's jump into some fundamentals that will definitely allow you to have a better understanding of your role so you can hit the ground running.

**GOAL**: After reading this you will understand how SaaS infrastructure works, common vulnerabilities, frameworks to be familiar with in guiding your vulnerability assessments, and some questions that you can ask to wow your employer!

My project entails performing a vulnerability assessment of a segment of assets and recommending strategies to improve. Being that the company I am working for is a SaaS company, that was my first stop for research. Let's dive in.

# SaaS Architecture Basics
In today's landscape, companies are moving to a more modern approach to house their applications, services, and data in the cloud. SaaS architecture is essential for building dynamic applications that meet consumer needs and can be scalable over time. Well-structured architecture is essential for seamless business operations.

The SaaS model represents a cloud-based approach where businesses have access to applications without installing heavy software onto their physical computers. Generally, the trend is that businesses are moving toward cloud-based software to cut down on costs that would occur due to on-premise maintenance.

One form of architecture is multi-tenant architecture, which lets multiple users access a single application. To access it, users pay a yearly or monthly fee. One benefit of this cloud-based approach is that these applications have automatic updates, built-in security patches, and a pay-for-what-you-use structure. SaaS applications often have APIs integrated for customization. The provider handles data storage and security. 

## Components of SaaS Infrastructure

SaaS environments consist of several interconnected components. Next, let's examine some of the common elements that make up a typical SaaS system.

- Intuitive User Interface
- Data storage and access
- Authentication and authorization
- Seamless integrations
- Scalability and performance
- Security
- Monitoring and logging
- Billing and subscription management
- Robust infrastructure
- Compliance and governance

# SaaS Security Risks

As you can see, SaaS architecture involves many interconnected components, and with that complexity comes significant security risks. For example, vulnerabilities from integrating third-party APIs that unknowingly have faulty code can increase risk. Additionally, having microservices that are codependent on one another can lead to cascading failure since one API's inoperability can lead to issues with another API.

Because microservices need to be properly configured and often forego defense-in-depth mechanisms usually employed by monolithic services, it can increase the network attack surface since there are more discoverable IPs and margins of error.

Cloud storage is a pillar in SaaS architecture, so there needs to be consideration on how data is stored and the risks associated with using the cloud. Things to consider include if one system is compromised in a shared environment, that increases the attack surface and allows threat actors to gain elevated access to information.
Additionally, the cloud provider should be in a country that has ample security laws that protect data and has certain standards for data storage and transmission. There should be end-to-end encryption to ensure that the data is secure and no one can intercept this data. Data should also be stored at rest, further highlighting the need for good security practices at the physical location where this data is stored.

Finally, as an organization, data should not just be stored in the cloud. A part of the CIA triad is availability. If one way to get data is not available, that disrupts services and business operations. So have a physical backup copy that is routinely updated in case of these emergencies.

Another thing to consider is authentication flow. Users want both ease of access and security. It is a delicate balance between increasing security, which adds more steps for users to log on, and actual user usability.
Especially with multi-tenant architecture, it is essential that authentication is configured correctly to mitigate or eliminate data leakage or cross-tenant access. Multifactor authentication is a common security layer used in SaaS platforms. However, there are levels to MFA flows.

Weak flows include relying on SMS or OTP, which have their own set of vulnerabilities. More secure MFA workflows include using passkeys and authenticators. Other MFA options include magic links and adaptive MFA (reliant on geolocation, login behavior, and device reputation). Moving forward, let's take a look at how organizations can mitigate these risks and better secure their systems.

# Cloud Security

Cloud security refers to policies and controls implemented to protect data, applications, and infrastructure and mitigate misconfigurations and unauthorized usage. Cloud security differs from on-premise security in a myriad of ways including, but not limited to:

- Misconfigurations and visibility gaps
- Identity and access complexities
- Shared responsibility confusion
- Rapidly changing infrastructure

With this comes a shared responsibility model: the customer is responsible for IAM configurations, and cloud providers are responsible for securing underlying infrastructure including the physical data centers.

Cloud security best practices include:

1.Maintain continuous asset visibility
2.Enforce strong identity and access management
3.Establish and reinforce secure baselines and monitor for drift
4.Protect data in transit and at rest (encryption)
5.Centralized log collection and monitoring
6.Incident response planning for cloud-specific incidents

The need for corporations to achieve cloud migration while retaining security has become increasingly challenging. With the advancement of AI, threat actors are harnessing the power of this tool in order to launch highly sophisticated attacks on cloud environments.

Here are some examples of SaaS threats:

- Data breaches due to IAM misconfigurations or inadequate encryption
- Account hijacking due to threat actors using stolen credentials
- Insecure APIs that are prone to attack if not properly vetted or secured
- DoS attacks that lead to business losses due to downtime
- Insider threats
- Compliance violations where businesses are not meeting regulatory standards to secure their data
- Supply chain attacks

When conducting your vulnerability assessment, these are factors to consider. While these cloud security practices are important, organizations often rely on established security frameworks to guide how these protections are implemented and managed.

# Security Frameworks

There are many security frameworks, and this is not an exhaustive list. You do not need to memorize every framework, but you should be familiar with the following ones. These frameworks help organizations identify risks, implement security controls, and continuously improve their security posture.

**NIST CSF** is used to help organizations manage and reduce cybersecurity risk. According to CSF 2.0, the functions include:
* Govern – Policy, cybersecurity risk management, and expectations are monitored
* Identify – Current cybersecurity risks are understood
* Protect – Safeguards are put in place
* Detect – Cybersecurity attacks are found and analyzed
* Respond – Actions are taken against cybersecurity incidents
* Recover – Operations that were affected are restored

**ISO 27001** is an information security management standard that provides organizations with a structured framework to safeguard information.

**STRIDE** is another framework to be familiar with for threat modeling, which will be discussed in the next section. It helps teams identify potential security threats by classifying them into six categories:

1. Spoofing
2. Tampering
3. Repudiation
4. Information Disclosure
5. Denial of Service
6. Elavation of Privilege
   
**OWASP Top 10** is the Open Web Application Security Project that focuses on the ten most critical risks to web applications. These include:

1. Broken Access Controls
2. Cryptographic Failures
3. Injection
4. Insecure Design
5. Security Misconfiguration
6. Vulnerable and Outdated Components
7. Identification and Authentication Failures
8. Software and Data Integrity Failures
9. Security and Logging Failures
10. Server-side Request Forgery


# Threat Modeling

While security frameworks provide structured guidance for managing risk, organizations must also identify the specific threats that could impact their systems. This is where threat modeling becomes an important part of the security process. Threat modeling is the identification and representation of all threats that could affect the security of applications, software, systems, networks, and other digital assets. It is the process of capturing and analyzing potential undesirable events and assessing vulnerabilities before they can be exploited.

A common framework used in threat modeling revolves around **four key** questions:

1. What are we working on?
This is determined by assessing the scope of the project and understanding the architecture, assets, and data flows within the system.

3. What can go wrong?
Potential threats are modeled using techniques such as STRIDE, cyber kill chains, or attack trees to identify possible attack vectors.

5. What are we going to do about it?
Mitigation strategies are implemented to reduce risk. Organizations may choose to mitigate, accept, transfer, or eliminate specific risks depending on the severity and likelihood of the threat.

7. Did we do a good job?
After mitigation strategies are implemented, the security plan should be reviewed to determine whether the system is sufficiently protected and whether additional safeguards are needed.

Once potential threats have been identified through threat modeling, organizations must implement systems that allow them to detect suspicious activity and respond quickly. This is where logging and monitoring become essential.

# Logging and Monitoring using SIEMs

Another important aspect of system health is logging and monitoring. Logging is the collection of records that capture events occurring within systems, applications, and networks, while monitoring involves using tools to analyze and evaluate those logs and metrics. By inspecting these logs, security teams are able to troubleshoot errors and identify suspicious activity that may occur within their environments.

SIEM, or Security Information and Event Management, provides log aggregation along with real-time monitoring and analysis. By collecting logs from multiple systems into a centralized location, SIEM platforms greatly enhance an organization's ability to monitor and secure its IT infrastructure.

A SOC analyst typically specializes in monitoring these SIEM platforms in order to detect anomalies and potential security incidents. Some popular SIEM platforms that you can use in your home labs are Splunk or Wazuh if you want to practice setting up and configuring dashboards to monitor different security events. However, that is beyond the scope of this article.Through my own experience working with SIEM tools, it emphasized how important it is to continuously monitor systems to maintain visibility and detect threats early.

# Questions to Guide Your Internship

In order to effectively monitor systems and detect potential threats, security teams must first understand how those systems are built and how data flows through them. This understanding often begins by asking the right questions during the early stages of an assessment.

Now that you know the basics, it's time to actually start your first kickoff call. In my own experience, the floor was opened immediately for us to ask any questions we had in order to begin performing our role.

While that initially caught me off guard, I wasn't completely unprepared. One of the first things I asked was for the CEO to identify the assets we would be working with and describe how the environment functioned. From there, the head of security walked us through the platform’s infrastructure and explained how the system was structured.

Moving forward, with my team we came up with a list of questions to further get a better sense of what we would be dealing with. You can use the questions below and tailor them based on your specific project.

- Where is the web app hosted? AWS, Azure, Google Cloud, Other?
- What components make up the application?
- Frontend framework (React, Angular, etc.)
- Backend services
- APIs
- Database
- Are there microservices or a single backend service?
- Are there separate environments?
- Development, Staging, Production
- What applicant or business data is collected?
- Is any of it regulated?
- Is it encrypted in transit? Is it encrypted at rest?
- How do users authenticate? Is there MFA in place?
- Can someone upload documents?
- What file types are allowed?
- Are files scanned for malware?
- Where are the files stored?

This initial conversation helped us understand the environment we were assessing and ensured that our vulnerability assessment was grounded in a clear understanding of the system. From there, the real work began.

I hope this article provided a helpful introduction into how cybersecurity professionals approach systems, risks, and security planning. Of course, the research does not end here. Continuing to close knowledge gaps before your internship begins will help ensure that you are not overwhelmed and that you can confidently ask questions, make connections, and leave a strong impression.

Sources
https://innovecs.com/blog/essential-guide-to-saas-architecture/
https://www.sei.cmu.edu/blog/3-api-security-risks-and-recommendations-for-mitigation/
https://www.sei.cmu.edu/blog/stop-imagining-threats-start-mitigating-them-a-practical-guide-to-threat-modeling/
https://www.descope.com/blog/post/saas-auth
https://www.cisa.gov/resources-tools/training/get-most-out-cloud-storage-and-services-while-minimizing-risk
https://www.darktrace.com/cyber-ai-glossary/the-most-common-cloud-security-threats
https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf
https://owasp.org/www-community/Threat_Modeling
https://www.securitycompass.com/blog/stride-in-threat-modeling/
https://www.paloaltonetworks.com/cyberpedia/what-is-siem logging#:~:text=SIEM%20Logging%20is%20a%20crucial,stage%20helps%20achieve%20that%20goal.
https://www.cloudflare.com/learning/security/threats/owasp-top-10/

