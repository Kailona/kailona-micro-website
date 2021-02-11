---
layout: project
title:  "Kailona Personal Health Records"
image: /assets/images/project_images/kailona/header.png
authors:
    - author: Kailona
      link: https://kailona.org
brief: "We give humans control over their health data."
summary: The dignity of humans is violable by uncontrolled access to health data. Kailona gives back control over health data. Our prototype allows developers to extend the base platform with custom health data
---

## Devoid of Dignity

No one chooses to get sick and no one should be discriminated for physical or mental health issues. Yet, personal health data is being exploited and used to discriminate against people, devastating their ability to find jobs, insurance coverage and economic stability. Right now, governments, device makers, and software companies are handing out your health data for corporations to exploit. Currently, there is a new wave of apps marketing secure personal health records, but their revenue models are based on selling the data to insurance and pharmaceutical companies and users are not made explicitly aware of the consequences of using these apps.

## Owning Data

Kailona provides open source health information technology to protect people from data exploitation, give them control over their health data, and improve the health of individuals and societies. Privacy is not a black and white phenomena, but rather has many shades of color. A dignified approach to health data means allowing people to make educated choices about which level of privacy they are comfortable with. At the most basic level, data can be protected by using end-to-end encryption, which locks the data with a private key before it is transmitted over the internet. At this level, adversaries are limited to extracting metadata, which provides information about who is exchanging data with whom. For the most part, the data itself is fairly well protected for the time being. At an interim level, metadata extraction can be limited by using Virtual Private Networks (VPN) or Tor browsers that obscure the information about the senders and receivers. At the highest level, open source operating systems, such as Linux, can prevent the extraction of decrypted data in the local browser storage. Furthermore, open source hardware can prevent  backdoor access to decrypted data. 

In most countries, it is mandatory for the healthcare providers to give the patient all their health records within a certain time frame. Unfortunately, many providers do not comply with these requirements and even if they do, they provide incomplete data on printed documents, CDs and DVDs. Very often patient medical data is transmitted in a fashion that compromises privacy, such as sending health reports through email. New legislation in Germany requires providers to share all health data in digital format with the patient. (Seit 1. Januar 2021 müssen die gesetzlichen Krankenkassen und Krankenhäuser den Patienten eine elektronische Patientenakte (ePA) anbieten. Ab 1. Juli 2021 sind Arztpraxen verpflichtet, mit ihren Systemen den Zugriff auf die ePA zu ermöglichen) Kailona provides a mechanism for patients to request their health records and keep track of compliance with the legislative requirements of the providers. The goal is for the Kailona users to always have the most complete health record and have absolute ownership and control over the data.

![Screencast: Data Request](/assets/images/project_images/kailona/data-request.gif)

## Changing behavior

Industrial medicine is proficient at diagnosing illness, but it does not fulfill its promises when it comes to healing people. Right now, the medical industry sequences genomes, gathers billions of data points, and generates countless medical images, but it does not have a way to translate this proliferation of data into  innovations that heal. Physical activity, nutritional data, mental and emotional data are the critical missing pieces.

At the most basic level, everyone knows that they need to exercise more, eat healthier food, get quality sleep, and consume less alcohol. However, people rarely change just because they know they should or are told to do so. Instead, when people experience for themselves the connection between physical activity, nutrition and well-being, they are likely to maintain positive behavioral changes. And with these sustained and healthier behaviors, the human body has an incredible potential for self-healing.

Kailona allows people to systematically manage activity, sleep, weight, nutrition, supplements, vital signs, lab results, medical images, pharmaceutical, genomic data and data about the mental and emotional states. Visualization tools allow people to understand the relationships between the data and encourage them to make healthier choices. Kailona is an opportunity for people to discover paths towards self-healing. 

![Screencast: Timeline](/assets/images/project_images/kailona/timeline.gif)

![Screencast: Import TCX](/assets/images/project_images/kailona/import-tcx.gif)

## Sharing data

