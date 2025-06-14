---
title: "Kudelski"
date: 2025-06-14
# draft: true
overview: true
# tags: ["test"]
weight: 10
---

# [Kudelski Group](https://www.nagra.com/): DevOps Engineer
* Cheseaux-sur-Lausanne, 1033 (VD)
* 2023 - Today
* Skills:
  * Extensive use of DevOps Tools: Terraform, Docker, Ansible, python/bash scripts, Gitlab / Azure DevOps pipelines
  * Multi-cloud / Saas solutions: AWS, Cloudflare and a bit of Azure (App registration / enterprise application, Azure Deveops)
  * Take over of abandonned projects / inventories
  * Data retrieval and analysis
  * PaloAlto Firewalls / Cisco routers and switches
  * Developement and consolidation of the inventories: Netbox, ServiceNow, Denodo
* Challenges:
  * Work with heterogeneous hardward and software version
  * Extra care to transfer the knowledge, especially to non-devops people.
  * Smooth transition from legacy to newer architecture/design
  * Avoid creating technical debts; favorize simple automations with great value



I worked on many projects, even some that were not managed by my team.  
I also asked to take over abandonned projects.  

As I displayed my capacity to just "make things work", I also inherited projects.


## Monitoring: Grafana-Prometheus Stack

## "AI"

I worked with LLM, CrewAI, Python, DuckDB, ... to make ...

## Domain Names

## Cloudflare

I was in charge of our Cloudflare accounts. I developed good reflexes regarding the Security aspects:
- WAF
- SSL
- ...
Our team also acted as a broker between Cloudflare and other teams.  

## [Denodo](https://www.denodo.com/en)

Denodo is an aggregation plateform that allowed us to take data from different sources, transform and combine them to finally expose them to different users. We could for example combine data from our IPAM inventory and results of internal scans.  

### My contributions
- Create, fix and simplified different views.  
  Using less obvious tools like `xpath`, I simplified most of our views.  
- I developed a custom extension to add many tools include some necessary for INET operations.  
  I also tested the performances impact to optimize our joins. Typically, customs functions should not be used in `JOIN` statements. 

## ServiceNow

We used ServiceNow to expose our services in the Catalog.  
This way, the rest of the company could easily ask us for standardized tasks.  

### My contributions
- Create and fix existing Catalog Items
- Added external automations that would pull from ServiceNow and/or push data to it.
- Developed Flow Tools for ServiceNow, like [Actions](https://developer.servicenow.com/dev.do#!/learn/courses/yokohama/app_store_learnv2_aescreateappfromscratch_yokohama_create_an_app_from_scratch_with_app_engine_studio/app_store_learnv2_aescreateappfromscratch_yokohama_automate_processes_with_flows/app_store_learnv2_aescreateappfromscratch_yokohama_actions)
- I integrated ServiceNow with Power Automate Platform

Of course, I was also a user and fullfiler of the platform.


## PKI (Public Key Infrastructure)

## Digicert: External PKI
## EJBCA: Internal PKI 

When I took over the PKI:
- There was no documentation
- We had no track of who asked for what, when and why.
- The configuration were wrong, for example:
  - nobody was receiving any notification
  - some operations were wrongly blocked by the WAF (because the mail template were using `${variable}` in templates, which looked like shell-injections)
  - we needed to manually extract the OID value and search on the ActiveDirectory to find the requester's email
- All the processes were done manually

I fixed all the configuration issues and documented all processes.  
I added features like ACME to allow automatic management of the certificates.  
This way:
- It was easier for user to ask for certificates
- Validation was delegated to the internal DNS
- Renewal was automatically managed
- All the internal traffic became encrypted and trusted