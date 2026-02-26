# staffedup-saas-risk-assesment
Cybersecurity Intern Project with Riipen


# Initial Research
As a junior cybersecurity consultant, my job is to 
- identify assets
- identify risks
- rate risks
- recommend fixes
- communicate clearly to leadership

Prior to starting the project, I developed my foundation knowledge of Saas Architecture Basics, Access Control Models, Cloud security Foundamentals, Common Saas Threats, as well as NIST CSF and ISO 27001. 


## Saas Architecture Basics
Saas Architecutre is essential for building a dynamic applications that meet consumer needs and can be scalable over time. Well structured architecture is essential for seamless business operations. Saas model represents a cloud-based approach where businesses have access to applications without installing heavy software onto your physical computer. Generally, the trend is that businesses are moving towards cloud-based software to cut down on costs that would occur due to on premise maintanence. One form of architecture is multi-tenant architecture which lets multiple users access a single application. To access users pay a yearly or monthly fee. One benefit to this cloud based approach is that these applications have automatic updates, built in security patches and a pay for what you use structure. Saas applications often have API's integrated to customization. The provider handles data storage and security. 

CI/CD help automate updates and deploying them across shared applications.

Included are multierd software seperating data, business and presentation.

Technologies that aid in Saas Applications
- Containerization
- Orchestration
- Data virtualization

  Components of Saas Infrustructure
  1. Inutitive User Interface
  2. Data storage and access
  3. Authentication and authorization
  4. seamless integrations
  5. scalability and performance
  6. security
  7. monitoring and logging
  8. billing and subsription management
  9. robust infrustructure
  10. Compliance, and governance

With Saas Models, there are also significant security risks. For example, vulnerablities from intrgrating third party API's that unknowingly have faulty code can increase risk. Additionally, having microservices that are co-dependent on one another can lead to cascading failure since one API's inoperability can lead to the issues with another API. Becauase microservices neeed to be properly configures and often for go defense in depth mechanisms usually employed by monloithic services, it can increase the network attack verture since there are more discoverable IP's and margins of error. 

Cloud storage is a pillar in Saas archetiecture and so there needs to be consideration on how  data is stored and the risks associated with using the cloud. Things to consider include if one system is compromised in a shared environment, that increases the attack surface and allows threat actors to gain elevated access to information. Additonally, the cloud provider should be in a country that has ample security laws that protect data and has certain standards for data storage and transmission. There shold be end to end encryption to ensure that the data is secure and no one can intercepth this data. Data should also be stored at rest further highlighting the need for good security practices at the physical location where this data is stored. Finally as an organization, data should not just be stored in the cloud. A part of the CIA triad is availibity. If one way to get data is not avalible that distrutps services/business. So, have a physical backup copy that is routinely updated in case of these emergencies. 

Another thing to consider is Authentication flow. Users want both ease of access and security. It is a delicate balance between increasing security which adds more steps for users to log on and atual user usability. Especially with multi-tenant architecture, it is essential that authentication is configured correctly to mitigate or eliminate data leakage or cross tenant access. Multifactor authenticatio is a comman security layer used in SAas platforms. However there are levels to MFA flows. Weak flows include relying on SMS or OTP which has its own set of vulnerabilties. More secure MFA workflows include using passkeys  and authenticators. Other MFA options include magic links, adaptive MFA(reliant on geolocation, login behavior and device reputation)

Cloud Security
Clous securirty refers to policies and controls impletented to protect data, applications and infrastructure and mitigate misconfiguration and unaurthorizes usage. Cloud security differes from on premise security in a myriad of ways including but not limited to:
-Misconfigurations and visibiulity gaps
-Identidy and access complexities
-Shared responsibility confusion
-Rapidly changing infrastructure

With this comes a shared responsibility model: the customer is responsible to for IAM configurations and cloud providers are repsonsible for securing underlying infrastructure including the physical data.

Cloud security best practices include:
1. Maintain continous asset visibility
2. Enforce strong identity and access management
3. Establish/ reinforce secure baselines & monitor for drifts
4. Protecting data in transit and at-rest (encryption)
5. Centralized log collection/ monitoring
6. Incedent response planning for cloud specific incidents

 
Sources
https://innovecs.com/blog/essential-guide-to-saas-architecture/
https://www.sei.cmu.edu/blog/3-api-security-risks-and-recommendations-for-mitigation/
https://www.sei.cmu.edu/blog/stop-imagining-threats-start-mitigating-them-a-practical-guide-to-threat-modeling/
https://www.descope.com/blog/post/saas-auth
https://www.cisa.gov/resources-tools/training/get-most-out-cloud-storage-and-services-while-minimizing-risk
