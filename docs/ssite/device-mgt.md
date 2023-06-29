---
layout: default
title: 6.4. Device management
parent: 6. Single-service site
nav_order: 4
---

## 6.4. Device management

The service entity represents a device that you set up on the site. The "<span class="text-blue">service</span>" section of the <span class="header-green">SITE CONFIGURATION</span> panel contains menu buttons for managing the service: "<span class="text-cyan">account</span>", "<span class="text-cyan">hostname</span>", "<span class="text-cyan">ping period</span>", and "<span class="text-cyan">structure</span>". In addition, the service status represents its operating state. If the service is incapable to operate, the service status is shown on the right side of the "<span class="text-blue">service</span>" section.

![]({{ site.baseurl }}{% link assets/images/image_ssite.4_1.png %})

### 6.4.1. Service status

The service on a site has four possible status values. If the site is blank, the service entity has a status "<span class="text-red">service type undefined</span>":  

![]({{ site.baseurl }}{% link assets/images/image_ssite.4_2.png %})

When the device connects to the blank site for the first time, Softnet builds the structure of the site in accordance with the **Site Structure** data provided by the device. After that, the service status is considered normal and nothing is shown on the right side of the "<span class="text-blue">service</span>" section:

![]({{ site.baseurl }}{% link assets/images/image_ssite.4_3.png %})

If the site is built for a certain service type, i.e., a service denoted by a certain &lt;<span class="text-st">Service Type</span>&gt; (&lt;<span class="text-st">Contract Author</span>&gt;), and then you connect a device with a different service type to the site, the service will be assigned the status "<span class="text-red">service type conflict</span>". How to resolve this situation, see further in the "[Site Structure]({{ site.baseurl }}{% link docs/ssite/device-mgt.md %}#645-site-structure)" subsection.  

For example, the image below demonstrates such a scenario. A device with a service interface, denoted as <span class="text-st">RTX-5</span> (<span class="text-st">Cold Vision</span>), connected to the site built for the service interface <span class="text-st">Baby Monitor</span> (<span class="text-st">Softnet Free</span>):

![]({{ site.baseurl }}{% link assets/images/image_ssite.4_4.png %})

It is possible that the device's interface and the site have the same service type, but the service status is "<span class="text-red">site structure mismatch</span>". This may be due to the fact that the interface of the device you connected to the site has some differences compared to the interface of the device for which the site was actually built. Check if they have compatible service versions. Anyway, the developer has made some changes to the device interface such that its Site Structure has also been changed. How to resolve this situation, see further in the "[Site Structure]({{ site.baseurl }}{% link docs/ssite/device-mgt.md %}#645-site-structure)" subsection.  

For example, the image below demonstrates such a scenario. A device with a service interface, denoted as <span class="text-st">Baby Monitor</span> (<span class="text-st">Softnet Free</span>), connected to the site with the same service type. However,  the service status is "<span class="text-red">site structure mismatch</span>", since the Site Structure provided by the device is different from what the site expects, i.e., what the site was built upon:

![]({{ site.baseurl }}{% link assets/images/image_ssite.4_5.png %})

### 6.4.2. Service account

The "<span class="text-cyan">account</span>" button of the service manager displays the service URI and a button to generate a password:

![]({{ site.baseurl }}{% link assets/images/image_ssite.4_6.png %})

The service URI has the following format: <span class="text-highlighted">softnet-srv://serviceUuid@serverAddress</span>. Here, "serviceUuid" is an unique identifier of the service entity, and "serverAddress" is an address of the Softnet server.  

To generate a password, click the "<span class="text-green">generate password</span>" button:

![]({{ site.baseurl }}{% link assets/images/image_ssite.4_7.png %})

If you lose the current password of the service, you'll not be able to retrieve it from the management system, but can only generate a new one.

### 6.4.3. Hostname

You can assign a name to the physical device where the service application is hosted. The clients of the device will see this name as a remote service hostname. Clicking the "<span class="text-cyan">hostname</span>" button opens the hostname editor:

