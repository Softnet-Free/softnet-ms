---
layout: default
title: 3.3. Assigning access rights to users
parent: 3. Deploying a single device
nav_order: 3
---

## 3.3. Assigning access rights to users

Let’s say the project owner has a family member that also want to have a remote control client on their smartphone. It would be quite reasonable if the owner assigns the <span class="text-role">Administrator</span> role to the Owner user (i.e., to himself/herself) and the <span class="text-role">User</span> role to a family member's user.  

At this point, we have a user called Owner in the domain and we'll create another user, Alex, for a family member. Then we'll assign various levels of access rights for the service to the users Owner and Alex.  

Let's create a new user, Alex. First, we go to the domain page by clicking the domain name at the top left of the panel:

![]({{ site.baseurl }}{% link assets/images/image_sdp.3_1.png %})

Here is the view of our domain page:  

![]({{ site.baseurl }}{% link assets/images/image_sdp.3_2.png %})

Clicking the "new user" button takes us to the "New User" page:  

![]({{ site.baseurl }}{% link assets/images/image_sdp.3_3.png %})

Here, we can create a **Private** user or a **Contact** user. [Chapter 8]({{ site.baseurl }}{% link docs/contacts/index.md %}) demonstrates how to share your devices with other persons or organizations via **Contact** users. This is a more convenient way to share devices. However, in this example we’ll create a **Private** user associated with an imaginary family member.  

We type the name "Alex" in the "user name" field of "PRIVATE USER", leave the "Dedicated" checkbox unchecked and click "Create". Now in the "USER LIST" section of the domain page appeared the user Alex:

![]({{ site.baseurl }}{% link assets/images/image_sdp.3_4.png %})

Then we go to the site configuration page by clicking the "config" button:  

![]({{ site.baseurl }}{% link assets/images/image_sdp.3_5.png %})

You can see that both users, Owner and Alex, are in the <span class="text-red">DENIED USERS</span> section. We'll now assign the <span class="text-role">Administrator</span> role to Owner, and the <span class="text-role">User</span> role to Alex.  

Clicking the "&gt;&gt;" button, which is to the right of Owner, opens the editor for managing roles of Owner:

![]({{ site.baseurl }}{% link assets/images/image_sdp.3_6.png %})

We check the <span class="text-role">Administrator</span> role and click "save". This results in Owner being moved from the <span class="text-red">DENIED USERS</span> section to the site:  

![]({{ site.baseurl }}{% link assets/images/image_sdp.3_7.png %})

Next, clicking the "&gt;&gt;" button for Alex opens the editor for managing roles of this user:

![]({{ site.baseurl }}{% link assets/images/image_sdp.3_8.png %})

We check the <span class="text-role">User</span> role and click "save". This results in Alex being moved from the <span class="text-red">DENIED USERS</span> section to the site:  

![]({{ site.baseurl }}{% link assets/images/image_sdp.3_9.png %})

Now, we are ready to set up clients on the site. This is a topic of the [next section]({{ site.baseurl }}{% link docs/single/sections/setup-clients.md %})

---
#### TABLE OF CONTENTS
* [3.1. Creating a domain]({{ site.baseurl }}{% link docs/single/sections/new-domain.md %})
* [3.2. Setting up a device]({{ site.baseurl }}{% link docs/single/sections/setup-dev.md %})
* 3.3. Assigning access rights to users
* [3.4. Setting up clients]({{ site.baseurl }}{% link docs/single/sections/setup-clients.md %})
