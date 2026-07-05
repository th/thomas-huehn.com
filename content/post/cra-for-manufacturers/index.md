---
title: "CRA for Manufacturers"
date: 2026-06-13T10:25:35+02:00
tags:
  - security
  - Cyber Resilience Act
description: "I have restructured and reordered the Cyber Resilience Act's requirements, in order to make them more practically manageable."
image: ""
aliases: []
draft: false
---
# Introduction

While the Cyber Resilience Act is rather readable for a legal instrument, it is structured in such a way that many requirements are duplicated, triplicated, or n-plicated across the Articles and their paragraphs. Just count how often you have to do a risk assessment, or fulfil the essential cybersecurity requirements.

I have decided to re-structure the requirements in such a way that the high-level topics get their own chapter, and the different parts of the Cyber Resilience Act requiring them are cited in one place. The idea is that the top-level headings provide an overview of what you actually need to do, a bit like a checklist. The requirements are stripped down to phrases (using [...] for omissions in quoted text). They should be intellegible on their own or in context of the preceding item. If necessary, I have added [context in brackets].

Additionally, I have broken up the paragraphs into the separate requirements. For example, Article 13 6. includes four requirements in two sentences: report vulnerabilities, remedy vulnerabilities, upstream the remedy, and use a machine-readable format.

Please note that while the Cyber Resilience Act repeatedly requires you to report something to ENISA and/or to the relevant CSIRT, in practice you're not going to be reporting to them directly by mail or post. Pursuant to Article 16, ENISA is building a [Single Reporting Platform](https://www.enisa.europa.eu/topics/product-security-and-certification/single-reporting-platform-srp) that shall be used for reporting, both to ENISA and CSIRT. The distinction the Cyber Resilience Act makes between the two is therefore moot for reporting purposes.

# Scope

This document collates manufacturers's obligations under the Cyber Resilience Act, ignoring requirements for EU member states, the EU Commission, Notified Bodies, or Open Source Stewards.

The requirements listed in here are a minimum set, assuming that the product in question belongs neither to the important, nor the critical class. Furthermore, high-risk AI systems are excluded. These requirements apply to software products, though.

## Exceptions

Neither spare parts for individual one-to-one replacement, nor exhibiting products in development at trade fairs fall under these requirements. Beta-testing software is allowed without fulfilling the Cyber Resilience Act at that time, but this exception only applied to software products, and only if the software product is not safety-related!

# Requirements

## Life-cycle
- designed, developed and produced in accordance with the essential cybersecurity requirements set out in Part I of Annex I (Article 13 1.)
- designed, developed and produced in such a way that they ensure an appropriate level of cybersecurity (Annex I Part I (1))
- made available on the market without known exploitable vulnerabilities (Annex I Part I (2) (a))
- apply effective and regular tests and reviews of the security of the product (Annex I Part II (3))

## Risk assessment
- undertake an assessment of the cybersecurity risks (Article 13 2.)
    - take the outcome of that assessment into account during the planning, design, development, production, delivery and maintenance phases ((Article 13 2.))
    - cybersecurity risk assessment shall be documented and updated as appropriate during a support period (Article 13 3.)
    - cybersecurity risk assessment shall indicate whether and, if so in what manner, the security requirements set out in Part I, point (2), of Annex I are applicable (Article 13 3.)
    - indicate how the manufacturer is to apply Part I, point (1), of Annex I and the vulnerability handling requirements set out in Part II of Annex I. (Article 13 3.)

## Product security
- secure by default configuration (Annex I Part I (2) (b))
    - unless otherwise agreed between manufacturer and business user in relation to a tailor-made product (Annex I Part I (2) (b))
- possibility to reset the product to its original state (Annex I Part I (2) (b))
- provide the possibility for users to securely and easily remove on a permanent basis all data and settings (Annex I Part I (2) (m))
- protection from unauthorised access by appropriate control mechanisms (Annex I Part I (2) (d))
    - report on possible unauthorised access (Annex I Part I (2) (d))
- protect the confidentiality of stored, transmitted or otherwise processed data (Annex I Part I (2) (e)) 
    - encrypting relevant data at rest or in transit by state of the art mechanisms	and by using other technical means (Annex I Part I (2) (e))
