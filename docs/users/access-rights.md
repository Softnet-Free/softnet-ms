---
layout: default
title: 9.3. User rights management
parent: 9. Users & access rights
nav_order: 3
---

## 9.3. User rights management

This section discusses how to manage access rights of users for various services in a domain. Softnet supports two kinds of access control: Role-Based Access Control (RBAC) and Plain Access Control (PAC). Which kind of access control is used by a given site depends on the Site Structure applied to the site. The Site Structure, as you know, is provided by the service application hosted on a device and set up on the site.  

To demonstrate operations with user access rights, the "Office Automation" demo project is used. [This is how the project's domain looks before assigning access rights to users]({{ site.baseurl }}{% link docs/users/demo-with-users.md %}).

### 9.3.1. Managing user rights on a site that uses RBAC

If the service application set up on the site employs role-based access control, the list of roles are displayed on the site in the "<span class="text-blue">supported roles</span>" section. In the image below, IP cameras support three user roles: "<span class="text-role">Administrator</span>", "<span class="text-role">Operator</span>" and "<span class="text-role">User</span>": 

![]({{ site.baseurl }}{% link assets/images/image_usr.3_1.png %})

In the <span class="header-green">SITE CONFIGURATION</span> panel, the user roles displayed in the "<span class="text-blue">supported roles</span>" section can be assigned to domain users. Users with one or more roles are displayed in the "<span class="text-blue">users</span>" section of the site. Users without any roles are displayed in the <span class="text-red">DENIED USERS</span> section. To the left of each domain user, there is a "<span class="text-cyan">&gt;&gt;</span>" button that, when clicked, opens the user role editor. You can check the roles you want to assign to the user and click the "<span class="text-green">save</span>" button. In the image below, the role editor is opened for Stewart, and the "<span class="text-role">User</span>" role is checked:

![]({{ site.baseurl }}{% link assets/images/image_usr.3_2.png %})

Clicking the "<span class="text-green">save</span>" button assigns the role to the user and moves it to the "<span class="text-blue">users</span>" section of the site:

![]({{ site.baseurl }}{% link assets/images/image_usr.3_3.png %})

Stewart is a Contact user associated with the contact Ben Stewart. Now he can create client entities and set up client applications that can interact with IP cameras with the rights of the "<span class="text-role">User</span>" role. [Here you can see another complete example of granting access to IP cameras to a contact]({{ site.baseurl }}{% link docs/contacts/using-contacts.md %}).  

In addition, we assign the "<span class="text-role">Administrator</span>" role to Owner, and the "<span class="text-role">Operator</span>" role to GuardPost. After this we have the following view of the "<span class="text-blue">users</span>" section:

![]({{ site.baseurl }}{% link assets/images/image_usr.3_4.png %})

### 9.3.2. Managing user rights on a site that uses PAC

### 9.3.3. Default access rights & dedicated users

Each site has an option to specify the default rights for domain users to access the service. However, this only applies to users who are not marked as dedicated. Using default rights may be convenient if you have more than a few users in the domain. This allows you to assign specific access rights to all users without having to do so explicitly for each user. Let's look at how to apply default access rights.  

If the site employs Role-Based Access Control, the owner can specify a default role for all domain users by setting the "<span class="text-blue">user default role</span>" option to one of the roles declared on the site. If such a role is specified, for each user who equired this role, it will be underlined.  


If the site employs Plain Access Control, the owner can set the "Implicit users" option of the site to <span class="text-green">allowed</span>.  


---
#### TABLE OF CONTENTS
* [9.1. Demo project]({{ site.baseurl }}{% link docs/users/demo.md %})
* [9.2. User management]({{ site.baseurl }}{% link docs/users/user-mgt.md %})
* 9.3. Assigning access rights