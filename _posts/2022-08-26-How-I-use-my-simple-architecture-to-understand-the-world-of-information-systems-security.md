---
layout: post
date: 2022-08-26
title: How I use my simple architecture to understand the world of information systems security?
image: /images/article-1.jpeg]
excerpt: "Add here"
Keywords: Information Systems Security, Cyber Security
---

<img src="https://sud0x0.com/images/article-1.jpeg"  width="100%">
<p style="font-size:12px"><a href="https://www.pexels.com/photo/white-and-brown-concrete-building-1119972/" target="_blankl">Photo by Johannes Plenio.</a></p>

<br>

Before the article, I believe that having a correct understanding of the following terms is important. Therefore, I thought to place them at the top of the article. The meanings were taken from NIST glossary. 


[Cyber security](https://csrc.nist.gov/glossary/term/cyber_security){:target="_blank"} means the ability to protect or defend the use of cyberspace from cyber-attacks.

[Cyberspace](https://csrc.nist.gov/glossary/term/cyberspace){:target="_blank"} means a global domain within the information environment consisting of the interdependent network of information systems infrastructures including the Internet, telecommunications networks, computer systems, and embedded processors and controllers.

An [information environment](https://csrc.nist.gov/glossary/term/information_environment){:target="_blank"} means the aggregate of individuals, organizations, and systems that collect, process, disseminate, or act on information.

An [information system](https://csrc.nist.gov/glossary/term/information_system){:target="_blank"} is a discrete set of information resources organized for the collection, processing, maintenance, use, sharing, dissemination, or disposition of information.

[Information resources](https://csrc.nist.gov/glossary/term/information_resources){:target="_blank"} means information and related resources, such as personnel, equipment, funds, and information technology.

[Information systems security](https://csrc.nist.gov/glossary/term/information_systems_security){:target="_blank"} means the protection of information systems against unauthorized access to or modification of information, whether in storage, processing, or transit, and against the denial of service to authorized users, including those measures necessary to detect, document, and counter such threats.

[Information security](https://csrc.nist.gov/glossary/term/information_security){:target="_blank"} means the protection of information and information systems from unauthorized access, use, disclosure, disruption, modification, or destruction in order to provide confidentiality, integrity, and availability.

An [enterprise](https://csrc.nist.gov/glossary/term/enterprise){:target="_blank"} means an organization with a defined mission/goal and a defined boundary, using information systems to execute that mission, and with responsibility for managing its own risks and performance.


I personally understand information systems security as a combination of both cyber security and information security. The NIST definition for information systems does not directly mention whether non-technical systems (such as a file cabinet) are considered information systems or not. But some of the definitions that are on the internet describe an information system as a sociotechnical system. Even definitions for information systems do not cover paper-based non-technical methods directly, there is a significant portion of physical security and information classification integrated into information systems security. The image below describes how I see these relationships.

A side note: CISO is one of the highest roles assigned to the enterprise information security architecture within an organisation.  The CISO handbook, written by cio.gov, mentions that security of both information and information systems is a responsibility of the CISO. It also mentions that a CISO should use standards such as FIPS 199. FIPS 199 covers both information (electronic or non-electronic) and information systems. Consequently, I believe that understanding information systems security as a combination of both information security and cyber security is the correct method. [[CISO Guidebook](https://www.cio.gov/resources/ciso-handbook), [FIPS 199](https://nvlpubs.nist.gov/nistpubs/fips/nist.fips.199.pdf)]

![_config.yml]({{ site.baseurl }}/images/cyber-security-and-information-security.png)

Information systems inherit the risk of cyberspace components as once you connect the components to an information system, they become a part of the information system.

What are the other components in the cyberspace of the enterprise that are not related to the information system? This is an extremely small area. For example, assume that there is an abandoned AWS account connected to one of the enterprise credit cards. This AWS account does not hold any information related to the enterprise or does not have any connections to the enterprise computer network. Someone can call this an information system because of the company credit card information, but I doubt that, and I think that this is just a virtual component in the cyberspace. There is a business risk associated with this scenario. A threat actor can use this account to do financial damage to the organisation.

From my standpoint, the primary reason for maintaining the information systems security of an enterprise is to avoid any breach of confidentiality, integrity, or availability related to the enterprise’s information systems or information that they use. If breach of confidentiality, integrity, or availability of information systems or information that they use becomes a business risk, that could lead to potential problems for the enterprise. This includes reputational damage, financial damage, and cessation to exist.

Also, in my view, the information systems security architecture of an enterprise has two main activities.

- Identify the risk.
- Manage the risk.

Some examples are,

- if the computer network is open to the internet without a method to observe and manage the traffic, malicious activities could happen. This could lead to serious business risks. Therefore, enterprises apply network protection tools such as firewalls, DoS mitigation tools, SSL inspection, etc.
- if constant monitoring and log management of traffic does not happen within an enterprise, the threat actor can conduct their malicious activities unnoticed. The enterprise will not be able to at least limit the destruction that could be done by them. Therefore, enterprises apply methods like SIEM tools to constantly monitor the computer network.


Even though this sounds simple, information systems security is somewhat of a massive field with multiple subdomains. I believe that having a proper understanding of these sub-domains provides us with a greater benefit when it comes to working in information systems security.

I prefer minimalistic and non-complicated methods when it comes to learning. I like to categorise information and come up with patterns that would help me to understand the concepts easily. To understand the information systems security architecture of an enterprise, I thought to identify the main domains first, and then to identify their tasks. To do that, I used my own experience, peer articles, books, CISSP, CRISC, and CISA course syllabuses.

![_config.yml]({{ site.baseurl }}/images/information-systems-security-domains.png)

All these subdomains are interconnected. That means one domain's output can be an input for any other domain.
Some of the areas, such as "Information Systems Risk Management" and "Governance", go beyond the information systems security architecture. Thus, they are also connected to the enterprise architecture. One example is that a workplace hazard that could lead to an injury to an employee is not connected to information systems risk management directly. But it is a risk and must be managed.
 
I do not intend to write a lot of information about these subdomains in this article. But I would like to introduce each domain.

<br>

## Domain 1: Infrastructure and Application security

This domain covers all cloud-based, on-premises, and hybrid (combination of both on-prem and cloud) infrastructures. This domain is about planning, implementation, and maintenance of security tools, controls, and processes in the network. 

Some of the tools, controls, and processes are as follows:

<style>
  table {
    border-collapse: collapse;
  }
  td, th, table {
    border: 2px solid black;
  }
</style>

| **Tools/Controls**                 | **Processes**                                                  |
| ---------------------------------- | -------------------------------------------------------------- |
| Firewall                           | Feed the logs to SIEM tools                                    |
| WAF (Web Application Firewall)     | Whitelisting/Blacklisting based on threat intelligence reports |
| IPS/IDS                            | Timely malware scanning                                        |
| DNS Sinkhole                       | Centralised log management                                     |
| Proxy                              | Backups management                                             |
| DoS Protection                     |                                                                |
| Malware Scanners                   |                                                                |
| Email Protection                   |                                                                |
| Server and MOE security management |                                                                |
| Geo blocking                       |                                                                |
| Identity and Access Management     |                                                                |

Planning part of this domain is connected to domain 9. However, some of the important strategies to follow when working on this domain are Defense in Depth and Zero Trust. Identity and access management is not limited to this domain, but most of the implementation and maintenance parts happen here. This domain also focuses on some parts of the physical security of network tools and components. However, physical security is not limited to information systems security architecture.


<br>

## Domain 2: Asset Security Management

When it comes to information security, the primary focus is on information that the network and its components hold.  Besides information, there are other assets that are important to be protected, such as,
- software/applications,
- network components.

Assets are interconnected. For example, assume that there is an SQL server that contains sensitive data. If the physical server that the SQL server is installed on becomes unusable, the data may also become inaccessible. 

This domain focuses on how to secure these assets based on various frameworks and methods. For example, NIST SP 800-18 and NIST SP 800-171 Rev 3. 

When it comes to securing assets, some of the focus areas are,
- assets and data classification,
- managing an assets information inventory,
- security of assets (for example encryption at rest, encryption in transit, DLP, CASB),
- lifecycle of assets,
- assigning assets to relevant management layers.

<br>

## Domain 3: Security Operations

Domain 1 focuses on the security of the infrastructure. Domain 2 focuses on the classification and identification of all the assets to help other domians to manage the security. Domain 3 is where constant monitoring happens. For example,
- Is there a threat actor inside the enterprise?
- Is classified data stored in this software under a malicious attack?

The tasks of domain 3 are,
- infrastructure activity monitoring,
- analysing the logs using SIEM tools or manually,
- threat intelligence, 
- digital forensic,
- incident response,
- disaster recovery and business continuity.

Disaster recovery and business continuity are not limited only to this domain. This domain helps to plan and execute the plans when necessary. Disaster recovery and business continuity is an area that is connected to various parts of the main enterprise architecture. 

The Security Operations Centre (SOC) concept is focused on this domain. Other domains can also be parts of the SOC team depending on the enterprise structure and needs. The tasks of this domain are more aligned towards the blue team.

<br>

## Domain 4: Security Assessments

The monitoring part in domain 3 provides the enterprise with information about current activities. One example of an activity is a threat actor using a known exploit to get into an enterprise infrastructure component. What if the enterprise can identify the vulnerabilities that the infrastructure components have before the threat actor can? That’s the task of domain 4. The red team concept is focused on this domain.

I prefer to divide this domain into 2 main parts.
- Physical Security Assessments
- Cyber Security Assessments

Cyber security assessment has 2 main parts.
- Hybrid security assessments (use of both manual and automated techniques). Penetration testing is an example for this part.
- Automated security assessments. A vulnerability assessment (vulnerability scan) is an example for this part.

Penetration testing focuses on a smaller scope but goes deeper into that scope. Whereas, vulnerability assessments are usually focused on a larger scope, but do not go as deep as penetration testing.

Even though it is linked to this domain, I prefer to put code security reviews into the 7th domain. 

The NIST definitions for penetration testing, vulnerability assessments and vulnerability scanning are as follows. 

[Penetration testing](https://csrc.nist.gov/glossary/term/penetration_testing){:target="_blank"} is a method of testing where testers target individual binary components or the application as a whole to determine whether intra or intercomponent vulnerabilities can be exploited to compromise the application, its data, or its environment resources.

[Vulnerability assessment](https://csrc.nist.gov/glossary/term/vulnerability_assessment){:target="_blank"} is a systematic examination of an information system or product to determine the adequacy of security measures, identify security deficiencies, provide data from which to predict the effectiveness of proposed security measures, and confirm the adequacy of such measures after implementation.

[Vulnerability scanning](https://csrc.nist.gov/glossary/term/vulnerability_scanning){:target="_blank"} is a technique used to identify hosts/host attributes and associated vulnerabilities.

<br>

## Domain 5: Information Systems Risk Management

This domain focuses on managing the identified risk. Some of the tasks focused on this domain are,
- risk identification (this is more about converting the identified various types of risks to business risks by looking at the damage that could happen to the enterprise),
- risk treatment plans,
- management of the risk ownership,
- management of a risk register,
- develop, evaluate, and maintain information systems security related policies and procedures,
- providing inputs to the governance domain based on business risk patterns,
- third party risk management (supply chain risk),
- disaster recovery and business continuity.

Disaster recovery and business continuity are not limited only to this domain. This domain helps to plan methods when necessary.
Supply chain risk management is somewhat of a big area due to its scope. Thus, it has connections to multiple domains, including domain 1.

<br>

## Domain 6: Security Training

People are the weakest link in security. No matter how many controls are in place, a simple mistake by an employee could lead to massive damage. The main reason for this is that every single person in the enterprise is not security minded. Thus, providing them with the necessary knowledge about cyber security and assessing their knowledge is as important as the implementation of firewalls. 

The tasks of this domain include,
- development of study materials for employees,
- planning mandatory cyber security exercises for employees.

<br>

## Domain 7: Secure Development

Assessments and monitoring activities provide security to the enterprise, but what if the components that we use daily contain vulnerabilities after each simple update or upgrade? How do we minimise the risk of introducing new vulnerabilities to the network? That’s the task of secure development.

The main tasks of this domain include,
- implementation of secure development practises and policies
- source code security scanning (SAST, DAST) 

One of the most important methodologies to follow in this domain is DevSecOps. DevSecOps means adding security to the DevOps development methodology by introducing code scanning and secure practices. 

This domain may not exist in some enterprises, as some enterprises do not have their own development team. However, other enterprises follow a hybrid method (internal team and use of external vendors) when it comes to development.

<br>

## Domain 8: Information Systems Security Governance 

Governance is a system that provides a framework for managing organisations. It identifies who can make decisions, who has the authority to act on behalf of the organisation and who is accountable for how an organisation and its people behave and perform. [[Charted Governance Institute UK & Ireland](https://www.cgi.org.uk/professional-development/discover-governance/looking-to-start-a-career-in-governance/what-is-governance){:target="_blank"}]

Governance enables the management team and the board to run organisations legally, ethically, sustainably, and successfully, for the benefit of stakeholders, including shareholders, staff, clients, and customers, and for the good of wider society. [[Charted Governance Institute UK & Ireland](https://www.cgi.org.uk/professional-development/discover-governance/looking-to-start-a-career-in-governance/what-is-governance){:target="_blank"}]

Likewise, the organisational governance, information systems security governance is about the information systems security team and its contribution towards the enterprise. In my opinion, information systems security governance is primarily involved in the development and maintenance of the information systems security architecture. The information security architecture then becomes a heavy influence on day-to-day decision making.

Organisations that have good governance use clear decision-making processes, behave openly by reporting on their activities, actively engage with their stakeholders, effectively manage the risks they face, and take responsibility for controlling and protecting their assets, including their reputation. Each of these areas of governance activity contributes to an organisation’s success. [[Charted Governance Institute UK & Ireland](https://www.cgi.org.uk/professional-development/discover-governance/looking-to-start-a-career-in-governance/what-is-governance){:target="_blank"}]


<br>

## Domain 9: Enterprise Information Systems Security Architecture

In my opinion, this is the key to better enterprise information systems security. A well-defined architecture not only protects the enterprise information systems but also helps with better governance.

The information security architecture defines the following main areas:
- Information systems security standards, mechanisms, processes, and frameworks from configurations to decision-making.
- The relationship is in-between the main enterprise architecture and the information systems security architecture.
- Information systems security-related policies.
- Information system security services and goals.
- Employees' roles and responsibilities in information system security.

There are multiple architecture models covering different parts of information systems security and enterprise architecture that can work together. One example is as follows:

TOGAF is the enterprise level architecture. SABSA covers the information systems security architecture but does not provide any specific control and relies on others. COBIT is also an enterprise level architecture. 

By using SABSA, COBIT and TOGAF together, a security architecture can be defined that is aligned with business needs and addresses all the stakeholder requirements. After the architecture and the goals are defined, the TOGAF framework can be used to create the projects and steps and monitor the implementation of the security architecture to get it to where it should be. [[ISACA](https://www.isaca.org/resources/isaca-journal/issues/2017/volume-4/enterprise-security-architecturea-top-down-approach)]

Some organisations do not have a properly defined information systems security architecture. In my opinion, the worst case that could result from this is similar to the following scenario:

<font color="purple">"They comply with multiple random standards and frameworks because that is what is needed to survive in the industry. The risk is not properly managed. Nothing is properly documented. Jobs are not well-defined. Thus, incapable people are all over the place. Capable and knowledgeable people are in a high-stress environment. Low-level employees never get a chance to come up and provide a better service. The decision-making process is highly political because what matters is existence, not security. In simple terms, the entire security team, including its services, is a mess."</font>

If this is not what an enterprise needs, it is always better to implement an acceptable information systems security architecture properly aligned to the enterprise architecture.

<br>

## Domain 10: Research Activities

Information systems security is a rapidly changing field. New technologies are constantly reaching the market. I strongly believe that “We are now stable, no need to change” or “if it works, do not change” mindsets will never succeed within information systems security. What is needed is to change along with the industry. 

Research is important when it comes to changing and upgrading. Within an enterprise, this could happen as separate projects or can be assigned to individuals. Some examples of research activities are as follows:
- Enterprise information systems security architecture upgrades such as adding new functions to the information systems security architecture.
- New exploitation methods.
- New threat intelligence methods.
- Use of new tools.
- Building new tools.

<br>

## Is that all?

Well, based on my opinion yes when it comes to domains. But there are deeper parts of Information Systems Security that I did not mention as separate domains. One example is Identity and Access Management (IAM). This requires a great amount of planning and always faces changes according to business needs. But I feel that this is connected to multiple domains and not a single domain. For example, the asset management domain classifies the systems, the infrastructure and application security domain implements the chosen IAM systems, and the security operations domain monitors the IAM systems. The rest of the parts are also connected with the other roles in the enterprise.
