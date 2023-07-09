---
layout: default
title: 10.1. It's just a piece of cake
parent: 10. Client management
nav_order: 1
---

## 10.1. It's just a piece of cake

Client management operations are performed in the <span class="header-green">CLIENT MANAGER</span> panel. Clicking the "<span class="text-cyan">clients</span>" button opens the manager:

![]({{ site.baseurl }}{% link assets/images/image_clt.1_1.png %})

Here is a client manager for the demo site "Surveillance System":

![]({{ site.baseurl }}{% link assets/images/image_clt.1_2.png %})

Client entities are displayed in the "<span class="text-blue">clients</span>" section. It contains a two-level list, where the first level consists of users authorized on the site, and the second level consists of clients associated with users of the first level and inheriting their access rights. To the right of each user, except for the Contact users, there is an "<span class="text-green">add client</span>" button, clicking on which adds a new client associated with this user.  

In the image below, a client is added for GuardPost:

![]({{ site.baseurl }}{% link assets/images/image_clt.1_3.png %})

Let's generate a password and connect a client application to the site. After the first connection of the client app, the client entity looks like this:

![]({{ site.baseurl }}{% link assets/images/image_clt.1_4.png %})

Typically, a client is represented on the site by a **client key** and **client description**. The **client key** is created by the site, but the **client description** is provided by the client itself. The latter is optional but highly desirable parameter. It usually contains the functional description of the client and its version, which helps the owner in administrative tasks. In case of our example, the client is represented by:  
* <span class="text-caption">client key</span>: k1uckqabs
* <span class="text-caption">description</span>: Cold Vision Monitor. V: 1.0.2

GuardPost has been assigned the <span class="text-role">Operator</span> and <span class="text-role">User</span> roles, so the client application will interact with the IP cameras in accondance with these roles.  

There can be multiple clients on the site associated with a user. In the following image, the second client "Cold Vision Remote Control. V: 2.2.1" is set up for GuardPost user:

![]({{ site.baseurl }}{% link assets/images/image_clt.1_5.png %})

To the left of each client entity, except for the clients of Contact users, there is a "<span class="text-cyan">&gt;&gt;</span>" button, clicking on which opens the client editor:

![]({{ site.baseurl }}{% link assets/images/image_clt.1_6.png %})

The client editor contains two menu buttons. The first button "<span class="text-cyan">account</span>" provides access to account information. The second button "<span class="text-cyan">ping period</span>" allows you to set the ping period. So what is the client ping period? Its purpose is similar to that discussed in the "[Ping Period]({{ site.baseurl }}{% link docs/ssite/device-mgt.md %}#644-ping-period)" section for a service application. If the device hosting your client application is highly mobile, it may change its IP address quite often. And when it happens, the client is unable to receive events from the Softnet platform until the client app detects that the device's address is changed and re-establishes the control channel. Depending on the underlying platform, the time required to detect a broken control channel can vary quite widely. However, using the Ping Period parameter, you can tune this time as you need. The Ping Period is the amount of time to wait between ping messages that the client app on the device sends to the site. If the ping message is not responded within a certain period of time, the control channel is considered as broken, and the client app re-establishes the control channel.  

Clicking the "<span class="text-cyan">ping period</span>" button opens the Ping Period editor: 

![]({{ site.baseurl }}{% link assets/images/image_clt.1_7.png %})

By default, the Ping Period is 300 seconds (5 minutes). The developer or the device user can set a specific ping period on the device, or leave it at the default value by specifying 0. The Ping Period can also be set here on the management panel. If you specify a value between 10 secondts and 300 seconds, it will overwrite the value set on the device. However, if you specify 0, the Ping Period will be set to the device’s local value, or to the default value of 300 seconds if the device’s local value is also 0.

In the image below, the ping period is set to 30 seconds. It is shown as "<span class="text-green">P</span>: 30":

![]({{ site.baseurl }}{% link assets/images/image_clt.1_8.png %})

---
#### TABLE OF CONTENTS
* 10.1. It's just a piece of cake
* [10.2. Clients of shared devices]({{ site.baseurl }}{% link docs/clients/shared.md %})
