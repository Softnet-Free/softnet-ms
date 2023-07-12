---
layout: default
title: 11.1. Stateful guest clients
parent: 11. Guest access
nav_order: 1
---

## 11.1. Stateful guest clients

If the service supports stateful guest clients, the site on which it is set up acquires two more sections: <span class="text-blue">guest status</span> and <span class="text-blue">guest page</span>. In the image below, IP cameras called <span class="text-st">RTX-5</span> (<span class="text-st">Cold Vision</span>) support stateful guest clients:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_1.png %})

1) The <span class="text-blue">guest status</span> section displays the allowed/denied status of **Guest** and a button to change this status to the opposite one. If you remember, Guest is a generic domain user that represents all anonymous clients. If the Guest status is set to <span class="text-green">allowed</span>, Guest is placed in the <span class="text-blue">users</span> section and guest clients are allowed. Otherwise, if it is set to <span class="text-red">denied</span>, Guest is placed in the <span class="text-red">DENIED USERS</span> section and guest clients are denied.  
2) The <span class="text-blue">guest page</span> section displays the guest page URL, where any Softnet user can create stateful guest clients to communicate with the service set up on the site even if he/she has no registration on the Softnet MS.  

### 11.1.1. Guest client management by registered Softnet users

A person or organization registered with a given Softnet network, can easily create and manage stateful guest clients for any public service on this network. On the guest page of a site, a logged-in person follows the same procedure for setting up guest clients on the site as for regular clients from named domain users.  

In the following image, Julia Robinson opened the guest page of the site with two IP cameras deployed by Markus Schmidt. The page is located at "<span style="color:#3399FF">http://ts.softnet-iot.org/guest.aspx?site=d8p585b3p</span>", which is displayed in the "<span class="text-blue">guest page</span>" section of a demo site shown above:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_9.png %})

Julia can create and manage guest clients on this site in the same way as regular clients. Curretly, she  has two guest clients.  

A registered Softnet user can manage all their guest clients on the "Public -> My Guest Clients" menu section. The <span class="header-green">OWNERS AND DOMAINS</span> page lists owners and their domains in which the user has guest clients. In the next image, Julia Robinson has guest clients in the "Holiday Vision" domain:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_10.png %})

The next image shows that Julia has two guest clients in this domain:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_11.png %})

### 11.1.2. Guest client management by anonymous users

A person who does not have an account on a given Softnet network, i.e. an anonymous user, can create stateful guest clients using their email. The procedure consists of three steps. In the first step, the user opens the guest page using the URL displayed on the site. On the guest page, the user sends a confirmation mail to his/her email. In the second step, the user goes to their email and opens the confirmation mail from the inbox. In the third step, the user navigates to the URL from the confirmation mail, which takes him/her to the page called “New Guest Client by EMail”. This page contains a  "<span class="text-green">create a guest client</span>" button that, when clicked, creates a client entity for a stateful guest client. This type of clients are called **guest clients by email**.  

In the image below, a guest page for "SITE_1" located at "<span style="color:#3399FF">http://ts.softnet-iot.org/guest.aspx?site=d8p585b3p</span>" is shown:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_2.png %})

I sent a confirmation mail to my email and received a guest client creation URL. In the next image, this URL is navigated:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_3.png %})

Clicking the "<span class="text-green">create a guest client</span>" button creates a stateful guest client like in the next image:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_4.png %})

You can browse and manage all guest clients you created using the email address on the page called <span class="header-green">GUEST CLIENTS BY EMAIL</span>. Click on the main menu item "Guest Clients By EMail" to open this page:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_5.png %})

The page prompts you to enter your email address and send a confirmation mail which contains a browsing URL. Navigating this URL opens the <span class="header-green">OWNERS AND DOMAINS</span> panel that displays owners and their domains where you have guest client entities. A browsing URL is valid for 7 days. In the image below, you can see what this page has displayed for my email address that I provided to the form above. It shows that I have guest client entities in the “Holiday Vision” domain that belongs to Markus Schmidt:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_6.png %})

The next image shows that I have 3 guest clients in this domain. Note that a browsing URL only allows an anonymous user to browse client entities, not edit them:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_7.png %})

To edit any of those clients, the browsing panel offers the user to send an editing URL to the same email address by which the user created the browsing URL. Then the user can navigate this URL from the inbox of their email and edit the guest client. An editing URL is only valid for 30 minutes. On the browsing panel, the user can also send a confirmation mail to create a new guest client:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_8.png %})

---
#### TABLE OF CONTENTS
* 11.1. Stateful guest clients
* [11.2. Conventional guest clients]({{ site.baseurl }}{% link docs/guest/stateless.md %})