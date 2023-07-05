---
layout: default
title: 9.3. Assigning access rights
parent: 9. Users & access rights
nav_order: 3
---

## 9.3. Assigning access rights

This section discusses how to assign access rights to users for various services in a domain. Softnet supports two kinds of access control mechanisms: Role-Based Access Control (RBAC) and Plain Access Control (PAC). Which kind of access control is used by a given site is defined by the Site Structure provided by the service and applied to the site.  

The demo project "[Office Automation]({{ site.baseurl }}{% link docs/users/office-automation.md %})" is used to demonstrate operations with access rights.

### 9.3.2. Default access rights & dedicated users

Each site has an option to specify the default rights for domain users to access the service. However, this only applies to users who are not marked as dedicated. Using default rights may be convenient if you have more than a few users in the domain. This allows you to assign specific access rights to all users without having to do so explicitly for each user. Let's look at how to apply default access rights.  

If the site employs Role-Based Access Control, the owner can specify a default role for all domain users by setting the "<span class="text-blue">user default role</span>" option to one of the roles declared on the site. If such a role is specified, for each user who equired this role, it will be underlined.  


If the site employs Plain Access Control, the owner can set the "Implicit users" option of the site to <span class="text-green">allowed</span>.  


---
#### TABLE OF CONTENTS
* [9.1. Demo project]({{ site.baseurl }}{% link docs/users/demo.md %})
* [9.2. User management]({{ site.baseurl }}{% link docs/users/user-mgt.md %})
* 9.3. Assigning access rights