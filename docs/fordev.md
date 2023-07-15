---
layout: default
title: 13. For developers
nav_order: 13
---

# 13. For developers

A service application, when it connects to a blank site for the first time, supplies a **Site Structure** object to the platform, which uses it to build the structure of the site. Whenever the service application reconnects to the site, the platform verifies if the current Site Structure object attached to the service app matches the original one that was used to build the site structure. Typically, if the service application is the same, then the Site Structure object is always the same as well. However, if you are a developer and you are developing a service application utilizing the Softnet platform, things might be different.  

The Site Structure contains elements and declarations used to build the site with the structure needed for the service interface. And the service interface, as you know, is indicated by the names of the **Service Type** and **Contract Author**, which are also elements of the Site Structure. In Softnet MS, they are displayed in the following format: &lt;<span class="text-st">Service Type</span>&gt; (&lt;<span class="text-st">Contract Author</span>&gt;). During application development, you may change the content of the Site Structure object, and the next time you connect the application to the site for testing purposes, the service entity can get an error status on the site. if you change the name of the Service Type or the Contract Author, the service status will be "<span class="text-red">service type conflict</span>". If you change one of the other elements of the Site Structure, such as one of the event parameters, an event access rule, a user role name, or even the case of a letter in the role name or event name, the guest access support flag, or the flag of stateless guest support, the service status will be "<span class="text-red">site structure mismatch</span>".  

If the service application you are developing is given an error status, then you just need to rebuild the structure of the site. On the <span class="header-green">SITE CONFIGURATION</span> panel, clicking on the "<span class="text-cyan">structure</span>" button displays another button "<span class="text-green">apply structure to the site</span>" that allows you to rebuld the site.  

Let's see what changes may affect the current settings of the site. If you changed the name a role, it is considered as deleting that role and creating a new one. Therefore, the role will be removed from all users that have been assigned this role. If you change the name of an event, it is considered as deleting that event's definition and creating a new one. Therefore, all instances of this event queued in the event broker will be removed. Also, if you change the name of the Service Type and/or Contract Author, this change must be applied to all client apps of this service as well.  

In the following image, the service app supports two roles: "<span class="text-role">Admin</span>" and "<span class="text-role">User</span>". The role "<span class="text-role">Admin</span>" is assigned to Owner, and the role "<span class="text-role">User</span>" is specified as the user default role:

![]({{ site.baseurl }}{% link assets/images/image_fordev.1.png %})

If, for example, I change the role name "<span class="text-role">Admin</span>" to "<span class="text-role">admin</span>", I'll have the following error status:

![]({{ site.baseurl }}{% link assets/images/image_fordev.2.png %})

Clicking the "<span class="text-cyan">structure</span>" button displays another button "<span class="text-green">apply structure to the site</span>":

![]({{ site.baseurl }}{% link assets/images/image_fordev.3.png %})

Clicking this button rebuilds the structure of the site:

![]({{ site.baseurl }}{% link assets/images/image_fordev.4.png %})

As you can see, the role "<span class="text-role">Admin</span>" has been removed from the user Owner.  

Now, If I change the role name "<span class="text-role">User</span>" to "<span class="text-role">user</span>" and apply the updated structure to the site, this role will be removed from the "<span class="text-blue">user default role</span>" section and all users that are implicitly assigned this role will lose it:

![]({{ site.baseurl }}{% link assets/images/image_fordev.5.png %})