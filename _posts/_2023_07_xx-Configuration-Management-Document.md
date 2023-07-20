---
title: "Waht are the Software Maintenance and Software Configuration Management in the IEC 62304"
categories:
  - General QMS
tags:
  - IEC 62304
  - SaMD
last_modified_at: 2023-07-xx
---

Just share notes and thoughts about the Software Maintenance and Software Configuration Management in IEC 62304 with you today (section 6 and 8 in 2015 version).

# Configuration Management

The "configuration management(CM)" is generic concept in ISO, IEC, and IEEE (or the [FDA Glossary](https://www.fda.gov/inspections-compliance-enforcement-and-criminal-investigations/inspection-guides/glossary-computer-system-software-development-terminology-895)). It is applicable for hardware, software, and for product and service. 

Tailor it for IEC 62304, in my language, it means *your controls over your listed software items*  That includes 
- identification both the itme level and the system level
- Change Control Processes (map with ISO 13485:2016, §7.3.9)
- Configuration status accounting, aka records of the history, including when and why --- to ensure only authorized modifications will go into the product(s).

## Deliverables:

### CM procedure

**Identifications**: describe the versioning system and the naming system:
- Versioning: Do you use major.minor.patch, major.minor.build.revion, or the year and date? And better to explain your definition of "major" and "minor."
  - Personally I prefer to have major and minor in the system, review the [FDA 510(k) software change guidnace](https://www.fda.gov/media/99785/download) or anything simliar from the regulatory authorities with the Engineering, and map the definition of "major" when we need to file a new submission.
- identifier: how do you name your software items
  - Please note, here the items including source code, object code, control code, control data, or a collection of these items.
  - you also can think about if you want to have an internal identifier for SOUPs and OTSs. You also can use its orignial names.
  - assets within the software will also be within the scope (e.g. any images, text...etc.)

**Change control**:

The process flow should be: 

```
Initiative a Chagne Request -> Approve Chagne Request -> Implement changes -> Verification -> Release.
```

Several points:
- I consider "change request" as a "plan" --- we document the scope and evaluate the impacts, and identify the applicable activities and tasks.
- I think that the term "implementation" in ISO 13485 is slightly different than IEC 62304 within this change control context. I believe this is due to the natural differece between standalong software and a general manufacturing: "implementation" in IEC 62304 §8.2.2, to me, is making change to the software configurable items prior to V&V. In ISO 13485:2016, §7.3.9, the implementation is when the design change has been approved and going to be transferred to the production.
- IEC 62304 §8.2.4 makes it clear that change request needs to serve traceability purposes: A Change request <-> a list of the product report (e.g. your bug tickets or open issues) <-> The approval that lists the changes on the configuration software items (§8.3).


### CM Plan (62304, §5.1.9)

| Requirements | Sections in your Plan | Notes |
| -------- | -------- | -------- |
| The classes, types, categories or lists of items to be controlled | Refer to your SOP/WI and specify where will you document this information (e.g., release note, SBOM...etc)  | For both system/product and all items involved |
| The configuration Management Activities and tasks | A table of applicable activities and the owners is recommended | See below Note 1 |
| The organization(s) responsible for performing software configuration management activities | This include storage, record keeping ...etc. | See below Note 1 |
| When the items are be placed under configuration control |  | |
| When the problem resolution process is to be used | |

**Note 1**: Several examles:
- Your configuration management includes OTS and SOUP items within your device(s). Based on the situation, you could download and store your own copies for your OTS/SOUP, or you could update the item lists when your vender update the version (e.g. the item is a Saas), or any other applicable manners.
- You may have different teams controlling different type of items (e.g., have a designated team for media controls, or technical writers for the IFU page...etc.)
- You may have an OEM for software development, and they are the one maintaining it
- You purhcased a customeized software component, and going to maintain it by yourself in the future. 


# Software Maintenance

# What do we need to do?

Actually, it is not really deviate from standard engineering practice (I hope).


