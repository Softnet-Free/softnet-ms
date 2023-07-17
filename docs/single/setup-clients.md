---
layout: default
title: 2.4. Setting up clients
parent: 2. Quickly deploying a single device
nav_order: 4
---

## 2.4. Setting up clients

Client management is carried out on the <span class="header-green">CLIENT MANAGEMENT</span> page. To switch to the client manager, click on the "<span class="text-cyan">clients</span>" button at the upper left corner of the panel:

![]({{ site.baseurl }}{% link assets/images/image_sdp.4_1.png %})

Here, you can set up clients for users authorized on the site:

![]({{ site.baseurl }}{% link assets/images/image_sdp.4_2.png %})

First, we create a client entity for the Owner user to set up a remote control application. Clicking the "<span class="text-green">add client</span>" button, which is to the right of Owner, creates a client entity:

![]({{ site.baseurl }}{% link assets/images/image_sdp.4_3.png %})

Clicking the "<span class="text-green">generate password</span>" button generates a client password:

![]({{ site.baseurl }}{% link assets/images/image_sdp.4_4.png %})

Now, we have the client URI and password:  

&nbsp;&nbsp;&nbsp;&nbsp;softnet-s://x6sgw0syd8@ts.softnet-iot.org  
&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-orange">password:</span> uVadVb7VGL  

We provide them to the client application and connect it to the site. If everything is Ok, the client gets online and the client entity takes the following view:

![]({{ site.baseurl }}{% link assets/images/image_sdp.4_5.png %})

Typically, a client is represented on the site by a **client key** and **client description**. The **client key** is created by the site, but the **client description** is provided by the client itself. The latter is optional but highly desirable parameter. It usually contains the functional description of the client and its version, which helps the owner in administrative tasks. In case of our example, the client is represented by:  
* <span class="text-caption">client key</span>: x6sgw0syd8
* <span class="text-caption">description</span>: Remote Control. V: 1.0.2

We've assigned the <span class="text-role">Adminstrator</span> role to Owner, so the remote control application we've set up can interact with the Smart Home controller with administrative rights.  

Now we'll create a client entity for Alex and set up a remote control application on this entity. Clicking the "<span class="text-green">add client</span>" button, which is to the right of Alex, creates a client entity:

![]({{ site.baseurl }}{% link assets/images/image_sdp.4_6.png %})

Then clicking on the "<span class="text-green">generate password</span>" button creates a password:

![]({{ site.baseurl }}{% link assets/images/image_sdp.4_7.png %})

We have the client URI and password:  

&nbsp;&nbsp;&nbsp;&nbsp;softnet-s://y0ge1532uu@ts.softnet-iot.org  
&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-orange">password:</span> NPwktPJmLd  

We provide them to the Alex's client application and connect it to the site. If everything is Ok, the client gets online and the client entity takes the following view:

![]({{ site.baseurl }}{% link assets/images/image_sdp.4_8.png %})

We have two remote control applications set up on the site. Each will interact with the Smart Home controller in accordance with the role we assigned to the appropriate user in the previous section.  

It’s worth noting that the mechanism of **Contacts** offers a much more efficient way to share access to devices with other persons/organizations. This is a topic of [chapter 8]({{ site.baseurl }}{% link docs/contacts/index.md %}).

---
#### TABLE OF CONTENTS
* [2.1. Creating a domain]({{ site.baseurl }}{% link docs/single/new-domain.md %})
* [2.2. Setting up a device]({{ site.baseurl }}{% link docs/single/setup-dev.md %})
* [2.3. Assigning access rights to users]({{ site.baseurl }}{% link docs/single/access-rights.md %})
* 2.4. Setting up clients
