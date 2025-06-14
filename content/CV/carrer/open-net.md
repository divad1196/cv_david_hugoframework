---
title: "Open Net Sàrl"
date: 2023-05-29
# draft: true
overview: true
weight: 50
---

# [Open Net Sàrl](https://www.open-net.ch/)
* Worked on [Odoo](https://www.odoo.com/) ERP ("Enterprise resource planning"), a contestant of the famous [SAP](https://www.sap.com)
* From September 2018 to September 2023
* Odoo gold partner (when I worked there): [1st partner in Switzerland](https://www.odoo.com/fr_FR/partners/country/suisse-41), and [7th partner worldwide](https://www.odoo.com/fr_FR/partners?&country_all=True). They dropped 2nd in Switzerland and 22nd worldwide 2 years after my departure.

## Roles, responsibilities and attributions

Through hard and consistant work, I quickly gained a lot of roles in this company. 
- Lead Sysadmin: Stabilize, document, standardize and improve the infrastructure.
- Lead Developer: Evaluate and assign projects, Take over sensitive tasks, code reviews, candidate interview, new hired and apprentices onboarding. 
- Security Expert: 
- Project Manager:  
- Business Analyst (for some of our biggest customers)
- Logistic ERP Expert (Stock, Manufacturing, Repair, PLM, ...  )

With all these roles to manage in parallel, I got better at scheduling my priorities and taking decisions.

# The story in details


## 1. How I became SysAdmin

When I arrived in the company:
- there was almost a crash per week.
- There was no troubleshooting methodology, nor post mortems.  
- Anybody, regardless of their experience, would be assigned the task of fixing the issue.  
  This often resulted in a reboot of the customer instance which solved the issue only temporarily.
- There was no documentation nor procedure on how to deploy the the services, therefore all the instances were heterogenous.
- There was no monitoring, the management of the certificates was done manually.

I requested to be assigned to the troubleshooting whenever something happened and kept notes of the issues detected.  
This allowed to better identify the cause of the issues and quickly fix them.  
In a second time, I worked with a colleague on defining a proper infrastructure and installation procedure.
This included:
- Using Ansible for the configuration of customer instances
- GitOps deployment of the new features
- Simplified IaC to manage the reverse proxy and certificate generation (Certbot + LetsEncrypt)
- Monitoring using Zabbix
- Fixed and limited accesses the instances 
- Integrated a WAF on our infrastructure.
- ...

When the colleague I was working with left the company, I onboarded 2 other colleagues on the administration side to ensure the well continuity of the project.  

The last improvement was to move our infrastructure to the Cloud: The infrascture we had could not scale neither up (for new customers) nor down (if customers where to leave). Managing the hardware had a cost and accessing the datacenter would take at least 2 hours in case of an issue.  

I tested multiple solutions: AWS (EC2, Kubernetes), GCP, OVH (with Saas Proxmox to extend our cluster), Jelastic (with different structures), ...  
The main issue was generally the price. We also didn't have a need for complex tools like kubernetes.  
After many researches and comparison, I was able to find a Cloud that was even cheaper on average than what we were paying for our on-prem infrastructure.  

I defined a smooth migration plan for our 150 customers over 6 months. If we passed the 6 months deadline, we would be commited for another year of lease in the datacenter which would have costed a lot of money. Most of the procedure was automated using terraform and cloud-init scripts.  
All customers migration dates were scheduled and spaced them for safety.  

As we knew that I was leaving in a few months and couldn't do the migration myself, but also for the sake of properly transferring the knowledge,
I did the first few migration in front of my colleagues, then assigned the task to one of them and supervised him during his first few migrations.  
A few month after my departure, I got the confirmation from my colleague that everything went smoothly and on time takes to the detailed procedure and planification made.

## 2. Project Manager & Business Analyst

When I arrived, I started to work on the customer that would soon become our biggest customer. This customer had big needs on the logistic side, and I quickly realized that nobody was confortable with this topic in the company. I started to learn and practice on my side to better understand how the logistic work in Odoo and learned how different companies works (Make-to-stock, Make-to-order, FIFO vs LIFO, storable vs consumable, tracking, ...). Working on this customer helped me train my newly acquired knowledges.

This customer had people from different departments (Stock, Manufacturing, Marketing, Sales, Accounting, ...) and I would do a meeting once a week with them in an Agile manner to define the next steps of the project. Thanks to this, I developed the capacity to understand and conciliate the needs of multiple different people that, sometimes, don't want to make compromises.

Honestly, this was a huge risk to assign a customer to a new hired so fast. The same expirement happened with other new hired, this would sometimes work, but we lost many customer because of this.

I got assigned many other customers, either new customers with specific logistic needs, or existing customers unhappy with their current point of contact.
Many of these unhappy customers were about to leave the company but I was able to re-assure them and provide them with a good support.  
I never lost a customer.


### 3. Lead Developer Role: 

This happened by itself. As time passed, my colleagues would face some issue and ask others for help. The more I fixed their issues, the more I gained their trust. I had set up a [bookstack](https://www.bookstackapp.com/) instance and documented there things that they asked me. I was also completing more tickets and more complexe ones on top of that. I was also the only one that was doing a bachelor at this moment. I got assigned tasks like:
- Code review
- Project complexity evaluation
- Review of candidate resume (and their projects on github)
- Technical Interviews of the candiates
- Onboarding of new hired and apprentices
- Optimization of code (with a few tweaks, I made a script run from 3h to 15min)

All of that combined made me gain the title of lead developer very soon.  



### Security Engineer

As I was doing my roles of Sysadmin and Lead Developer, I sometimes discovered insecure code / configuration and fixed them.  
I was also doing a bachelor in Cybersecurity in parallel of my job.  

There was no clearly defined responsabilities. I was already reviewing the infrastructure and code with security in mind.  

This title was mostly useful to reassure the customers. Typically, some customers would just run a scanning tool like Tenable Nessus and would panic when they see a medium CVSS score that they don't understand.  
For example, at some point we were using NGINX 1.18 when the 1.21 was out for compatibility reason with modeSecurity V3.  The CVSS score reported 2 things:
- off-by-one on the resolver: requires that we use the resolver feature, which we were not using. It also required specific conditions for the exploit.
- module to optimize the streaming video: We didn't even have the module installed.

These customers sometimes paid external parties that didn't provide any explanation and were not granted any permission to scan our infrastructure.