![]({{ site.baseurl }}{% link assets/images/image_ssite.4_8.png %})

Enter a name in the text box and click the "save" button. Below, the name of the Baby Monitor device is changed from "Service1" to "Monitor 1":

![]({{ site.baseurl }}{% link assets/images/image_ssite.4_9.png %})

### 6.4.4. Ping Period  

A highly mobile device, such as an unmanned aerial vehicle connected to the Internet or a device roaming between Wi-Fi hotspots, can quite often change its IP address. And when it happens, you lose the control over the device until the service application on the device detects that the address is changed and re-establishes the control channel. Depending on the underlying platform, the time required to detect a broken connection can vary quite widely. However, using the Ping Period parameter, you can tune this time as you need. The Ping Period is the amount of time to wait between ping messages that the service app on the device sends to the site. If the ping message is not responded within a certain period of time, the control channel is considered as broken, and the service application re-establishes the control channel.  

Clicking the "<span class="text-cyan">ping period</span>" button opens the Ping Period editor: 

![]({{ site.baseurl }}{% link assets/images/image_ssite.4_10.png %})

By default, the Ping Period is 300 seconds (5 minutes). The developer or the device user can set a specific ping period on the device, or leave it at the default value by specifying 0. The Ping Period can also be set here on the management panel. If you specify a value between 10 secondts and 300 seconds, it will overwrite the value set on the device. However, if you specify 0, the Ping Period will be set to the device's local value, or to the default value of 300 seconds if the device’s local value is also 0.

### 6.4.5. Site Structure  

The last button in the service management menu is "<span class="text-cyan">structure</span>". Clicking this button shows the "<span class="text-green">apply structure to the site</span>" button:

![]({{ site.baseurl }}{% link assets/images/image_ssite.4_11.png %})

Let's consider what means applying structure to the site. When a device connects to the site for the first time, it provides the site with the **Site Structure** data. And if the site is blank, Softnet builds the structure of the site using the Site Structure data. But what happens if the site has already been built? If the Site Structure provided by the device is identical to what the site is built upon, the service gets online. However, if they're not identical, there can be two more situations:

1. The name of the device's interface represented as &lt;<span class="text-st">Service Type</span>&gt; (&lt;<span class="text-st">Contract Author</span>&gt;) is different from what the site expects, then the service entity is blocked with the status "<span class="text-red">service type conflict</span>". If the device you connected to the site is a wrong device, just disconnect it and connect the right one. However, If it is a right device that you want to set up on the site, then just click the "<span class="text-green">apply structure to the site</span>" button. As a result, the site will be rebuilt and the service status become "normal". However, be aware that perhaps some of the clients set up on the site have &lt;<span class="text-st">Service Type</span>&gt; (&lt;<span class="text-st">Contract Author</span>&gt;) different from what the site will obtain after rebuilding. In this case, they will be blocked with the error status "<span class="text-red">service type conflict</span>";  

2. The name of the device’s interface is what the site expects but the Site Structure provided by the device is different from what the site is built upon, then the service entity is blocked with the status "<span class="text-red">site structure mismatch</span>". This may be due to the fact that the device's interface has some differences compared to the interface of the device for which the site was actually built. And these differences are so significant that the Site Structures also turned out to be different. If the device you connected to the site is a right device that you want to set up, then just click the "<span class="text-green">apply structure to the site</span>" button. As a result, the site will be rebuilt and the service status become "normal". However, be aware that some of the clients may become incompatable with an updated service version;

---
#### TABLE OF CONTENTS
* [6.1. Creating a new site]({{ site.baseurl }}{% link docs/ssite/creating-site.md %})
* [6.2. Building the site structure]({{ site.baseurl }}{% link docs/ssite/building-str.md %})
* [6.3. Site management]({{ site.baseurl }}{% link docs/ssite/site-mgt.md %})
* 6.4. Device management