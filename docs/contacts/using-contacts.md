---
layout: default
title: 8.4. Using contacts
parent: 8. Contacts & partnerships
nav_order: 4
---

## 8.4. Using contacts

This section briefly demonstrates you how to give contacts access to devices. In the "[Multi-service site]({{ site.baseurl }}{% link docs/msite/index.md %})" chapter, there is an example where John Doe creates a "Home Surveillance" domain and deploys multiple IP cameras. Let's grant access to the IP cameras from that example to the contact we've created in this chapter. The following image shows the John Doe's domain "Home Surveillance":  

![]({{ site.baseurl }}{% link assets/images/image_cont.4_1.png %})

The domain contains two users Owner and Guest. Owner is associated with the device owner, i.e., John Doe. He is already assigned the "<span class="text-role">Administrator</span>" role. And now we'll create a Contact user for Karina Koifman and assign her the "<span class="text-role">User</span>" role. Clicking the "<span class="text-cyan">new user</span>" button takes us to the <span class="header-green">NEW USER</span> page:

![]({{ site.baseurl }}{% link assets/images/image_cont.4_2.png %})

Here, we select the contact "Karina Koifman". The name "Karina", which is the default name for this contact, is substituted in the "user name" field by the form itself. We do not change it. Then we check the "Enabled" box and uncheck the "Dedicated" box:

![]({{ site.baseurl }}{% link assets/images/image_cont.4_3.png %})

Clicking on the "Create" button takes us back to the domain page, where a new Contact user Karina has appeared in the user list:

![]({{ site.baseurl }}{% link assets/images/image_cont.4_4.png %})

Now we'll assign her the "<span class="text-role">User</span>" role. Clicking on the "<span class="text-cyan">config</span>" button of the site opens the <span class="header-green">SITE CONFIGURATION</span> page:

![]({{ site.baseurl }}{% link assets/images/image_cont.4_5.png %})

Here, the user Karina is in the <span class="text-red">DENIED USERS</span> section. Clicking the "<span class="text-cyan">&gt;&gt;</span>" button, which is to the left of Karina, opens the editor for managing roles:

![]({{ site.baseurl }}{% link assets/images/image_cont.4_6.png %})

We check the <span class="text-role">User</span> role and click "<span class="text-green">save</span>". This results in Karina being moved from the <span class="text-red">DENIED USERS</span> section to the site: 

![]({{ site.baseurl }}{% link assets/images/image_cont.4_7.png %})

On the site, the name of a contact user is followed by the contact name in angle brackets. In our example, the name "Karina" is followed by the contact name "Karina Koifman" in angle brackets.  

We are done with giving Karina Koifman access to the IP cameras. Now we'll take a look at how she can consume these devices. The following is an account of Karina Koifman in Softnet MS:

![]({{ site.baseurl }}{% link assets/images/image_cont.4_8.png %})

Among recent contacts we can see John Doe. Clicking on it opens the contact page:

![]({{ site.baseurl }}{% link assets/images/image_cont.4_9.png %})

In the <span class="header-green">CONTACT DOMAINS</span> list, there is a "Home Surveillance" domain shared by John Doe. Clicking on it opens the contact domain page:

![]({{ site.baseurl }}{% link assets/images/image_cont.4_10.png %})

Here, Karina can create client entities and set up client applications that able to interact with IP cameras of type RTX-5 (Cold Vision). The "<span class="text-green">add client</span>" button adds a new client entity. The following images show setting up a client app called "Cold Vision Monitor".

![]({{ site.baseurl }}{% link assets/images/image_cont.4_11.png %})

After the first connection of the client app to the site, in the Karina's account we have this:

![]({{ site.baseurl }}{% link assets/images/image_cont.4_12.png %})

And the following image shows how this client appears in the John Doe's account:

![]({{ site.baseurl }}{% link assets/images/image_cont.4_13.png %})

As you can see, the device owner can only view clients created by their partners, but not edit them.

---
#### TABLE OF CONTENTS
* [8.1. MY CONTACTS]({{ site.baseurl }}{% link docs/contacts/my-contacts.md %})
* [8.2. Sending a contact invitation]({{ site.baseurl }}{% link docs/contacts/sending-inv.md %})
* [8.3. Handling a contact invitation]({{ site.baseurl }}{% link docs/contacts/handling-inv.md %})
* 8.4. Using contacts