- protect the integrity of stored, transmitted or otherwise processed data, [...] commands, programs and configuration against any manipulation or modification not authorised by the user (Annex I Part I (2) (f))
    - report on corruptions (Annex I Part I (2) (f))
- process only data, personal or other, that are adequate, relevant and limited to what is necessary in relation to the intended purpose of the product (Annex I Part I (2) (g))
- protect the availability of essential and basic functions [...] against denial-of-service attacks (Annex I Part I (2) (h))
- minimise the negative impact by the products themselves or connected devices on the availability of services provided by other devices or networks (Annex I Part I (2) (i))
- designed, developed and produced to limit attack surfaces (Annex I Part I (2) (j))
- designed, developed and produced to reduce the impact of an incident using appropriate exploitation mitigation mechanisms and techniques (Annex I Part I (2) (k))
- provide security related information by recording and monitoring relevant internal activity (Annex I Part I (2) (l))
    - including the access to or modification of data, services or functions (Annex I Part I (2) (l))
	- opt-out mechanism for the user (Annex I Part I (2) (l))

## Third party components
- exercise due diligence when integrating components sourced from third parties (Article 13 5.)
- vulnerabilities of that product, including its components, are handled effectively (Article 13 8.)
- identify and document components (Annex I Part II (1))
- drawing up a software bill of materials (Annex I Part II (1))
    - in a commonly used and machine-readable format (Annex I Part II (1))
    - covering at the very least the top-level dependencies of the products (Annex I Part II (1))
- format and elements of the software bill of materials (Article 13 24.)
- market surveillance authorities may request manufacturers of such categories of products with digital elements to provide the relevant software bills of materials ((Article 13 25.))
- [sharing of information about potential vulnerabilities] in third-party components contained in that product (Annex I Part II (6))

## Vulnerability management
- identify and document vulnerabilities (Annex I Part II (1))
- report the vulnerability to the person or entity manufacturing or maintaining the component (Article 13 6.)
- remediate the vulnerability (Article 13 6., Annex I Part II (2))
    - providing security updates (Annex I Part II (2))
- share the relevant code or documentation with the person or entity manufacturing or maintaining the component (Article 13 6.)
    - where appropriate in a machine-readable format (Article 13 6.)
- vulnerabilities of that product, including its components, are handled effectively (Article 13 8.)
- appropriate policies and procedures, including coordinated vulnerability disclosure policies [...] to process and remediate potential vulnerabilities (Article 13 8.)
- take the corrective measures necessary to bring that product with digital elements or the manufacturer’s processes into conformity (Article 13 21.)
    - or to withdraw or recall the product (Article 13 21.)
- put in place and enforce a policy on coordinated vulnerability disclosure (Annex I Part II (5))
- facilitate the sharing of information about potential vulnerabilities in their product (Annex I Part II (6))
	- providing a contact address for the reporting of the vulnerabilities  (Annex I Part II (6))

### Actively exploited vulnerability
- notify any actively exploited vulnerability [...] to the CSIRT (Article 14 1.)
    - via the single reporting platform (Article 14 1., Article 14 7.)
        - submitted using the electronic notification end-point of the CSIRT designated as coordinator of the Member State where the manufacturers have their main establishment in the Union (Article 14 7.)
    - early warning notification of an actively exploited vulnerability (Article 14 2. (a))
        - without undue delay and in any event within 24 hours (Article 14 2. (a))
    - vulnerability notification (Article 14 2. (b))
        - without undue delay and in any event within 72 hours (Article 14 2. (b))
        - provide general information [...] about the product (Article 14 2. (b))
        - general nature of the exploit and of the vulnerability (Article 14 2. (b))
        - corrective or mitigating measures taken (Article 14 2. (b))
		- corrective or mitigating measures that users can take (Article 14 2. (b))
		- indicate, where applicable, how sensitive the manufacturer considers the notified information to be (Article 14 2. (b))
    - final report (Article 14 2. (c))
        - no later than 14 days after a corrective or mitigating measure is available (Article 14 2. (c))
        - description of the vulnerability, including its severity and impact (Article 14 2. (c) (i))
        - information concerning any malicious actor that has exploited or that is exploiting (Article 14 2. (c) (ii))
        - details about the security update or other corrective measures (Article 14 2. (c) (iii))
