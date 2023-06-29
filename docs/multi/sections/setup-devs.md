---
layout: default
title: 4.3. Setting up devices
parent: 4. Deploying multiple identical devices
nav_order: 3
---

## 4.3. Setting up devices on a multi-service site

At this moment, our multi-service site contains nothing but one blank service entity with status "<span class="text-red">service type undefined</span>". And the site status is "<span class="text-red">site blank</span>":

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_1.png %})

We set up the first IP camera to "Service1" entity. Clicking the "&gt;&gt;" button, which is to the left of "Service1", opens the service management panel:

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_2.png %})

Clicking the "account" button shows the service URI and a button to generate a password:

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_3.png %})

Clicking the "generate password" button generates a password:

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_4.png %})

We have the following service URI and password that we can use to connect an IP camera:  

&nbsp;&nbsp;&nbsp;&nbsp;softnet-srv://572c8a65-6c6e-431f-97bf-d6ea81bf98af@ts.softnet-iot.org  
&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-orange">password</span>: v5j8x4pnEZ  

When the camera first connects to the site, it provides the required information to the Softnet server to build the structure of the site. The following is our constructed multi-service site:

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_5.png %})

Let’s change the default service’s hostname, "Service1", to "Camera 1". Clicking the "&gt;&gt;" button, which is to the left of the name "Service1", opens the service management panel: 

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_6.png %})

Clicking the "hostname" button opens the hostname editor:

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_7.png %})

We enter the name "Camera 1" to the text field and click the "save" button. Then we have the following view of the IP camera entity. It is displayed as a combination of the device's name "Camera 1" and software version "2.3.1":

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_8.png %})

So far we set up only one device. To set up the next device, we create a new service entity. Clicking the "new service" button displays a textbox for entering the hostname for a new service:

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_9.png %})

We enter the name "Camera 2" and click the "add service" button:

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_10.png %})

Now we have a blank service entity named "Camera 2":

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_11.png %})

Clicking the "&gt;&gt;" button opens the service management panel:

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_12.png %})

Further, we repeat the steps made for the "Camera 1":
* generate a password by clicking the "generate password" button;
* provide the service URI and password to the next IP camera and connect it to the site.

As a result, we have the following:

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_13.png %})

To set up the next device, we create a new service entity and repeat all those steps we made for the second device. Continuing in this way, we can set up multiple identical devices on  the site. The image below shows four IP cameras set up on the site: 

![]({{ site.baseurl }}{% link assets/images/image_mdp.3_14.png %})


---
#### TABLE OF CONTENTS
* [4.1. Creating a domain]({{ site.baseurl }}{% link docs/multi/sections/new-domain.md %})
* [4.2. Creating a multi-service site]({{ site.baseurl }}{% link docs/multi/sections/msite.md %})
* 4.3. Installing devices


