---
title: Part 2&#58; Laying the Virtual Groundwork
layout: post
excerpt: As mentioned in Part 1 I'm hoping to go through and test out the various hypervisors that are currently on the market. To give them all a fair playing field I've set aside a machine for this purpose. Currently I only have one so I will be limited in testing certain features but there is a hope to have two identical machines soon to test out things such as High Availability and Clusters. 
---

<p class="intro"><span class="dropcap">A</span>s mentioned in Part 1 I'm hoping to go through and test out the various hypervisors that are currently on the market. To give them all a fair playing field I've set aside a machine for this purpose. Currently I only have one so I will be limited in testing certain features but there is a hope to have two identical machines soon to test out things such as High Availability and Clusters. For now the details of the dev machine are below.</p>

* Mini-ITX Board with Intel Celeron 847 Dual-Core CPU with 8GB RAM
* Dual Realtek NICs and 256GB SSD for local datastore

###Features I'll be testing
To ensure each tool gets tested in the same areas I've drafted a rough list of various things I'll be testing on each. It's not an exhaustive list but it will provide a base of comparison between them.

1. Installation of hypervisor
2. Creation of Virtual Machines 
 * Ubuntu Server 14.04.1
 * Windows Server 2012 R2 Standard Edition
 * CentOS 7 and/or openSuse 13.2
 * Possibly Debian stable
3. Creation of templates and deploying templates
4. Performance logs/statistics
5. Resource allocations/pool allocation
6. Management of server/vms (on host, management application, web client)
7. Built in backup and available backup tools

###Features I won't be testing
Certain things I can't test due to needing multiple machines so for now I won't be looking at them. However, once I've gotten two machines to set aside for testing I'll revisit the below features.

1. HA
2. Moving and migration between datastores
3. Clusters/pools

###Hypervisors
I've decided to try out the 4 big players in the virtual market to start. I'm also starting out with XenServer because there seems to be less information regarding it around on the web; VMware is the de-facto standard for many after all.

1. XenServer 6.5
2. Hyper-V 2012 Server
3. vSphere ESXi 5.5
4. KVM

###Linux Containers
Finally I hope to give Docker a test out too for certain use cases. Linux containers are currently a hot topic and it would be interesting to see how it functions for virtualizing various Linux machines. I'm keeping it separate however as it is a different product than a typical hypervisor. For a quick overview of what Linux containers have a look at the Linux Containers website, Docker, and a blog post showing how to get one up and running quickly.

[Click here for Part 3.1!]({% post_url 2015-02-15-part-3-1-xenserver %})