- provide an intermediate report on relevant status updates (Article 14 6.)

### Severe incident
- [Definition of "severe"] (Article 14 5.)
- notify any severe incident [...] to ENISA (Article 14 3.)
    - via the single reporting platform (Article 14 3., Article 14 7.)
        - submitted using the electronic notification end-point of the CSIRT designated as coordinator of the Member State where the manufacturers have their main establishment in the Union (Article 14 7.)
    - early warning notification of a severe incident (Article 14 4. (a))
        - without undue delay and in any event within 24 hours (Article 14 4. (a))
        - whether the incident is suspected of being caused by unlawful or malicious act (Article 14 4. (a))
		- indicate, where applicable, the Member States on the territory of which the manufacturer is aware that their product with digital elements has been made available (Article 14 4. (a))
    - incident notification (Article 14 4. (b))
        - without undue delay and in any event within 72 hours (Article 14 4. (b))
		- provide general information, where available, about the nature of the incident (Article 14 4. (b))
		- initial assessment of the incident (Article 14 4. (b))
		- corrective or mitigating measures taken (Article 14 4. (b))
		- corrective or mitigating measures that users can take (Article 14 4. (b))
		- indicate, where applicable, how sensitive the manufacturer considers the notified information to be (Article 14 4. (b))
    - final report (Article 14 4. (c))
        - within one month (Article 14 4. (c))
        - detailed description of the incident, including its severity and impact (Article 14 4. (c) (i))
        - type of threat or root cause (Article 14 4. (c) (ii))
        - applied and ongoing mitigation measures (Article 14 4. (c) (iii))
- provide an intermediate report on relevant status updates (Article 14 6.)

## Security updates
- security updates (Annex I Part I (2) (c), Annex I Part II (2))
    - in an automatic manner (Annex I Part II (7))
    - automatic security updates that are installed within an appropriate timeframe (Annex I Part I (2) (c))
        - default setting, with a clear and easy-to-use opt-out mechanism (Annex I Part I (2) (c))
    - notification of available updates to users (Annex I Part I (2) (c))
    - option to temporarily postpone them (Annex I Part I (2) (c))
    - new security updates shall be provided separately from functionality updates (Annex I Part II (2))
    - mechanisms to securely distribute updates (Annex I Part II (7))
    - where security updates are available to address identified security issues, they are disseminated without delay (Annex I Part II (8))
    - free of charge (Annex I Part II (8))
    - accompanied by advisory messages providing users with the relevant information (Annex I Part II (8))
        - including on potential action to be taken (Annex I Part II (8))
- once a security update has been made available, share and publicly disclose information about fixed vulnerabilities (Annex I Part II (4))
    - description of the vulnerabilities (Annex I Part II (4))
    - information allowing users to identify the product with digital elements affected (Annex I Part II (4))
	- the impacts of the vulnerabilities (Annex I Part II (4))
	- their severity (Annex I Part II (4))
	- clear and accessible information helping users to remediate the vulnerabilities (Annex I Part II (4))

## Technical documentation
- draw up the technical documentation (Article 13 12.)
- general description (Annex VII 1.)
    - intended purpose (Annex VII 1. (a))
    - versions of software affecting compliance with essential cybersecurity requirements (Annex VII 1. (b))
    - (hardware) photographs or illustrations showing external features, marking and internal layout (Annex VII 1. (c))
    - user information and instructions as set out in Annex II (Annex VII 1. (d))
- description of the design, development and production of the product (Annex VII 2.)
    - necessary information on the design and development of the product
	- drawings and schemes (Annex VII 2. (a))
	- description of the system architecture (Annex VII 2. (a))
	- how software components build on or feed into each other and integrate into the overall processing (Annex VII 2. (a))
- vulnerability handling processes (Annex VII 2.)
    - information and specifications of the vulnerability handling processes put in place by the manufacturer (Annex VII 2. (b))
	- software bill of materials (Annex VII 2. (b))
	- coordinated vulnerability disclosure policy (Annex VII 2. (b))
	- evidence of the provision of a contact address for the reporting of the vulnerabilities (Annex VII 2. (b))
	- description of the technical solutions chosen for the secure distribution of updates (Annex VII 2. (b))
