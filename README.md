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
- SaaS Security Risks

With SaaS models, there are also significant security risks. For example, vulnerabilities from integrating third-party APIs that unknowingly have faulty code can increase risk. Additionally, having microservices that are codependent on one another can lead to cascading failure since one API's inoperability can lead to issues with another API.

Because microservices need to be properly configured and often forego defense-in-depth mechanisms usually employed by monolithic services, it can increase the network attack surface since there are more discoverable IPs and margins of error.

Cloud storage is a pillar in SaaS architecture, so there needs to be consideration on how data is stored and the risks associated with using the cloud. Things to consider include if one system is compromised in a shared environment, that increases the attack surface and allows threat actors to gain elevated access to information.
Additionally, the cloud provider should be in a country that has ample security laws that protect data and has certain standards for data storage and transmission. There should be end-to-end encryption to ensure that the data is secure and no one can intercept this data. Data should also be stored at rest, further highlighting the need for good security practices at the physical location where this data is stored.

Finally, as an organization, data should not just be stored in the cloud. A part of the CIA triad is availability. If one way to get data is not available, that disrupts services and business operations. So have a physical backup copy that is routinely updated in case of these emergencies.

Another thing to consider is authentication flow. Users want both ease of access and security. It is a delicate balance between increasing security, which adds more steps for users to log on, and actual user usability.
Especially with multi-tenant architecture, it is essential that authentication is configured correctly to mitigate or eliminate data leakage or cross-tenant access. Multifactor authentication is a common security layer used in SaaS platforms. However, there are levels to MFA flows.

Weak flows include relying on SMS or OTP, which have their own set of vulnerabilities. More secure MFA workflows include using passkeys and authenticators. Other MFA options include magic links and adaptive MFA (reliant on geolocation, login behavior, and device reputation).

# Cloud Security
Cloud security refers to policies and controls implemented to protect data, applications, and infrastructure and mitigate misconfigurations and unauthorized usage. Cloud security differs from on-premise security in a myriad of ways including, but not limited to:
-Misconfigurations and visibility gaps
-Identity and access complexities
-Shared responsibility confusion
-Rapidly changing infrastructure

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

When conducting your vulnerability assessment, these are factors to consider.

# Security Frameworks
You do not need to memorize every framework, but you should be familiar with the following ones.

**NIST CSF** is used to help organizations manage and reduce cybersecurity risk. According to CSF 2.0, the functions include:
* Govern – Policy, cybersecurity risk management, and expectations are monitored
* Identify – Current cybersecurity risks are understood
* Protect – Safeguards are put in place
* Detect – Cybersecurity attacks are found and analyzed
* Respond – Actions are taken against cybersecurity incidents
* Recover – Operations that were affected are restored

**ISO 27001** is an information security management standard that provides organizations with a structured framework to safeguard information.

**STRIDE** is another framework to be familiar for threat modeling which will be discussed in the next section. This helps teams identify potential security threats by classifying them into 6 categories.
1. Spoofing
2. Tampering
3. Repudiation
4. Information Disclosure
5. Denial of Service
6. Elavation of Privilege

# Threat Modeling

Threat modeling is the identification and representation of all threats that could affect the security of applications, software, systems, networks, and other digital assets. It is the process of capturing and analyzing potential undesirable events and assessing vulnerabilities before they can be exploited.

A common framework used in threat modeling revolves around **four key** questions:

1. What are we working on?
This is determined by assessing the scope of the project and understanding the architecture, assets, and data flows within the system.

3. What can go wrong?
Potential threats are modeled using techniques such as STRIDE, cyber kill chains, or attack trees to identify possible attack vectors.

5. What are we going to do about it?
Mitigation strategies are implemented to reduce risk. Organizations may choose to mitigate, accept, transfer, or eliminate specific risks depending on the severity and likelihood of the threat.

7. Did we do a good job?
After mitigation strategies are implemented, the security plan should be reviewed to determine whether the system is sufficiently protected and whether additional safeguards are needed.


# Logging and Monitoring using SIEM's

Another important aspect of system health is logging and monitoring. Logging is the collection of logs that hold record of events while monitoring is the use of tools to analyzeand evaluate those metrics. By inspecting these logs, teams are able to troubleshoot errors that may occurs. SIEM or Security Information and Event Management provides log aggreagation and real time monitoring and analyses. SIEM logging greatly enhances an organizations ability to monitor and secure their IT systems. 

A SOC analyst specialized in monitoring these SIEM's in order to detect any anomolies. Some popular SIEM's that you can use in your homelabs are splunk or Wazuh if you want to practice setting up and configuring a dashboard to monitor different events (but that is beyond the scope of this article). Through my own practices of using SIEM's, it truly emphasized to me how important it is to constantly monitor systems. 


# Questions to Guide Your Internship
Now that you know the basics, it's time to actually start your first kickoff call. In my own experience, the floor was opened immediately to us in order to ask any questions we had to perform our job function.

While that caught me off guard, I wasn't totally unprepared. I first asked the CEO to name all of the assets we would be working with and describe the flow of the environment. Then we had the head of security explain the infrastructure of the platform we would be working with.

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

From here is where the real work begins. I hope you enjoy this brief introduction into how a cybersecurity professional thinks. Of course the research does not end here. Close any gaps you might have before your internship starts so it is not overwhelming and you can confidently ask questions, make connections, and leave a good impression.

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

