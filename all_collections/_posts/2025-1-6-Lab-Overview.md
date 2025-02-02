---
layout: post
title: Lab Overview
date: 2025-1-6
categories: ["Homelab", "Showcase"]
---

It has been awhile since my last lab update and a lot has changed since. As I enter my last semester of undergrad I would like to use this opportunity to showcase what I currently run. Most projects align with my goal of becoming a cybersecurity engineer.

## Overview:

![file.jpg](/assets/file.jpg)
  

#### **Cheap Amazon Table (Left):**

##### Supermicro E300-8D:

- **Proxmox**. The workhorse of my lab 
    - **PfSense**
        - Suricata: NIPS/NIDS
        - pfBlockerNG: Geofencing
        - OpenVPN: Remote lab access for internal applications and resources.
    - **Kasm:** Used mainly for malware/phishing email analysis.
    - **Elasticsearch:** Currently running a single node, going to expand onto my Lenovo running Proxmox soon to have a place for replica shards.
    - **Ubuntu Server:** Main docker host 
        - Bookstack: Notes and blog storage.
        - Keycloak
        - Nextcloud: Self hosted OneDrive.
        - Gitlab: My container registry in progress.
        - Watchtower: Automated container updates.

##### TP-Link 8 Port Managed Switch(Hidden):   


- To be replaced soon as I rely solely on my larger switch.

##### Lenovo Mini #1: 

- **Proxmox**
    - **Ubuntu Server:** Secondary docker host. 
        - **LLDAP:** Contains user and group information for Keycloak.
        - **Watchtower:** Automated container updates.
    - **Ubuntu Server:** Dedicated backup VM. Makes backups easier by avoiding the hassle of Synology's GUI.
    - **Ubuntu Server:** Dedicated log ingestor for pfSense, this VM has an elastic agent installed with the pfSense integration.

##### Lenovo Mini #2: 

- Ubuntu, this is my lab metrics viewer on the right.

##### Synology NAS:

- Spinning disks here for backup purposes.

![supermicro.jpeg](/assets/supermicro.jpeg)

#### **Standing Desk (Middle):** 

##### Laptop:

- Nothing special, just my work PC I hook up to the dock setting just behind it.

##### Gaming Rig: 

- Dual boots into Windows and Ubuntu for the best of both worlds. Occasionally used for some gaming when I am not working on certifications or coursework.

#### **Wood Table (Right):**

 Though hard to believe, I built the table myself to be able to store a Poweredge r710 vertically for when I need a space heater. /s

##### Cisco Catalyst 2960-X:

- Great for my VoIP phone that requires PoE, no more injectors!

##### Dell Poweredge r710:

- Not currently in use, used for experimentation and white noise.

![monitor.jpeg](/assets/monitor.jpeg)

### Whats Next

 As a homelab-ing goes, my laundry list of items are endless but here are a few:

- Switch Consolidation
- SELinux on hosts
- Elasticsearch expansion and add additional threat intel sources
- Use Keycloak as the IDP for Nextcloud

 Thanks for reading! If you have any questions or comments, I would love to talk about it! Please message me on LinkedIn!
