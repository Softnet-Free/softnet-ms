---
layout: default
title: 7.4. Device management
parent: 7. Multi-service site
nav_order: 4
---

## 7.4. Device management

The <span class="header-green">SITE CONFIGURATION</span> panel has a section "<span class="text-blue">list of services</span>" which contains a list of service entities representing the devices set up on the site, and a "<span class="text-cyan">new service</span>" button to create a new service entity. The image below shows a multi-service site with an IP camera set up on it:

![]({{ site.baseurl }}{% link assets/images/image_msite.4_1.png %})

To the left of each service entity, there is a "&gt;&gt;" button which opens the service management menu: 

![]({{ site.baseurl }}{% link assets/images/image_msite.4_2.png %})

### 7.4.1. Service account

The "<span class="text-cyan">account</span>" button of the service manager displays the service URI and a button to generate a password. The service URI has the following format: <span class="text-highlighted">softnet-srv://serviceUuid@serverAddress</span>. Here, "serviceUuid" is an unique identifier of the service entity, and "serverAddress" is an address of the Softnet server.  

To generate a password, click the "<span class="text-green">generate password</span>" button:

![]({{ site.baseurl }}{% link assets/images/image_msite.4_3.png %})

If you lose the current password of the service, you'll not be able to retrieve it from the management system, but can only generate a new one.

### 7.4.2. Hostname

You can assign a name to the physical device on which the service application is hosted. The clients of the device will see this name as a remote service hostname. Clicking the "<span class="text-cyan">hostname</span>" button opens the hostname editor:

![]({{ site.baseurl }}{% link assets/images/image_msite.4_4.png %})

Enter a name in the text box and click the "save" button. In the image below, the IP camera name is changed from "Service1" to "Camera 1":

![]({{ site.baseurl }}{% link assets/images/image_msite.4_5.png %})

### 7.4.3. Service enabling / disabling  

You can use service disabling to temporarily suspend communication between the device and their clients. The "<span class="text-cyan">enable/disable</span>" menu button shows the service's current enabled/disabled status, as well as a button to disable the service if it is enabled, or a button to enable the service if it is disabled.  

The image below shows the service status as "<span class="text-green">enabled</span>" and a button to disable it:

![]({{ site.baseurl }}{% link assets/images/image_msite.4_6.png %})

The next image shows the service status as "<span class="text-red">disabled</span>" and a button to enable it. Also, the service status is shown on the right side of the service management panel:

![]({{ site.baseurl }}{% link assets/images/image_msite.4_7.png %})

### 7.4.4. Site Structure 

Clicking the "<span class="text-cyan">structure</span>" menu button shows the "<span class="text-green">apply structure to the site</span>" button:

![]({{ site.baseurl }}{% link assets/images/image_msite.4_8.png %})

Let's consider what means applying structure to the site. When a device connects to the site for the first time, it provides the site with the **Site Structure** data. And if the site is blank, Softnet builds the structure of the site using the Site Structure data. But what happens if the site has already been built? If the Site Structure provided by the device is identical to what the site is built upon, the service gets online. However, if they're not identical, there can be two more situations:

1. The name of the device's interface represented as &lt;<span class="text-st">Service Type</span>&gt; (&lt;<span class="text-st">Contract Author</span>&gt;) is different from what the site expects, then the service entity is blocked with the status "<span class="text-red">service type conflict</span>". If the device you connected to the site is a wrong device, just disconnect it and connect the right one. However, If it is a right device that you want to set up on the site, then just click the "<span class="text-green">apply structure to the site</span>" button. As a result, the site will be rebuilt and the service status become "normal". However, be aware that:
*  If you have other services on the site, perhaps, some of them have &lt;<span class="text-st">Service Type</span>&gt; (&lt;<span class="text-st">Contract Author</span>&gt;) different from what the site will obtain after rebuilding. In this case, they will be blocked with the error status "<span class="text-red">service type conflict</span>";
*  Perhaps, some of the clients set up on the site have &lt;<span class="text-st">Service Type</span>&gt; (&lt;<span class="text-st">Contract Author</span>&gt;) different from what the site will obtain after rebuilding. In this case, they will be blocked with the error status "<span class="text-red">service type conflict</span>"  

2. The name of the device’s interface is what the site expects but the Site Structure provided by the device is different from what the site is built upon, then the service entity is blocked with the status "<span class="text-red">site structure mismatch</span>". This may be due to the fact that the device's interface has some differences compared to the interface of the device for which the site was actually built. And these differences are so significant that the Site Structures also turned out to be different. If the device you connected to the site is a right device that you want to set up, then just click the "<span class="text-green">apply structure to the site</span>" button. As a result, the site will be rebuilt and the service status become "normal". However, be aware that:
*  If you have other services on the site, perhaps, some of them have the Site Structure different from what you are going to apply to the site. In this case, they will be blocked with the error status "<span class="text-red">site structure mismatch</span>". Anyway, services with different Site Structures cannot coexist on the site;
*  Some of the clients may become incompatable with an updated service version;  

The possible service statuses are considered in the "[Service status]({{ site.baseurl }}{% link docs/msite/device-mgt.md %}#748-service-status)" subsection

### 7.4.5. Ping Period  

