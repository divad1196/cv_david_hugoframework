---
title: "Skills"
date: 2023-05-29
# draft: true
overview: true
# tags: ["test"]
weight: 30
---

# Skills


## Languages
1. **French**: Mother tongue
2. **English**: B2 Cambridge certified (~C1 estimated, not certified)
3. **German**: B1 certified (~B2 estimated, not certified). I would need a few days to get back on track.
4. **Italian**: ~A2
5. **Portuguese**: Notions (A1 at most, able to understand easy speeches)
6. **Japanese**: Notions (N5 at most, still learning)



## Cybersecurity Engineer

My CS Bachelor degree is about security. The skills I got and trained are:
* Security risks awareness: What is dangerous and why
* Security mitigation: How to prevent/fix such risks
* Software/Malware/Cryptographic Analysis. Tools: Ghidra, Volatility, gdb, pwntools...
* Attacks
  * On algorithm weakness (e.g. mode of operation for ciphers)
  * On wireless network (e.g. sniffing, trame injections, ...). Tools: wireshark, scapy, nmap, ...
  * High/Low level programming attacks (e.g. various kind of injections like SQL injection or XSS/CSRF, buffer overflows, weak OAuth flows, ...)
  * Side channel and fault attacks
  * Various attacks using Metasploit and python scripting
* Defenses
  * High/Low level programming (Good practices and algorithms, input sanitization, ...)
  * Network: firewall, WAF, Snort
  * Cryptography: Symetric and Asymetric Signatures(Simple, multi-sig and threshold)/Encryption(operating modes, authenticated cipher)/hash(cryptographically safe vs unsafe), SSL/TLS, ...

A complete audit of a company was also part of the formation.  
It is worth mentioning that, even though the knowledge required are linked, we did more attacks than defenses.  
Nb: We did learn a lot, but these skills need to be sharpened with the experience.  

## Software Engineer
* Good logic and understanding of various DSA and IT concepts
* Knowledge of many design patterns and paradigms. I can easily compare many solutions.
* Easily adapt to the language idiomatic ways of programming which makes better code (performance, readability and maintenance)
* Ability to forecast and plan the implementation.

The following chart shows my own programming language skill evaluation.

<!-- {{< chart data=charts.example >}} -->
{{<barChart data=charts.skills >}}

Some more details below
### 1. Python &#x1F5F2;
* Started to learn in 2018 and used daily: work (Odoo) and hobbies
* Frameworks & libraries:
  * **Web**: Fastapi, Flask, Django, Odoo
  * **ORM**: SQLAlchemy, PonyOrm, Odoo
  * **Data**: Pandas, numpy
  * **Interface**: Tkinter, pygame
  * **Scripting/Scrapping**: lxml, json, requests, Pillow, ... 
  * ...
  
  I am trying to get better statistical skills and learn to create my own ML models (pytorch)

### 2. C/C++
* Started to learn in 2016
* Used regularly at school and occasionally on small personal projects
* Implementation of custom-made Data structures and algorithms at need for performance.
  Now, I usually prefer to use Rust when possible
* Frameworks & libraries:
  * **Interface/Graphism**: [SFML](https://www.sfml-dev.org/), QT (Did a harmonic movement simulator)
  * **Web**: CrowCpp, Pistache.io
  * **Math**: Eigen
  * **Misc**: Boost, [nlohmann/json](https://github.com/nlohmann/json), ...
  * ...


### 3. Rust &#x2665;
* Started to learn at the beginning of 2022 by myself and got a course later on it during in my formation
* My current favorite language.  
  Its syntax, its powerful macros, its project management and its good design and good usage of functional programming concepts, security concerns ... are unmatched
* Frameworks & libraries:
  * **Web**: Rocket, Axum & Actix
  * **Concurrency**: Rayon, Tokyo
  * **Serialization**: Serde (what else ?)
  * **ORM**: Diesel
  * **Permissions**: Casbin
  * **CLI**: clap  

  and the list keeps growing!

### 4. Javascript (& Web)
* Started to learn in 2018
* Mostly frontends: Vuejs, ReactJS, AlpineJs, HTMX, Jquery, [OWL](https://github.com/odoo/owl), CSS/SCSS, bootstrap.  
  Nb: I don't have a graphical skill, meaning I am usually not the one creating the design.
* Also did some projects on: algorithms implementations, rendering, scrapping (puppeteer), ML (Tensorflow for hand gesture recognition) and WebRTC/streaming

### 5. Java
* Started to learn in 2019
* 
* Mostly did:
  * Data structure and algorithms implementations
  * Interface (Swing)
  * Web (Springboot)

### 6. Go
* Started to learn in 2019
* Mostly did:
  * Microservices (e.g. proxy to transform requests)
  * Terraform provider

### 7. Bash
* Started to learn in 2018
* Mostly did:
  * I extensively use the terminal. 
    Using bash allow me to test and reproduce my workflows.
  * One-shot scripts
  * CI scripts (often in combination with [Makefile](https://www.gnu.org/software/make/manual/make.html) and [Phony targets](https://www.gnu.org/software/make/manual/html_node/Phony-Targets.html))

### 8. SQL
I am comfortable with the old standard and the Postgres' flavor, but since I saw [modern SQL](https://modern-sql.com/), I think I have some more to learn before being statisfied with my level.

### 9. Kotlin
Learned the basics of how to create a native android app.

<!-- # Python
test
[python]({{< ref "skills" >}} "See python") -->


## System administrator (Linux)

* **Reverse Proxy**: Nginx, Traefik
* **Containers/virtualization**: Docker, Podman, Kubernetes, OpenStack, Jelastic
* **Management**: Ansible, Fabrik, Terraform (+ Terragrunt), Vagrant
* **Network**: iptables, nftables, snort
* **Monitoring**: Zabbix, Grafana Dashboard, fluentd
* **Benchmark**: Apache Jmeter

## Cryptography (Signatures, Challenges, encryptions, ...)

I have a good understanding of cryptographical concepts.  
Among them, I have worked a lot with certificates (public and internal).

I know how self-signed certificates work and how to use them.

Wildcard certificates don't work on the firs level, e.g. `*.mydomain` will not be validated by a browser for security reasons.
But `*.sub.mydomain` will work.

## DNS

CNAME are not aliases, they must be unique per name. This is why we cannot have a CNAME at the APEX: Because they conflict with the NS records.
DNS are used for DNS-challenges upon certificate generation, especially when using multiple SAN or wildcard certificates.