- information and specifications of the production and monitoring processes of the product (Annex VII 2. (c))
    - validation of those processes (Annex VII 2. (c))
- include the cybersecurity risk assessment (Article 13 4., Annex VII 3.)
    - including how the essential cybersecurity requirements set out in Part I of Annex I are applicable (Annex VII 3.)
- document [...] relevant cybersecurity aspects concerning the products with digital elements including vulnerabilities of which they become aware (Article 13 7.)
- include the information that was taken into account to determine the support period of a product with digital elements in the technical documentation (Article 13 8.)
- copy of the EU declaration of conformity (Annex VII 7.)
- keep the technical documentation and the EU declaration of conformity at the disposal of the market surveillance authorities for at least 10 years (Article 13 13.)
- relevant information that was taken into account to determine the support period (Annex VII 4.)
- list of the harmonised standards applied in full or in part the references of which have been published in the Official Journal of the European Union (Annex VII 5.)
- common specifications as set out in Article 27 of this Regulation or European cybersecurity certification schemes (Annex VII 5.)
- where those harmonised standards, common specifications or European cybersecurity certification schemes have not been applied, descriptions of the solutions adopted to meet the essential cybersecurity requirements set out in Parts I and II of Annex I (Annex VII 5.)
- list of other relevant technical specifications applied (Annex VII 5.)
- In the event of partly applied harmonised standards, common specifications or European cybersecurity certification schemes, the technical documentation shall specify the parts which have been applied (Annex VII 5.)
- reports of the tests carried out to verify the conformity of the product (Annex VII 6.)
reports [...] of the vulnerability handling processes (Annex VII 6.)
- software bill of materials (Annex VII 8.)

## User communication
- Manufacturers may maintain public software archives enhancing user access to historical versions. In those cases, users shall be clearly informed in an easily accessible manner about risks associated with using unsupported software. (Article 13 11.)
- [type, batch or serial number] is provided on their packaging or in a document accompanying the product (Article 13 15.)
- indicate the name, registered trade name or registered trademark of the manufacturer, and the postal address, email address or other digital contact details, as well as, where applicable, the website (Article 13 16.)
    -  also be included in the information and instructions to the user in a language which can be easily understood by users and market surveillance authorities (Article 13 16.)
- designate a single point of contact to enable users to communicate directly and rapidly with them (Article 13 17.)
    - single point of contact is easily identifiable by the users (Article 13 17.)
    - include the single point of contact in the information and instructions to the user (Article 13 17.)
- accompanied by the information and instructions to the user (Article 13 18.)
- in a language which can be easily understood by users and market surveillance authorities (Article 13 18.)
- clear, understandable, intelligible and legible (Article 13 18.)
- allow for the secure installation, operation and use of products (Article 13 18.)
- [end date of the support period]
    - packaging or by digital means (Article 13 19.)
    - display a notification to users informing them that their product with digital elements has reached the end of its support period (Article 13 19.)
- provide a copy of the EU declaration of conformity or a simplified EU declaration of conformity (Article 13 20.)
    - contain the exact internet address at which the full EU declaration of conformity can be accessed (Article 13 20.)
- by any means available and to the extent possible, the users of the relevant products [cessation of operations] (Article 13 23.)
- [actively exploited or severe incident] inform the impacted users (Article 14 8.)
    - where appropriate all users (Article 14 8.)
    - of any risk mitigation and corrective measures that the users can deploy to mitigate the impact of that vulnerability or incident (Article 14 8.)
    - where appropriate in a structured, machine-readable format that is easily automatically processable (Article 14 8.)
- notification of available updates to users (Annex I Part I (2) (c))
- once a security update has been made available, share and publicly disclose information about fixed vulnerabilities (Annex I Part II (4))
    - description of the vulnerabilities (Annex I Part II (4))
    - information allowing users to identify the product with digital elements affected (Annex I Part II (4))
	- the impacts of the vulnerabilities (Annex I Part II (4))
	- their severity (Annex I Part II (4))
	- clear and accessible information helping users to remediate the vulnerabilities (Annex I Part II (4))
- [security updates] accompanied by advisory messages providing users with the relevant information (Annex I Part II (8))
    - including on potential action to be taken (Annex I Part II (8))