A highly mobile device, such as an unmanned aerial vehicle connected to the Internet or a device roaming between Wi-Fi hotspots, can quite often change its IP address. And when it happens, you lose the control over the device until the service application on the device detects that the address is changed and re-establishes the control channel. Depending on the underlying platform, the time required to detect a broken connection can vary quite widely. However, using the Ping Period parameter, you can tune this time as you need. The Ping Period is the amount of time to wait between ping messages that the service app on the device sends to the site. If the ping message is not responded within a certain period of time, the control channel is considered as broken, and the service application re-establishes the control channel.  

Clicking the "<span class="text-cyan">ping period</span>" button opens the Ping Period editor: 

![]({{ site.baseurl }}{% link assets/images/image_msite.4_9.png %})

By default, the Ping Period is 300 seconds (5 minutes). The developer or the device user can set a specific ping period on the device, or leave it at the default value by specifying 0. The Ping Period can also be set here on the management panel. If you specify a value between 10 secondts and 300 seconds, it will overwrite the value set on the device. However, if you specify 0, the Ping Period will be set to the device's local value, or to the default value of 300 seconds if the device’s local value is also 0.

### 7.4.6. Deleting a service

At the upper right corner of the service manager, there is a button "<span class="text-red">X</span>" which allows you to delete the service and consequently the device from the site. This happens without confirming the deletion: 

![]({{ site.baseurl }}{% link assets/images/image_msite.4_10.png %})

### 7.4.7. Creating a new service

You create a new service entity to set up a new device on the site. Clicking the "<span class="text-cyan">new service</span>" button opens a text box to specify the hostname for a new service:

![]({{ site.baseurl }}{% link assets/images/image_msite.4_11.png %})

On the image below, there was created a service with a hostname "Camera 2":

![]({{ site.baseurl }}{% link assets/images/image_msite.4_12.png %})

As you can see, the newly created service has a status "<span class="text-red">service type undefined</span>". To set up a device on this entity, click the "&gt;&gt;" button:

![]({{ site.baseurl }}{% link assets/images/image_msite.4_13.png %})

To generate a password, click the "<span class="text-green">generate password</span>" button:

![]({{ site.baseurl }}{% link assets/images/image_msite.4_14.png %})

Of course, the service account parameters will be different in your case. Enter them into your device and connect it to the site. When first connected, the device provides the site with the Site Structure. If this structure is identical to what the site is built upon, your device will be set up on the site and represented as a service. For this example, we have the second IP camera set up on the site:

![]({{ site.baseurl }}{% link assets/images/image_msite.4_15.png %})

### 7.4.8. Service status

The service on the site can be in one of four possible statuses. If the site is blank, the service entity has a status "<span class="text-red">service type undefined</span>":  

![]({{ site.baseurl }}{% link assets/images/image_msite.4_16.png %})

When the device connects to the service entity for the first time, it provides the site with the Site Structure. If the structure is identical to what the site was built upon, the device is set up on the site. After that, the service status is considered normal and nothing is shown on the right side of the service entity. In the image below, an IP camera is set up on the third service entity named "Camera 3":

![]({{ site.baseurl }}{% link assets/images/image_msite.4_17.png %})

If the site is built for a certain service type, i.e., a service denoted by a certain &lt;<span class="text-st">Service Type</span>&gt; (&lt;<span class="text-st">Contract Author</span>&gt;), and then you connect a device with a different service type to the site, the service will be assigned the status "<span class="text-red">service type conflict</span>". How to resolve this situation, see earlier in the "[Site Structure]({{ site.baseurl }}{% link docs/msite/device-mgt.md %}#744-site-structure)" subsection.  

For example, the image below demonstrates such a scenario. A device with a service interface denoted as <span class="text-st">RTX-7</span> (<span class="text-st">Cold Vision</span>) is connected to the site built for <span class="text-st">RTX-5</span> (<span class="text-st">Cold Vision</span>):

![]({{ site.baseurl }}{% link assets/images/image_msite.4_18.png %})

It is possible that the device's interface and the site have the same service type, but the service status is "<span class="text-red">site structure mismatch</span>". This may be due to the fact that the interface of the device you connected to the site has some differences compared to the interface of the device for which the site was actually built. Check if they have compatible service versions. Anyway, the developer has made some changes to the device interface such that its Site Structure has also been changed. How to resolve this situation, see earlier in the "[Site Structure]({{ site.baseurl }}{% link docs/msite/device-mgt.md %}#744-site-structure)" subsection.  

For example, the image below demonstrates such a scenario. An IP camera with a service interface, denoted as <span class="text-st">RTX-5</span> (<span class="text-st">Cold Vision</span>), connected to the site with the same service type. However,  the service status is "<span class="text-red">site structure mismatch</span>", since the Site Structure provided by the device is different from what the site expects, i.e., what the site was built upon:

![]({{ site.baseurl }}{% link assets/images/image_msite.4_19.png %})

---
#### TABLE OF CONTENTS
* [7.1. Creating a new site]({{ site.baseurl }}{% link docs/msite/creating-site.md %})
* [7.2. Building the site structure]({{ site.baseurl }}{% link docs/msite/building-str.md %})
* [7.3. Site management]({{ site.baseurl }}{% link docs/msite/site-mgt.md %})
* 7.4. Device management