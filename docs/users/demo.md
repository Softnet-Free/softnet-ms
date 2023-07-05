---
layout: default
title: 9.1. Demo project
parent: 9. Users & access rights
nav_order: 1
---

## 9.1. Demo project

Our demo project consists of a video surveillance system, a smart thermostat, and an alarm system. All devices are deployed in a domain called "Office Automation". How to create a domain is described in "[Creating a domain]({{ site.baseurl }}{% link docs/domains/new-domain.md %})".  

A demo surveillance system consists of a few IP cameras called RTX-5 (Cold Vision) and a client app for remote control. The devices employ a role-based access control and use three roles. All cameras are set up on a multi-service site. Building a multi-service site and setting up devices is discussed in "[Multi-service site]({{ site.baseurl }}{% link docs/msite/index.md %})". Setting up client apps for this demo system is shown in the next chapter "[Client management]({{ site.baseurl }}{% link docs/clients/index.md %})". Below is a view of this site named "Surveillance System":

![]({{ site.baseurl }}{% link assets/images/image_usr.1_1.png %})

The next demo system is a smart thermostat called iBreeze (SmartEco). The system consists of a controller and a remote control app. The device employs a role-based access control and use two roles: "Admin" and "User". The controller is set up on a single-service site. For more information on building a single-service site and setting up a device, see the "[Single-service site]({{ site.baseurl }}{% link docs/ssite/index.md %})" chapter. Setting up client apps for this demo is shown in the next chapter "[Client management]({{ site.baseurl }}{% link docs/clients/index.md %})". Below is a view of this site named "Smart Thermostat":

![]({{ site.baseurl }}{% link assets/images/image_usr.1_2.png %})

The third demo project component is an alarm system called iSentry (Argus). The system consists of a controller, which is set up on a single-service site, and a remote control app. In contrast to previous systems, the controller employs a plain access control. Setting up client apps for this demo is also shown in the next chapter "[Client management]({{ site.baseurl }}{% link docs/clients/index.md %})". Below is a view of this site named "Alarm System":

![]({{ site.baseurl }}{% link assets/images/image_usr.1_3.png %})

---
#### TABLE OF CONTENTS
* 9.1. Demo project
* [9.2. User management]({{ site.baseurl }}{% link docs/users/user-mgt.md %})
* [9.3. Assigning access rights]({{ site.baseurl }}{% link docs/users/access-rights.md %})
