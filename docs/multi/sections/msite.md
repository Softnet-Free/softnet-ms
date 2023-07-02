---
layout: default
title: 4.2. Creating a multi-service site
parent: 4. Deploying multiple identical devices
nav_order: 2
---

## 4.2. Creating a multi-service site

To set up several IP cameras, we need to create a multi-service site. The devices will be represented on the site as a list of services. Clicking the “new site” button takes us to the “New Site” page:

![]({{ site.baseurl }}{% link assets/images/image_mdp.2_1.png %})

We can leave the "description" field empty and click "Create", which creates a site and takes us to the SITE CONFIGURATION page:  

![]({{ site.baseurl }}{% link assets/images/image_mdp.2_2.png %})

This is a blank site on which we can set up a single device. However, if we want to set up multiple identical devices on the site, we need to convert it to multi-service by clicking the "multi-service hosting" button. Convertion must be done while the site is blank:  

![]({{ site.baseurl }}{% link assets/images/image_mdp.2_3.png %})

Before converting the site, it prints a warning message that asks us to pay attention that all services on a multi-service site must be of the same type:  

![]({{ site.baseurl }}{% link assets/images/image_mdp.2_4.png %})

Since all of our IP cameras are identical, we go ahead and click the "set as multi-service site" button. This turns the site into multi-service:  

![]({{ site.baseurl }}{% link assets/images/image_mdp.2_5.png %})

You might have noticed two changes:  
1.	The site section that was previously called "service" has changed to "list of services";
2.	Under the "list of services" heading, a "new service" button has appeared, which allows you to add a new service entity to set up a new device.  

There are also two limitations to be considered:
1.	Converting a site to multi-service must be done while it is a blank site, that is, before connecting any device to the site. If the site has already been constructed, which happens the first time a device connects to the site, it cannot be converted to multi-service;
2.	A site, once converted to multi-service, cannot be converted back to single-service.  

Now we can set up devices on the site. This is a topic of the [next section]({{ site.baseurl }}{% link docs/multi/sections/setup-devs.md %}).

---
#### TABLE OF CONTENTS
* [4.1. Creating a domain]({{ site.baseurl }}{% link docs/multi/sections/new-domain.md %})
* 4.2. Creating a multi-service site
* [4.3. Setting up devices]({{ site.baseurl }}{% link docs/multi/sections/setup-devs.md %})
