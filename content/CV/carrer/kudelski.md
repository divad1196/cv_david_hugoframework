---
title: "Nagra — Kudelski Group"
date: 2025-06-14
# draft: true
# overview: true
# weight: 10
---

# [Nagra — Kudelski Group](https://www.nagra.com/): DevOps Engineer

I joined the corporate IT team as the DevOps expert, simplifying and improving legacy services and adding new ones following state-of-the-art practices.  
My management skills led me to take on projects beyond my role.


## Example of Projects and Tasks


### AI integration

With the rise of AI, I was tasked with evaluating the complexity and benefits of its implementation. I worked primarily with CrewAI, Ollama, and Python on LLMs.

While LLMs are easy to extend and integrate, common use cases, such as corporate-specific responses, are already addressed by existing products.  
Implementing AI internally without creating a new product would have introduced unnecessary technical debt.

### Domain Names Inventory

We owned hundreds of domain names with no consolidated tracking. Previous attempts at inventory were outdated and scattered across multiple registrar platforms.

I assessed the situation and led a corporate-wide collection of information over several months to consolidate the inventory. I ensured that each domain had a clear owner and implemented notifications for ownership transfer when an owner departs.

The inventory now enables security scans and monitoring, ensures a known point of contact for faster issue resolution, allows periodic review to remove unused domains, and serves as a reliable source for automations.

It has also been extended to manage parked domains, ensuring proper records, hardening, and HTTP redirections, reducing workload for the CorpSec, Legal, and Marketing teams.


## Monitoring: Grafana-Prometheus Stack

## Netbox Inventory


## Cloudflare

...
Our team also acted as a broker between Cloudflare and other teams.  

## [Denodo](https://www.denodo.com/en) (Data Agregation Platform)

- Created, fixed, and simplified various views, using techniques like xpath to streamline complex queries.
- Developed a custom extension adding multiple tools, including ones essential for INET operations.
- Tested performance impacts to optimize joins, avoiding costly use of custom functions in JOIN statements.

## [ServiceNow](https://www.servicenow.com/uk/)
- Defined and refined existing catalog items.
- Used ServiceNow as the source of truth for automations.
- Developed Flow Tools, including [Actions](https://developer.servicenow.com/dev.do#!/learn/courses/yokohama/app_store_learnv2_aescreateappfromscratch_yokohama_create_an_app_from_scratch_with_app_engine_studio/app_store_learnv2_aescreateappfromscratch_yokohama_automate_processes_with_flows/app_store_learnv2_aescreateappfromscratch_yokohama_actions)
- Integrated ServiceNow with the Power Automate platform.
- Acted as a user and fulfiller of the platform, ensuring end-to-end understanding of workflows.


## PKI (Public Key Infrastructure)

## Digicert: External PKI

When I took over Digicert management, the process was largely manual, with no tracking or history, as all previous requests had been submitted via email.  
Requesters had to monitor certificate expirations themselves, which led to major outages when multiple certificates expired between my predecessor's departure and my takeover.
Digicert certificates are expensive, and my predecessor used a laborious workaround with wildcard and duplicate certificates to save costs, which further complicated management.

I identified that many requests did not actually require Digicert and could use, for example, Let's Encrypt instead.  
I enforced the use of the ACME protocol, presenting it to users as a self-provisioning, maintenance-free solution, and provided documentation and support to facilitate adoption.

## EJBCA: Internal PKI 

When I took over the PKI, there was no documentation, no tracking of requests, and many configuration issues:
- Notifications were not being sent.
- Some operations were blocked by the WAF due to mail templates using `${variable}`, which resembled shell injections.
- OID values had to be manually extracted and matched in Active Directory to identify requesters.
- All processes were performed manually.

I resolved the configuration issues and documented all processes. I also activated features such as ACME for automatic certificate management.

As a result:
- Requesting certificates became easier for users.
- Validation was delegated to the internal DNS.
- Certificate renewal was fully automated.
- All internal traffic became encrypted and trusted.