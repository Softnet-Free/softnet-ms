---
layout: default
title: 9.2. User management
parent: 9. Users & access rights
nav_order: 2
---

## 9.2. User management

This section describes the features of various types of domain users and operations on them. It uses the "Office Automation" demo project to demonstrate these operations. Initially, a domain with two integrated users looks like this:

![]({{ site.baseurl }}{% link assets/images/image_usr.2_1.png %})

To add a new user, click the "<span class="text-blue">new user</span>" button. It takes you to the following page:

![]({{ site.baseurl }}{% link assets/images/image_usr.2_2.png %})

The <span class="header-green">NEW USER</span> panel contains three sections. The first section <span class="text-subheader">PRIVATE USER</span> is for creating a Private user. It contains a text field "user name", and a checkbox labeled "Dedicated". As you can see, the <span class="text-subheader">CONTACT USER</span> section also contains a "Dedicated" checkbox. This can be a useful feature in certain circumstances. We'll look at what it means for a user to be **dedicated** at the end of this section. To create a Private user, enter the name of a user in the "user name" field, select the value for the "Dedicated" checkbox and click "Create". In the following image, a private user GuardPost is being created in the "Office Automation" domain of our demo project:

![]({{ site.baseurl }}{% link assets/images/image_usr.2_3.png %})

After adding two Private users, GuardPost and Assistant, the list of users in "Office Automation" looks like this:

![]({{ site.baseurl }}{% link assets/images/image_usr.2_4.png %})

The <span class="text-subheader">CONTACT USER</span> section of the <span class="header-green">NEW USER</span> panel is for creating a Contact user:

![]({{ site.baseurl }}{% link assets/images/image_usr.2_5.png %})

First you need to select a contact from the contact list. If the user default name has been previously set for the selected contact, it is populated in the "user name" field. In the following image, a contact "Ben Stewart" is selected. The user default name “Stewart” was previously set for this contact, so it is populated in the “user name” field:

![]({{ site.baseurl }}{% link assets/images/image_usr.2_6.png %})

Clicking the "Create" button adds a new user. After adding two Contact users, Stewart and Robinson, the list of users in "Office Automation" looks like this:

![]({{ site.baseurl }}{% link assets/images/image_usr.2_7.png %})

Each site has the ability to specify the default rights for domain users to access the service. However, this only applies to users who are not marked as dedicated. Now let's see how they look like the default access rights. If the site employs Role-Based Access Control, the owner can specify a default role for all domain users by setting the "<span class="text-blue">user default role</span>" option to one of the roles declared on the site. If such a role is specified, for each user who equired this role, it will be underlined.  


 If the site employs Plain Access Control, the owner can set the "Implicit users" option of the site to <span class="text-green">allowed</span>.  


