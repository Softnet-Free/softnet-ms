---
layout: default
title: 3.5. Setting up clients
parent: 3. Quickly deploying several identical devices
nav_order: 5
---

## 3.5. Setting up clients

Client management is carried out on the <span class="header-green">CLIENT MANAGEMENT</span> page. To switch to the client manager, click on the "<span class="text-cyan">clients</span>" button at the upper left corner of the panel:

![]({{ site.baseurl }}{% link assets/images/image_mdp.5_1.png %})

Here, you can set up clients for users authorized on the site:

![]({{ site.baseurl }}{% link assets/images/image_mdp.5_2.png %})

First, we create a client entity for the Owner user to set up a remote control application. Clicking the "<span class="text-green">add client</span>" button, which is to the right of Owner, creates a client entity:

![]({{ site.baseurl }}{% link assets/images/image_mdp.5_3.png %})

Clicking the "<span class="text-green">generate password</span>" button generates a client password:

![]({{ site.baseurl }}{% link assets/images/image_mdp.5_4.png %})

Now, we have the client URI and password:  

&nbsp;&nbsp;&nbsp;&nbsp;softnet-m://a78rhvpwn@ts.softnet-iot.org  
&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-orange">password:</span> rxj6EprGR  

We provide them to the client application and connect it to the site. If everything is Ok, the client gets online and the client entity takes the following view:

![]({{ site.baseurl }}{% link assets/images/image_mdp.5_5.png %})

Typically, a client is represented on the site by a **client key** and **client description**. The **client key** is created by the site, but the **client description** is provided by the client itself. The latter is optional but highly desirable parameter. It usually contains the functional description of the client and its version, which helps the owner in administrative tasks. In case of our example, the client is represented by:  
* <span class="text-caption">client key</span>: a78rhvpwn
* <span class="text-caption">description</span>: Surveillance Control. V: 2.1.2  

We've assigned the <span class="text-role">Adminstrator</span> role to Owner, so the remote control application we've set up can interact with the IP cameras with administrative rights.  

Now we'll create a client entity for Alison and set up a remote control application on this entity. Clicking the "<span class="text-green">add client</span>" button, which is to the right of Alison, creates a client entity:

![]({{ site.baseurl }}{% link assets/images/image_mdp.5_6.png %})

Then clicking on the "<span class="text-green">generate password</span>" button creates a password:

![]({{ site.baseurl }}{% link assets/images/image_mdp.5_7.png %})

We have the client URI and password:  

&nbsp;&nbsp;&nbsp;&nbsp;softnet-m://t5bd8tyt6@ts.softnet-iot.org  
&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-orange">password:</span> Zk964byTN  

We provide them to the Alison's client application and connect it to the site. If everything is Ok, the client gets online and the client entity takes the following view:

![]({{ site.baseurl }}{% link assets/images/image_mdp.5_8.png %})

We have two remote control applications set up on the site. Each will interact with the IP cameras in accordance with the role we assigned to the appropriate user in the previous section.  

It’s worth noting that the mechanism of **Contacts** offers a much more efficient way to share access to devices with other persons/organizations. This is a topic of [chapter 8]({{ site.baseurl }}{% link docs/contacts/index.md %}).

---
#### TABLE OF CONTENTS
* [3.1. Creating a domain]({{ site.baseurl }}{% link docs/multi/new-domain.md %})
* [3.2. Creating a multi-service site]({{ site.baseurl }}{% link docs/multi/msite.md %})
* [3.3. Setting up devices]({{ site.baseurl }}{% link docs/multi/setup-devs.md %})
* [3.4. Assigning access rights to users]({{ site.baseurl }}{% link docs/multi/access-rights.md %})
* 3.5. Setting up clients