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

### 9.3.2. Managing user rights on a site that uses Plain Access Control

If the service application set up on the site employs plain access control, users have a full access to the service by the fact of being added to the site. PAC is used when the service application does not require different levels of access, or the application implements its own access control mechanism.  

In the <span class="header-green">SITE CONFIGURATION</span> panel, users added to the site explicitly are displayed in the "<span class="text-blue">explicit users</span>" section. Some users may be added to the site implicitly, which is the subject of the next subsection below. Users without access rights are displayed in the <span class="text-red">DENIED USERS</span> section. In the following image, Owner is explicitly added to the site "Alarm System" of our demo project:

![]({{ site.baseurl }}{% link assets/images/image_usr.3_5.png %})

In the <span class="text-red">DENIED USERS</span> section, to the left of each domain user, there is an "<span class="text-cyan">add</span>" button that, when clicked, adds a user to the site. Those users that are already added to the site has a "<span class="text-cyan">rem</span>" button that, when clicked, removes a user from the site.

### 9.3.3. Default access rights & dedicated users

Each site has an option to specify the default rights for users to access the service. However, this only applies to users who are not marked as dedicated. The dedicated users acquire only those rights that you assign them explicitly. Using default rights may be convenient if you have more than a few users in the domain. This allows you to assign some minimum access rights to all users without having to do so explicitly for each user. Let's look at how to apply default access rights, first when using RBAC and then when using PAC.   

1) **If the site employs Role-Based Access Control**, you can specify a default role for all domain users by setting the "<span class="text-blue">user default role</span>" option to one of the roles declared on the site. Each user that is given a default role will have it underlined. However, if some of the users must not have the default rights, you can make them dedicated. Note that dedicated users are also underlined.

Let's recall our demo site "Surveillance System". Earlier, we explicitly assigned roles to three users, and two Contact users remained in the <span class="text-red">DENIED USERS</span> section (Guest not considered):

![]({{ site.baseurl }}{% link assets/images/image_usr.3_6.png %})

Let's make "<span class="text-role">User</span>" the default role and see what happens:

![]({{ site.baseurl }}{% link assets/images/image_usr.3_7.png %})

Each user acquired the "<span class="text-role">User</span>" role. As the default role, it is underlined except for the Assistant, which is explicitly assigned this role. Assume we do not want Stewart to have any access to the IP cameras, then we make it dedicated so that it could not acquire the default role:

![]({{ site.baseurl }}{% link assets/images/image_usr.3_8.png %})

After clicking "<span class="text-green">save</span>" we have the following view (note that Stewart is underlined as dedicated user):

![]({{ site.baseurl }}{% link assets/images/image_usr.3_9.png %})

2) **If the site employs Plain Access Control**, you can set the "Implicit users" option to "<span class="text-green">allowed</span>" to add the domain users to the site implicitly. The option is displayed in the "<span class="text-blue">access defaults</span>" section. However, you may want to prevent certain users from being added to the site by applying this option. In this case, you can make them dedicated. Note that implicit and explicit users have equal access rights to the service.  

Let's consider the demo site "Alarm System". Currently, the "Implicit users" option is set to "<span class="text-red">denied</span>":

![]({{ site.baseurl }}{% link assets/images/image_usr.3_10.png %})

Clicking the "<span class="text-green">allow</span>" button makes the "Implicit users" option allowed:

![]({{ site.baseurl }}{% link assets/images/image_usr.3_11.png %})

Users implicitly added to the site are moved to the "<span class="text-blue">implicit users</span>" section. To the left of each user in this section, an "<span class="text-cyan">exp</span>" button is displayed, clicking on which makes the user explicitly added to the site and moves it to the "<span class="text-blue">explicit users</span>" section. Note that because Stewart is a dedicated user, the default access settings are not applied to it.

---
#### TABLE OF CONTENTS
* [9.1. Demo project]({{ site.baseurl }}{% link docs/users/demo.md %})
* [9.2. User management]({{ site.baseurl }}{% link docs/users/user-mgt.md %})
* 9.3. Assigning access rights