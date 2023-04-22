---
title: "Odoo"
date: 2023-04-22
# draft: true
overview: true
weight: 40
---

# [Odoo](https://www.odoo.com/)
I work on Odoo since 2018.
Odoo is a new generation ERP, aka "Enterprise resource planning".
It positions itself as a contestant of the famous [SAP](https://www.sap.com), leader in this field.

You will find my opinion on Odoo here

## Open Source
Odoo community edition is **Open Source**, this means anyone can read the code [here](https://github.com/odoo/odoo).
Nb: The code for the enterprise edition is also open source but you need to have an enterprise license to gain access.

Why is that important?
* Odoo Community is also a free software, meaning anyone can install and use this version.
* You can benefit from the [OCA ("Odoo Community Association")](https://github.com/OCA) which develops many extensions to the framework.

### Open Source vs Security
From a security perspective, security researcher tend to disagree wheter it is a good or bad practice to have Open Source code.
Hiding the code is called "blackbox security", you make it more difficult for hackers to find an exploit.
I personnaly disagree:
* There are powerful tools that a malicious person can use to find exploits
* Even without reading the code, there are ways to find exploits.
* Once an exploit is found by a malicious person, it can take months before it is discovered and fixed.
* Only ethical hackers/security research won't be able to help without obtaining special permissions.
Having the code Open Source make it easier for everyone to read and contribute.
You are more likely to have helpful feedback than attacks.

## Prices
* Odoo community is totally free, but free can be expensive: having someone to maintain and migrate your Odoo, loosing your data because of a mistake, having bad processes/configuration of your Odoo because you never got a formation on the tool,... all of this cost money.  
  If you want to use Odoo community, I still recommend having a formation made by an official integrator.
* Odoo enterprise requires a paid license, but:
  * The price is quite affordable
  * You have support and migration from Odoo SA
  * You benefit from more modules maintained by Odoo (which is, from my point of view, the least intersting privilege)

## End-Users usage
I honestly think that, for end-users, Odoo is a great tool:
* It is modular, you can activate any module just with one single click.  
  Therefore, you won't be as cluttered as other solutions
* Functional fields are quiet well integrated and will suit most of your needs out of the box.
* There are many tutorials, documentations and forums to help you
* Odoo can be customized easily, it even provides its own tool called "Odoo Studio" which allows you to customize your ERP.  
  
  
### Odoo Studio: Not recommended (personal opinion)
I personnaly discourage the use of this tool, at least for the moment:
* You can never just "remove" something you made, it will hide it, which has a big performance downside
* You can break your Odoo: this has been improved a lot, but this is still possible break something.
We had a client that required 7min to open a mere page because of an error he did with this tool.
* Depending the change you make, some module won't be able to be installed anymore.
* If once you need to have some more complexe modifications requiring a developper to make it, it will make the developpement a lot harder and certainly increase the total cost of the development.


## Development
It is the easiest framework I have ever used, even more than Ruby-on-rails, we can easily create new models/fields/view/custom search filters/reports/.... in minutes!
What's hard is knowing the whole Odoo ecosystems and functional needs.
The framework is not the fastest (if compared with Django, FastAPI or ROR) but it is fast enough and is becoming faster through the versions.
The security layer is also integrated into the framework. This prevents from mistakes that would cause security issues and spares a lot of time.

They are also making their source code more hookable which simplifies how the software can be extended.


## My modules
I have developped and publish some modules through time, but most of them are not maintained.

* [odoo_graphql](https://github.com/divad1196/odoo_graphql): Add a generic graphql API to Odoo. Graphql is a good to retrieve data, this module can be useful when an external system needs to retrieve data from Odoo. You can find it on [the odoo app store](https://apps.odoo.com/apps/modules/16.0/odoo_graphql/)

