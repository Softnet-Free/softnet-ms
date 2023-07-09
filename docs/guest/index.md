---
layout: default
title: 11. Guest access
nav_order: 11
---

# 11. Guest access

Some service applications may support guest access. It is convenient for users as guest clients do not require registration. Let's see how guest access is implemented in Softnet. Traditionally, a guest client has no state on the server as it has no account. However, some client-server interaction scenarios require that clients preserve the state on the server between reconnections. Imagine that some client makes a request to the service, but the response might be ready after an indefinite period of time. The request-response session cannot last such a long time and completes before session timeout expires. When the requested data is ready, the service needs to deliver it to the client. In Softnet, services use Private events for this purpose. However, Private events can only be sent to stateful (registered) clients. So that guest clients could also receive Private events, they are implemented as stateful clients, each with an account on the server and unique URI. If a Softnet service supports a guest access mode, it is called a public service. Any person can find any public service in a Softnet network and create a stateful guest client without even being logged into the Softnet Management System. If the service supports stateful guests, the site on which it is set up acquires two more sections: <span class="text-blue">guest status</span> and <span class="text-blue">guest page</span>. In the image below, IP cameras called <span class="text-st">RTX-5</span> (<span class="text-st">Cold Vision</span>) supports stateful guest clients:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_1.png %})

1) The <span class="text-blue">guest status</span> section displays the allowed/denied status of **Guest** and a button to change this status to the opposite one. If it is set to <span class="text-green">allowed</span>, Guest is placed in the <span class="text-blue">users</span> section and guest clients are allowed. Otherwise, if it is set to <span class="text-red">denied</span>, Guest is placed in the <span class="text-red">DENIED USERS</span> section and guest clients are denied.  
2) The <span class="text-blue">guest page</span> section displays the guest page URL, where any Softnet user can create stateful guest clients to communicate with the service even if he/she has no registration on the Softnet MS.  

If a Softnet user is not signed in to Softnet MS, a stateful client can be created on the guest page using the user's email. The guest page offers to send a confirmation mail to the user's email and follow the url from the inbox of the email to create the client entity for a statefull guest client. This type of clients are called "Guest Clients by EMail". In the image below, the guest page for the "SITE_1" considered above is shown:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_2.png %})

In the next image, a guest client creation URL contained in the confirmation mail is opened:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_3.png %})

Clicking the "<span class="text-green">create a guest client</span>" button creates a stateful guest client like in the next image:

![]({{ site.baseurl }}{% link assets/images/image_guest.1_4.png %})