Kailona enables people to securely share their health data, whether it be with their inner circle of friends and family or as an anonymous participant in research endeavors. This empowers people to leverage their own data to benefit themselves, their communities, and societies at large.
By sharing an anonymized version of health data with the research community, people accelerate innovation in diagnosis and treatment. Furthermore, many patients find strength when they know that they are not alone in their diagnoses, but rather that they are a part of a larger community of patients and passionate researchers searching for effective treatments. Sharing an anonymized version of one’s health data allows researchers to make faster progress with effective treatments. Kailona also opens the possibility to connect with other patients and find support at whatever level of anonymity feels comfortable.

There are several levels of anonymization. On one end of the spectrum is re-identifiable data. On the other end of the spectrum is completely anonymized data, such as synthetic data that consists of simulated data not based on any real-word individuals or events. Creating synthetic data is particularly important in preventing re-identification of complex data, including medical images and DNA sequences.

At this point, the Kailona app only provides basic sharing features among patients, providers and family members, but the Kailona team is working on partnerships with some of the leaders in synthetic data.

## System Architecture

When building privacy solutions, the technical challenges of keeping the solution continuously secure are immense. In order for us to deliver a robust privacy solution in a short time frame, the Kailona team decided to first build on top of the open source project, Nextcloud. With it’s end-to end encryption, Nexcloud is compliant with the Health Insurance Portability and Accountability Act (HIPAA) and General Data Protection Regulation (GDPR), provides credential management, and, last but not least, has a large community of users that understands the importance of privacy and data ownership. Kailona provides the flexible client source code under the MIT open source license. A modular software architecture allows anyone to add plugins of their interest to the application. All health data is stored in Health Level 7 (HL7) Fast Healthcare Interoperability Resources (FHIR) standard, which makes data exchange as open and flexible as possible.

![Image: System Architecture](/assets/images/project_images/kailona/architecture.svg)

## Learnings from the prototype project 

Communicating the relevance of health privacy and health data ownership to the general public has been the most challenging part of the project. For many people, the problem we are solving is still too abstract and not yet a priority. As a solution to the communication challenge, we have identified three types of early adopters:

- people and their guardians seeking or facing a new diagnosis

- people interested in optimizing their body performance (sleep performance, blood pressure, sports, etc.)

- people who are migrating because they are dislocated from their homes, language and care providers, will thus greatly benefit from a continuity of health records and care

From a technical perspective, scrum planning with small sprints based on continuous integration (CI)  and continuous deployment (CD) is essential. This is critical for team alignment, quality control and  allowing non-technical team members, such as designers and social scientists, to give early feedback during the development process.

## Releases

Nextcloud users can setup a FHIR server and enable the Kailona Nextcloud app from the Nextcloud App Store. Refer to our developer docs for the deployment instructions.

https://apps.nextcloud.com/apps/ehr

For those that cannot or choose not to install a Nextcloud server, we are installing an instance of the Kailona app on AWS and we will continuously update it. Please note that the Kailona app is currently in alpha stage.

https://app.kailona.org

We also provide the following websites for documentation, community discussions and marketing.

https://docs.kailona.org

https://help.kailona.org

https://kailona.org

## Next steps

Kailona will continue to add new features and plugins to the platform. We are planning a series of communication campaigns with Nextcloud and independent Nextcloud hosting providers. We will contact the device makers, such as bio vital trackers, and encourage them to write Kailona plugins. We have started to reach out to our contacts in Governments and the United Nations High Commissioner for Refugees (UNHCR) to roll out Kailona as the preferred health records solution for displaced people.

## About

Kailona ("kailo-" Proto-Indo-European for "whole, uninjured, of good omen") provides a global open-source platform for developers that allows individuals to make healthier choices and the research and developer community to accelerate health innovation.

We are an international team of designers, sociologists, anthropologists, and engineers passionate about the dignity, self-determination, trust and healing of people all over the globe.

The Kailona team is proud to be sponsored by the Prototype Fund, a project of the Open Knowledge Foundation Germany, funded by the Federal Ministry of Education and Research (BMBF) Förderkennzeichen 01|S20S38, MEDKEN, ACANIO and TOCA.
