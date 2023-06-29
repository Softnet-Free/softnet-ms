---
layout: default
title: 7.1. Creating a new site
parent: 7. Multi-service site
nav_order: 1
---

## 7.1. Creating a new site

Select the domain in which you want to create a site:

![]({{ site.baseurl }}{% link assets/images/image_msite.1_2.png %})

Below is a domain called "Home Surveillance":

![]({{ site.baseurl }}{% link assets/images/image_msite.1_2.png %})

Clicking the "new site" button takes you to the "New Site" page:

![]({{ site.baseurl }}{% link assets/images/image_msite.1_3.png %})

You can specify the name of a new site or leave it empty and click the "Create" button. This takes you to the <span class="header-green">SITE CONFIGURATION</span> page:

![]({{ site.baseurl }}{% link assets/images/image_msite.1_4.png %})

This is a blank site on which you can install a single device. However, if you want to install multiple identical devices on the site, you need to convert it to multi-service by clicking the "multi-service hosting" button. Convertion must be done while the site is blank:

![]({{ site.baseurl }}{% link assets/images/image_msite.1_5.png %})

Before converting the site, it prints a warning message that asks you to pay attention that all services on a multi-service site must be of the same type. Go ahead and click the "set as multi-service site" button. This turns the site into multi-service:

![]({{ site.baseurl }}{% link assets/images/image_msite.1_6.png %})

The site conversion resulted in two changes:  
1.	The site section that was called "services" has changed to "list of services";
2.	Under the "list of services" heading, a "new service" button has appeared, which allows you to add a new service entity to set up a new device.  

There are also two limitations to be considered:
1.	Converting a site to multi-service must be done while it is a blank site, that is, before connecting any device to the site. If the site structure has already been built, which happens the first time a device connects to the site, it cannot be converted to multi-service;
2.	A site, once converted to multi-service, cannot be converted back to single-service.  

The next step is [building the site structure]({{ site.baseurl }}{% link docs/msite/building-str.md %}).

---
#### TABLE OF CONTENTS
* 7.1. Creating a new site
* [7.2. Building the site structure]({{ site.baseurl }}{% link docs/msite/building-str.md %})
* [7.3. Site management]({{ site.baseurl }}{% link docs/msite/site-mgt.md %})
* [7.4. Device management]({{ site.baseurl }}{% link docs/msite/device-mgt.md %})