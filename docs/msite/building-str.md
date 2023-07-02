---
layout: default
title: 7.2. Building the site structure
parent: 7. Multi-service site
nav_order: 2
---

## 7.2. Building the site structure

A blank multi-service site has a status "<span class="text-red">site blank</span>". It can contain multiple blank service entities with status "<span class="text-red">service type undefined</span>":

![]({{ site.baseurl }}{% link assets/images/image_msite.2_1.png %})

To set up devices and clients on the site, you first need to build the site structure. Fortunately, this is done automatically just by connecting a device to the site. Softnet builds the site structure in accordance with the **Site Structure** data provided by the device. To connect a device to the site, you need the account data of any service entity of the site. In the image below, we have one service entity named "Service1". Clicking the "&gt;&gt;" button, which is to the right of "Service1", opens the service management panel:

![]({{ site.baseurl }}{% link assets/images/image_msite.2_2.png %})

Clicking the "<span class="text-cyan">account</span>" button displays the service URI and a button to generate a password:

![]({{ site.baseurl }}{% link assets/images/image_msite.2_3.png %})

Clicking the "<span class="text-green">generate password</span>" button creates a password:

![]({{ site.baseurl }}{% link assets/images/image_msite.2_4.png %})

For this example, we have the following service URI and password:  

&nbsp;&nbsp;&nbsp;&nbsp;softnet-srv://e286aef9-edbe-4175-9952-6cae5810131d@ts.softnet-iot.org  
&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-orange">password:</span> NkZnsk8JLgcC  

Of course, the service account parameters will be different in your case. Enter them into your device and connect it to the blank site. After building the site structure, your device will be represented on the site as a service. Depending on whether your device employs Role-Based Access Control or Plain Access Control, the site obtains an appropriate set of parameters, which we'll consider next. For more information on using access control, see the chapter "[Users & access rights]({{ site.baseurl }}{% link docs/access/index.md %})".

### Site with Role-Based Access Control

If your device employs RBAC, the site will be constructed accordingly. As an example, let's take an IP camera, which uses three roles <span class="text-role">Administrator</span>, <span class="text-role">Operator</span> and <span class="text-role">User</span> to implement different levels of access to the device. The site constructed for our example has the following view:

![]({{ site.baseurl }}{% link assets/images/image_msite.2_5.png %})

The site, after building the structure, obtaines a set of additional parameters, which are circled in the following image and described below:  

![]({{ site.baseurl }}{% link assets/images/image_msite.2_6.png %})

In the descriptions below, a service application is software hosted or embedded in a device that implements an interface for interacting with clients over IP networks. The interface is denoted by the names of **service type** and **contract author**, represented in Softnet MS as &lt;<span class="text-st">Service Type</span>&gt; (&lt;<span class="text-st">Contract Author</span>&gt;).  

1.	Here are placed the names of &lt;<span class="text-st">Service Type</span>&gt; (&lt;<span class="text-st">Contract Author</span>&gt;) provided by your device to the site. They indicate the device’s functionality. In case of our example, these names are <span class="text-st">RTX-5</span> (<span class="text-st">Cold Vision</span>). Of course, the names in your case will be different from our example. Clients you are going to set up on the site must be designed to interact with the given type of device, i.e., the type denoted by the same &lt;<span class="text-st">Service Type</span>&gt; (&lt;<span class="text-st">Contract Author</span>&gt;). In case of our example: <span class="text-st">RTX-5</span> (<span class="text-st">Cold Vision</span>);  
2.	If your service application employs versioning, the service version will appear in this place;  
3.	If your service application employs Role-Based Access Control (RBAC), the list of roles will appear in this place. You can assign these roles to domain users;  
4.	Here you can select one of the roles listed above as the default role for every domain user. This is useful if you have many users and want to assign to all of them (except dedicated users) one specific role by default rather than explicitly assigning that role to each user;
5.  Some service applications may specify a role that will be assigned to **Owner** when the site structure is built. In our example, the IP camera has specified the <span class="text-role">Administrator</span> role to assign to Owner;  
6.	Users that do not have any access rights to the service are listed in the <span class="text-red">DENIED USERS</span> section.  

For a detailed description of items 3 to 6 circled in the image above, see the "[Users & access rights]({{ site.baseurl }}{% link docs/access/index.md %})" chapter.  

### Site with Plain Access Control

If your device employs Plain Access Control, the domain users will have a full access to the device by the fact of being added to the site. The site constructed for such a device does not have parameters **3**, **4** and **5** of an RBAC-based site. Instead of them, it obtains one parameter called "Implicit users" that allows or denies the domain users that are not explicitly added to the site. See the "[Users & access rights]({{ site.baseurl }}{% link docs/access/index.md %})" chapter for details.  

The following image shows the site constructed for our IP camera that uses Plain Access Control:

![]({{ site.baseurl }}{% link assets/images/image_msite.2_7.png %})

*  The first two parameters **1** and **2** are exactly the same as those discussed in the previous section for an RBAC-based site;
*  Parameter **3**: "Implicit users" with possible values <span class="text-green">allowed</span> / <span class="text-red">denied</span>. This parameter is useful if you have many domain users and want to add all of them (except dedicated users) to the site rather than explicitly adding each user to the site;
*  Parameter **4**: users that do not have access rights to the service are listed in the <span class="text-red">DENIED USERS</span> section.  

---
#### TABLE OF CONTENTS
* [7.1. Creating a new site]({{ site.baseurl }}{% link docs/msite/creating-site.md %})
* 7.2. Building the site structure
* [7.3. Site management]({{ site.baseurl }}{% link docs/msite/site-mgt.md %})
* [7.4. Device management]({{ site.baseurl }}{% link docs/msite/device-mgt.md %})
