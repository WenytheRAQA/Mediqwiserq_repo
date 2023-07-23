---
title: "To bring my existing software product/item onboard to IEC 62304"
categories:
  - General QMS
tags:
  - IEC 62304
  - SaMD
last_modified_at: 2023-07-23
---

Integrating legacy devices (or bringing in legacy devices) into a Quality Management System (QMS) has become essential in the dynamic field of medical devices. Regulatory standards are not static. They evolve to keep pace with technological advancements, ensuring healthcare safety and efficacy. 

One critical standard is the IEC 62304, a widely accepted guideline that defines life cycle requirements for developing medical software and software within medical devices. This blog post aims to share thoughts about using Section 4 of the IEC 62304 standard to integrate legacy medical devices into Quality Management Systems (QMS). Please note, clause 4 is applicable from a devices were not establishec in accordance with any version of IEC 62304, to the devices existing prior to 2015 revision and bring them on board.

Clause 4 includes the following steps

1. Risk management
2. Determine the Software Safety Classification of your device and determine the deliverables applicable
3. Justification and Maintenance.

Let's walk through them together!

## Risk Management

1. First of all, gather as much existing information as possible and start thinking about your claim/intended use of legacy software. No matter your legacy software is a software item of your product or the legacy software is the product itself, the claim is crucial for you to do the risk assessment.2. Perform risk assessment based on
2. Perform risk assessment based on
   <ol type="a">
   <li>the intended use of your legacy software (software item within a product or being the product itself),</li>
   <li>known feedback/post-production information, especially incident and near-incident events and known anomalies; and</li>
   <li>for integrating legacy software items, their positions and connections within the entire product's architecture</li>
   </ol>
3. Perform regular risk management against this legacy software item(s) and the impacts on the entire product as per ISO 14971 and IEC 62304 §7.1 & 7.2.
  - Reminder 1: these controls should be part of the requirements.
  - Reminder 2: check appendix C in your IEC 62304 guidance for the relationship between ISO 14971 and IEC 62304.

## Software Safety Classification and Gap Mitigations

1. Use your pre-mitigating risk assessment results and the existing external risk controls to determine your Software Safety Classification. It will also likely determine your [documentation level](https://wenytheraqa.github.io/fda/Final-FDA-guidance-on-Content-of-Premarket-Submissions-for-Device-Software-Functions/) if you plan to make a 510(k) submission.
2. Based on the determined Software Safety Classification A, B, or C, you can determine the deliverables you will need.
   - If you ready has some existing deliverables - review them and do a gap assement;
   - If you have some non-formalized requirements, architecture, or testing - do gap assessments and take the credits from them;
   - In any case, 
     - List your requirements and draw the architecture diagrams, then do the mapping to see if any unmet requirements need to be re-engineered;
     - List your requirements and your current testing, then do mapping to ensure the full coverage of your testing.
   - As stated in the guidance, the minimum deliverable should be your software system test records.
     - Reminder 3: If the legacy device is integrating into a system (but not the system itself), the details of the system testing should be based on your software safety classification of the **system**, not the legacy devices. The software safety classification of legacy devices depends on partitioning software items within your software system. Figure B.1 in IEC 62304 explains the concept well.

## Justification and Maintenance

Manufacturers should provide the justification why you determine legacy devices are still good to use. 

After all the deliverables are complete, no matter you newly create them or you review and deem the existing deliverables are acceptable, the following activities will be back to regular maintenance processes and activities.

## Additional Notes

Of course, QMS is way more than IEC 62304. There are also the implementations of ISO 13485 and ISO 14971 (fun stuff!) In addition, please definitely check [Principles and Practices for the Cybersecurity of Legacy Medical Devices](https://www.imdrf.org/consultations/principles-and-practices-cybersecurity-legacy-medical-devices) published by IMDRF. Cybersecurity is now vital and worth a designated post to talk about. 
