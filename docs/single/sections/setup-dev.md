---
layout: default
title: 3.2. Setting up a device
parent: 3. Deploying a single device
nav_order: 2
---

## 3.2. Setting up a device

To set up a Smart Home controller, we create a site. The controller will be presented on the site as a **service**. Clicking the "new site" button takes us to the "New Site" page:

![]({{ site.baseurl }}{% link assets/images/image_sdp.2_1.png %})

We leave the "description" field empty and click "Create". This creates a site and takes us to the SITE CONFIGURATION panel:

![]({{ site.baseurl }}{% link assets/images/image_sdp.2_2.png %})

The newly created site contains nothing but one blank service entity with status "<span class="text-red">service type undefined</span>". The site itself has a status "<span class="text-red">site blank</span>". We can set up on the site one service application. It can be an autonomous device or PC application that employs the Softnet platform. The site we have created is called a single-service site. Deploying multiple identical devices on the site is discussed in the [next chapter]({{ site.baseurl }}{% link docs/multi/index.md %}).  

The images below demonstrate setting up a Smart Home controller on the site. Clicking the "account" button displays the service URI and a button to generate a password:

![]({{ site.baseurl }}{% link assets/images/image_sdp.2_3.png %})

Clicking the "generate password" button creates a password:

![]({{ site.baseurl }}{% link assets/images/image_sdp.2_4.png %})

Now we have the service URI and password:  

&nbsp;&nbsp;&nbsp;&nbsp;softnet-srv://1c25b985-ed51-436c-ab5a-f3b111e6494b@ts.softnet-iot.org  
&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-orange">password:</span> K4aBbKd9K2  

For your device, the service account parameters will have a similar format. Enter them into your device and connect it to the site. When your device connects for the first time, the site structure is built according to the information provided by your device. On the site, your device will be represented as a service. For our example, we have the following:

![]({{ site.baseurl }}{% link assets/images/image_sdp.2_5.png %})

Let's take a look at 5 parameters circled in the following image:

![]({{ site.baseurl }}{% link assets/images/image_sdp.2_6.png %})

1.	These are the names of &lt;<span class="text-st">Service Type</span>&gt; and &lt;<span class="text-st">Contract Author</span>&gt; provided by the Smart Home controller to the blank site. They indicate the service interface, that is, the device’s functionality. Clients that we are going to set up on the site must be designed to consume the service of this type, i.e.,  <span class="text-st">Smart Home</span> (<span class="text-st">John Doe</span>);  
2.	If your service application employs versioning, the service version will appear in this place;  
3.	If your service application employs role-based access control (RBAC), the list of roles will appear in this place. You can assign these roles to domain users;  
4.	Here you can select one of the roles listed above as the default role for every domain user. This is useful if you have many users and want to assign to all of them one specific role by default rather than explicitly assigning that role to each user;  
5.	Users that do not have any access rights to the service are listed in the <span class="text-red">DENIED USERS</span> section.  

In the [next section]({{ site.baseurl }}{% link docs/single/sections/access-rights.md %}) we'll assign access rights to users.

---
#### TABLE OF CONTENTS
* [3.1. Creating a domain]({{ site.baseurl }}{% link docs/single/sections/new-domain.md %})
* 3.2. Setting up a device
* [3.3. Assigning access rights to users]({{ site.baseurl }}{% link docs/single/sections/access-rights.md %})
* [3.4. Setting up clients]({{ site.baseurl }}{% link docs/single/sections/setup-clients.md %})
