---
layout: default
title: 11.1. Stateful guest clients
parent: 11. Guest access
nav_order: 1
---

## 11.1. Stateful guest clients

If the service supports stateful guest clients, the site on which it is set up acquires two more sections: <span class="text-blue">guest status</span> and <span class="text-blue">guest page</span>. In the image below, IP cameras called <span class="text-st">RTX-5</span> (<span class="text-st">Cold Vision</span>) supports stateful guest clients:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_1.png %})

1) The <span class="text-blue">guest status</span> section displays the allowed/denied status of **Guest** and a button to change this status to the opposite one. If you remember, Guest is a generic domain user that represents all anonymous clients. If the Guest status is set to <span class="text-green">allowed</span>, Guest is placed in the <span class="text-blue">users</span> section and guest clients are allowed. Otherwise, if it is set to <span class="text-red">denied</span>, Guest is placed in the <span class="text-red">DENIED USERS</span> section and guest clients are denied.  
2) The <span class="text-blue">guest page</span> section displays the guest page URL, where any Softnet user can create stateful guest clients to communicate with the service even if he/she has no registration on the Softnet MS.  

### 11.1.1. Guest clients by email

If a Softnet user does not have a Softnet MS account, a stateful client can be created by an anonymous user in three steps. In the first step, the user opens the guest page using the URL displayed on the site. On the guest page, the user sends a confirmation mail to his/her email. In the second step, the user goes to their email and opens the confirmation mail from the inbox. In the third step, the user navigates to the URL from the confirmation mail, which takes him/her to the page called “New Guest Client by EMail”. This page contains a  "<span class="text-green">create a guest client</span>" button that, when clicked, creates a client entity for a stateful guest client. This type of clients are called "guest clients by email". In the image below, a guest page for "SITE_1" located at "<span style="color:#3399FF">http://ts.softnet-iot.org/guest.aspx?site=d8p585b3p</span>" is shown:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_2.png %})

In the next image, a guest client creation URL contained in the confirmation mail is navigated:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_3.png %})

Clicking the "<span class="text-green">create a guest client</span>" button creates a stateful guest client like in the next image:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_4.png %})