### Information and instructions to the user
- name, registered trade name or registered trademark (Annex II 1.)
- postal address (Annex II 1.)
- email address (Annex II 1.)
- website (Annex II 1.)
- single point of contact where information about vulnerabilities of the product with digital elements can be reported and received (Annex II 2.)
- providing a contact address for the reporting of the vulnerabilities  (Annex I Part II (6))
- where the manufacturer’s policy on coordinated vulnerability disclosure can be found (Annex II 2.)
- name and type and any additional information enabling the unique identification of the product (Annex II 3.)
- intended purpose of the product (Annex II 4.)
- security environment provided by the manufacturer (Annex II 4.)
- essential functionalities (Annex II 4.)
- information about the security properties (Annex II 4.)
- known or foreseeable circumstance, [...] in accordance with its intended purpose [...] which may lead to significant cybersecurity risks (Annex II 5.)
    - or under conditions of reasonably foreseeable misuse (Annex II 5.)
- internet address at which the EU declaration of conformity can be accessed (Annex II 6.)
- type of technical security support offered by the manufacturer (Annex II 7.)
- end-date of the support period during which users can expect vulnerabilities to be handled and to receive security updates (Annex II 7.)
- detailed instructions or an internet address (Annex II 8.)
    - necessary measures during initial commissioning and throughout the lifetime of the product [...] to ensure its secure use (Annex II 8. (a))
    - how changes to the product with digital elements can affect the security of data (Annex II 8. (b))
    - how security-relevant updates can be installed (Annex II 8. (c))
    - secure decommissioning of the product with digital elements (Annex II 8. (d))
        - including information on how user data can be securely removed (Annex II 8. (d))
    - how the default setting enabling the automatic installation of security updates [...] can be turned off (Annex II 8. (e))
    - information necessary for the integrator to comply with the essential cybersecurity requirements (Annex II 8. (f))
- If the manufacturer decides to make available the software bill of materials to the user, information on where the software bill of materials can be accessed (Annex II 9.)
- keep the information and instructions to the user set out in Annex II at the disposal of users and market surveillance authorities for at least 10 years (Article 13 18.)
- manufacturers shall ensure that [information and instructions to the user] are accessible, user-friendly and available online (Article 13 18.)

## Support period
- cybersecurity risk assessment shall be documented and updated as appropriate during a support period (Article 13 3.)
- determine the support period (Article 13 8.)
- each security update [...] which has been made available to users during the support period, remains available after it has been issued for a minimum of 10 years or for the remainder of the support period, whichever is longer. (Article 13 9.)
- users of the versions that were previously placed on the market have access to the version last placed on the market free of charge (Article 13 10.)
- end date of the support period [...] is clearly and understandably specified (Article 13 19.)
    - at least the month and the year (Article 13 19.)
	- at the time of purchase (Article 13 19.)
	- in an easily accessible manner (Article 13 19.)
- end-date of the support period during which users can expect vulnerabilities to be handled and to receive security updates (Annex II 7.)

## Conformity
- carry out the chosen conformity assessment procedures (Article 13 12.)
- draw up the EU declaration of conformity (Article 13 12.)
- affix the CE marking (Article 13 12.)
- keep the technical documentation and the EU declaration of conformity at the disposal of the market surveillance authorities for at least 10 years (Article 13 13.)
- procedures are in place for products [...] to remain in conformity (Article 13 14.)
    - take into account changes in the development and production process or in the design or characteristics of the product [...] and changes in the harmonised standards (Article 13 14.)
- bear a type, batch or serial number (Article 13 15.)
- take the corrective measures necessary to bring that product with digital elements or the manufacturer’s processes into conformity (Article 13 21.)
    - or to withdraw or recall the product (Article 13 21.)
- provide that authority, in a language which can be easily understood by that authority [...], in paper or electronic form, necessary to demonstrate the conformity of the product (Article 13 22.)
    - with all the information and documentation (Article 13 22.)
    - in a language which can be easily understood by users and market surveillance authorities (Article 13 18.)
- and of the processes put in place (Article 13 22.)
cooperate with that authority, at its request, on any measures taken to eliminate the cybersecurity risks (Article 13 22.)
- inform, before the cessation of operations takes effect, the relevant market surveillance authorities (Article 13 23.)

