---
layout: default
title: 3.4. Assigning access rights to users
parent: 3. Quickly deploying identical devices
nav_order: 4
---

## 3.4. Assigning access rights to users

Let’s say John Doe's wife also want to have a remote control client on her smartphone. As a project owner, John Doe assigns the <span class="text-role">Administrator</span> role to Owner, i.e., to himself, and the <span class="text-role">User</span> role to a user associated with his wife.  

At this point, we have a user called Owner in the domain and we’ll create another user, Alison, for the owner's wife. Then we’ll assign them various levels of access rights for the service.  

Let’s create a new user, Alison. First, we go to the domain page by clicking the domain name "Home Surveillance" at the top left of the panel:

![]({{ site.baseurl }}{% link assets/images/image_mdp.4_1.png %})

Here is the view of our domain page:

![]({{ site.baseurl }}{% link assets/images/image_mdp.4_2.png %})

Clicking the “new user” button takes us to the “New User” page:

![]({{ site.baseurl }}{% link assets/images/image_mdp.4_3.png %})

Here, we can create a **Private** user or a **Contact** user. [Chapter 8]({{ site.baseurl }}{% link docs/contacts/index.md %}) demonstrates how to share your devices with other persons and organizations via **Contact** users. This is a more convenient way to share devices. However, in this example, we’ll create a **Private** user associated with an imaginary family member.  

We type the name "Alison" in the "user name" field of "PRIVATE USER", leave the "Dedicated" checkbox unchecked and click "Create". Now in the section "USER LIST" of the domain page, the user Alison appeared:

![]({{ site.baseurl }}{% link assets/images/image_mdp.4_4.png %})

Then we go to the site configuration page by clicking the "<span class="text-cyan">config</span>" button:  

![]({{ site.baseurl }}{% link assets/images/image_mdp.4_5.png %})

You can see that both users, Owner and Alison, are in the <span class="text-red">DENIED USERS</span> section. We'll now assign the <span class="text-role">Administrator</span> role to Owner, and the <span class="text-role">User</span> role to Alison.  

Clicking the "<span class="text-cyan">&gt;&gt;</span>" button, which is to the left of Owner, opens the editor for managing roles of Owner:

![]({{ site.baseurl }}{% link assets/images/image_mdp.4_6.png %})

We check the <span class="text-role">Administrator</span> role and click "<span class="text-green">save</span>". This results in Owner being moved from the <span class="text-red">DENIED USERS</span> section to the site:  

![]({{ site.baseurl }}{% link assets/images/image_mdp.4_7.png %})

Next, clicking the "<span class="text-cyan">&gt;&gt;</span>" button for Alison opens the editor for managing roles of this user:

![]({{ site.baseurl }}{% link assets/images/image_mdp.4_8.png %})

We check the <span class="text-role">User</span> role and click "<span class="text-green">save</span>". This results in Alison being moved from the <span class="text-red">DENIED USERS</span> section to the site:  

![]({{ site.baseurl }}{% link assets/images/image_mdp.4_9.png %})

Now, we are ready to set up clients on the site. This is a topic of the [next section]({{ site.baseurl }}{% link docs/multi/setup-clients.md %})

---
#### TABLE OF CONTENTS
* [3.1. Creating a domain]({{ site.baseurl }}{% link docs/multi/new-domain.md %})
* [3.2. Creating a multi-service site]({{ site.baseurl }}{% link docs/multi/msite.md %})
* [3.3. Setting up devices]({{ site.baseurl }}{% link docs/multi/setup-devs.md %})
* 3.4. Assigning access rights to users
* [3.5. Setting up clients]({{ site.baseurl }}{% link docs/multi/setup-clients.md %})