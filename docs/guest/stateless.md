---
layout: default
title: 11.2. Conventional guest clients
parent: 11. Guest access
nav_order: 2
---

## 11.2. Conventional guest clients

Some services may support conventional guest clients that have no state on the server. In Softnet, they are also called stateless guest clients. If a given service supports stateless guest clients, the site on which it is set up acquires one more section: "<span class="text-blue">guest shared uri</span>. In this section, the site displays a URI that all stateless guest clients use to connect to the site.  

In the image below, IP cameras called <span class="text-st">RTX-7</span> (<span class="text-st">Cold Vision</span>) support stateless guest clients. In the "<span class="text-blue">guest shared uri</span>" section, a URI "softnet-ms://ibgf8ib6n@ts.softnet-iot.org" for conventional guest clients is displayed. Since the site is multi-service, the URI scheme has a format "softnet-ms":

![]({{ site.baseurl }}{% link assets/images/image_guest.2_1.png %})

In the next image, a single-service site displays a guest shared URI "softnet-ss://smm4ri56y@ts.softnet-iot.org". Since the site is single-service, the URI scheme has a format "softnet-ss":

![]({{ site.baseurl }}{% link assets/images/image_guest.2_2.png %})

---
#### TABLE OF CONTENTS
* [11.1. Stateful guest clients]({{ site.baseurl }}{% link docs/guest/stateful.md %})
* 11.2. Conventional guest clients